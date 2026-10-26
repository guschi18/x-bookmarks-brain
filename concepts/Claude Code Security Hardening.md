---
tags: [security, agents, tools]
sources: [tweet-2042086577636061436.md, tweet-2110974023299699003.md, tweet-2114023867916112257.md]
created: 2026-10-22
updated: 2026-10-26
---

# Claude Code Security Hardening

## Überblick (Stand 2026-04)

Ein X-Artikel (verlinkt aus dem Post von noisyb0y1) beschreibt drei Stufen, um [Claude Code](../entities/Claude%20Code.md) gegen Datenabfluss durch Prompt Injection abzusichern, etwa über eine CLAUDE.md in einem geklonten Repository. Die genannten Zahlen (55 % leaken Nutzerdaten, 8.000 bis 50.000 USD Schaden, 197 Tage bis zur Entdeckung, 84 % weniger Bestätigungsdialoge) sind im Artikel ohne nachprüfbare Quelle; die beiden "bis 2.0.65 ungepatchten kritischen Lücken" sind eine Behauptung des Autors. [tweet-2042086577636061436](../sources/tweet-2042086577636061436.md)

## Stufe 1, 15 Minuten (Stand 2026-04)

- `/sandbox` mit Auto-allow-Modus aktivieren. Laut Artikel greifen Deny-Regeln ohne Sandbox nur für eingebaute Tools; Bash-Befehle umgingen sie. Mit Sandbox wirken sie auf OS-Ebene (Seatbelt unter macOS, bubblewrap unter Linux; dort vorher `bubblewrap` und `socat` installieren). [tweet-2042086577636061436](../sources/tweet-2042086577636061436.md)
- `~/.claude/settings.json` mit einer Allow-Liste für Routinebefehle (npm run/test, prettier, eslint, git status/diff/log/commit, ls, cat, grep) und einer Deny-Liste: Lesen von `~/.ssh`, `~/.gnupg`, `~/.aws`, `~/.azure`, `~/.kube`, `~/.npmrc`, `~/.git-credentials`, `~/.config/gh`, `*.env` und `.env.*`; Bearbeiten von `~/.bashrc` und `~/.zshrc`; Bash-Befehle curl, wget, nc, ssh und git push. [tweet-2042086577636061436](../sources/tweet-2042086577636061436.md)
- `enableAllProjectMcpServers: false`, damit bösartige MCP-Konfigurationen in fremden Repositories nicht automatisch laden, und `sandbox.filesystem.denyRead` für `.env`-Dateien als zweite Schicht. [tweet-2042086577636061436](../sources/tweet-2042086577636061436.md)
- `claude update` ausführen; der Artikel empfiehlt das monatlich. [tweet-2042086577636061436](../sources/tweet-2042086577636061436.md)

## Stufe 2, 30 Minuten: Trail of Bits (Stand 2026-04)

Der Artikel verweist auf das Setup von Trail of Bits: `claude plugin marketplace add trailofbits/skills` und danach `/trailofbits:config`, das vorhandene Komponenten prüft und fehlende ergänzt. Genannt werden Workflow-Hooks (Planung vor Code, strukturiertes Debugging, Prüfung vor Auslieferung), Security-Skills, eine CLAUDE.md-Vorlage gegen spekulative Features und unnötige Abhängigkeiten sowie die Skill-Kette brainstorm, plan, execute, verify. [tweet-2042086577636061436](../sources/tweet-2042086577636061436.md)

## Stufe 3, rund 1 Stunde: Devcontainer (Stand 2026-04)

Claude läuft in einem Container ohne Zugriff auf SSH-Schlüssel, Cloud-Zugangsdaten und Dateien außerhalb des Projekts (`@devcontainers/cli` plus Repository `trailofbits/claude-code-devcontainer`; `devc .`, `devc shell`, `devc sync`). Innerhalb des Containers ist bypassPermissions aktiv, weil der Container die Grenze bildet. Gedacht ist das für verdächtige Repositories oder Kundencode. [tweet-2042086577636061436](../sources/tweet-2042086577636061436.md)

## Einordnung und Grenzen

Eine spätere Dokumentationsprüfung zu Claude Code (Stand 2026-05) hält fest, dass die Permissions-Dokumentation Deny-Regeln beschreibt, aber keinen vollständigen Prozess-Sandbox; indirekte Dateizugriffe über Python oder Node seien nicht abgedeckt. Die Artikelaussage, `/sandbox` schließe diese Lücke auf OS-Ebene, ist damit nicht unabhängig bestätigt; die Befehlsreferenz führt `/sandbox` lediglich als vorhandenen Befehl (Stand 2026-06). Beide Aussagen sind getrennt datiert und stehen auf [Claude Code](../entities/Claude%20Code.md). [tweet-2042086577636061436](../sources/tweet-2042086577636061436.md)

Die Deny-Liste ist ein Beispiel aus dem Artikel, keine geprüfte Sicherheitskonfiguration; ein Block von curl und git push kann legitime Arbeitsabläufe stören. [tweet-2042086577636061436](../sources/tweet-2042086577636061436.md)

## Sicherheitsprüfung vor dem Merge (Stand 2026-10)

Der Supabase-CTO nennt als häufigsten Anfängerfehler, den Agenten vor dem Produktivgang nicht um einfache Sicherheitstests zu bitten. Sein Vorschlag: das beste verfügbare Modell fragen, wie ein Angreifer dieses Projekt auf zehn Wegen brechen würde, und prüfen, ob der Schutz greift; dazu eine Regel, die diese Prüfung bei jedem Merge nach main auslöst. Das kostet Tokens und fängt laut ihm vor allem leicht erreichbare Lücken. [tweet-2110974023299699003](../sources/tweet-2110974023299699003.md)

Für Datenzugriff empfiehlt er eine Read Replica für Analysen und Datenbank-Branching für Entwicklungszweige, damit Agentenfehler die Produktivdaten nicht erreichen. Frühere Modelle hätten für schnelle Ergebnisse RLS abgeschaltet; das sei inzwischen besser. Das sind Erfahrungsaussagen des Gasts und keine geprüfte Konfiguration. Einordnung: [Supabase](../entities/Supabase.md). [tweet-2110974023299699003](../sources/tweet-2110974023299699003.md)

## Stripe-MCP: Schreibaktionen bestätigen (Stand 2026-10)

Daniel San beschreibt für den Stripe-MCP-Server (mcp.stripe.com), dass Lesetools harmlos sind, Schreibtools wie Rückerstattungen, Abos oder Treasury-Transfers aber vom Modell nicht anders behandelt werden. Er nennt die Einstellung permissions/stripe-mcp-confirm-writes aus Claude Code Templates, die eine Bestätigung vor Schreibaktionen erzwingen soll, auch im Auto-Modus: npx claude-code-templates@latest --mcp devtools/stripe --skill development/stripe-integration --setting permissions/stripe-mcp-confirm-writes. [tweet-2114023867916112257](../sources/tweet-2114023867916112257.md)

Evidenzgrenze: Der gespeicherte Artikeltext bricht nach der Einleitung ab; Regelwortlaut und Auto-Modus-Verhalten sind nicht belegt und nicht getestet. [tweet-2114023867916112257](../sources/tweet-2114023867916112257.md)
