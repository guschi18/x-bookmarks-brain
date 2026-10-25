---
tags: [agents, tools, product-building, security]
sources: [tweet-2040705762406895940.md, tweet-2012378465664745795.md]
created: 2026-10-21
updated: 2026-10-22
---

# Everything Claude Code

## Projekt und zeitliche Einordnung

Everything Claude Code (ECC) ist ein System aus Skills, Agentenrollen, Hooks, Regeln, Review- und Speicherabläufen für Coding-Harnesses. Das vom Nutzer bestätigte Repository ist [affaan-m/ECC](https://github.com/affaan-m/ECC/blob/90606c8315ee09cafc303515c5f33024db6b9882/README.md); der frühere Name everything-claude-code ist als historische URL zu behandeln. Der April-Tweet nennt 27 Agenten, 64 Skills und 33 Befehle; die gespeicherte spätere README beschreibt 2.2.2. Diese Zahlen werden nicht als aktueller April-Bestand ausgegeben. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

Bei der gesonderten Prüfung am 21.10.2026 nennen README und [Plugin-Manifest](https://github.com/affaan-m/ECC/blob/90606c8315ee09cafc303515c5f33024db6b9882/.claude-plugin/plugin.json) Version 2.2.3 sowie 71 Agenten, 311 Skills und 97 Befehls-Shims. Der geprüfte Commit 90606c8315ee09cafc303515c5f33024db6b9882 stammt vom 20.10.2026; README und Metadaten belegen den dokumentierten Projektstand, keine Wirksamkeit oder Sicherheitsprüfung. Die Quellen nennen MIT für das offene Repository und unterscheiden davon den gehosteten Pro-Dienst. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

## Arbeitsablauf und Auswahl

Der README-Ablauf lautet Plan → Test → Implementierung → Review → Verifikation → Erinnern → Verbessern. Für eine Änderung werden Planartefakt, zunächst fehlschlagender Test, bestandener Test und Review aus frischem Kontext als nachvollziehbare Ergebnisse verlangt. Praktische Einstiegspunkte sind /ecc:plan, tdd-workflow, /code-review und /build-fix; sie sind dokumentierte ECC-Oberflächen, hier nicht ausgeführte Befehle. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

ECC unterscheidet vier Aufgaben: Skills laden Verfahren bei Bedarf, Agenten isolieren Arbeit mit eigenen Werkzeugrechten und Kontexten, Regeln sind dauerhaft geladene Standards, Hooks laufen ereignisgesteuert außerhalb des Modellkontexts. Instincts ergänzen gelernte Muster mit Konfidenzwerten. Deshalb empfiehlt die README eine Auswahl nach Arbeitsablauf und Stack statt pauschal alle Komponenten zu laden. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

## Installation und Wartung (Nachrecherche 2026-10-21)

Die README nennt für den geführten Claude-Einstieg npx ecc-universal@2.2.3 setup mit Node.js ab 18, Git und [Claude Code](Claude%20Code.md) ab 2.1 auf PATH. Die native Alternative verwendet /plugin marketplace add https://github.com/affaan-m/ECC und /plugin install ecc@ecc. Pro Harness soll genau ein Installationsweg gewählt werden: Vollständige manuelle Kopie zusätzlich zum Plugin kann Skills und Hooks duplizieren. Diese Befehle dienen als belegter Stand, es wurde nichts installiert. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

Die [configure-ecc-Anleitung](https://github.com/affaan-m/ECC/blob/90606c8315ee09cafc303515c5f33024db6b9882/skills/configure-ecc/SKILL.md) beginnt bei Claude mit Bestandsaufnahme, Auswahl von User-/Projekt-/Local-Scope und Hook-Modus, Vorschau, einer Bestätigung und anschließender Prüfung. Sie trennt diese Claude-Scope-/Hook-Auswahl ausdrücklich vom [Codex](Codex.md)-Pfad. Die README nennt für [Codex](Codex.md) einen eigenen nativen Plugin-Lebenszyklus und kennzeichnet den alten Sync-Skriptweg als Kompatibilitätsoption; das ist eine ECC-Dokumentationsaussage, keine hier getestete [Codex](Codex.md)-Konfiguration. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

Für geringe Kontextlast dokumentiert die README minimale Installation ohne Hooks beziehungsweise gezielte Skills und Regelpakete. Eine Vollinstallation kopiert nicht bloß Wissen: Hooks können lokale Befehle ausführen. Nach Plugin-Installation soll hooks/hooks.json nicht nochmals manuell eingetragen werden. Vor Neuinstallation beschreibt das Projekt list-installed, doctor und repair; Deinstallation bietet eine Vorschau und orientiert sich an erfassten eigenen Dateien. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

## Konkrete Kontextregler

Die README dokumentiert ECC_SESSION_START_MAX_CHARS zum Begrenzen von Startzusätzen und ECC_SESSION_START_CONTEXT=off zum Abschalten dieses Zusatzkontexts. ECC_MAX_INJECTED_INSTINCTS begrenzt eingespielte Muster, ECC_INSTINCT_CONFIDENCE_THRESHOLD filtert nach Konfidenz und ECC_DISABLED_HOOKS schaltet ausgewählte Hook-IDs aus. Diese Optionen sind präzise Ansatzpunkte für [Context Engineering](../concepts/Context%20Engineering.md), keine hier gemessene Tokenersparnis. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

## Memory Vault und Übergaben

Der [Unified-Memory-Skill](https://github.com/affaan-m/ECC/blob/90606c8315ee09cafc303515c5f33024db6b9882/skills/unified-memory/SKILL.md) beschreibt portable ecc.memory.v1-Markdown-Dokumente: projektlokaler Kontext unter .ecc/memory/project/, zur menschlich geprüften gemeinsamen Ablage gedachter Team-Scope unter .ecc/memory/team/ und persönlicher Scope unter ~/.ecc/memory/. Normale Suche berücksichtigt aktive Projekt- und Team-Einträge; User-Scope wird explizit angefordert. Eine Harness-Bezeichnung ist ein Routingfilter, keine Benutzerberechtigung. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

Der dokumentierte Ablauf ist Suchen → relevante Erinnerung lesen → benötigten Zustand speichern oder übergeben → mit memory doctor prüfen. Ein Handoff nennt Ziel, aktuellen Zustand, Belege, betroffene Dateien, offene Punkte und nächsten Schritt. Inhalte werden über stdin oder --body-file übergeben. Skills allein installieren die nötige Memory-Runtime nicht; das Paket oder ein Repo-Checkout stellt die CLI separat bereit. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

Neue Einträge bleiben unreviewed und sind grundsätzlich create-only. Wichtige Aussagen müssen an aktuellen Quellen geprüft werden; Erinnerungstext ist weder Richtlinie noch Erlaubnis. Der optionale MCP-Server bietet nur Speichern, Suchen, Lesen und Prüfen; seine Identität wird serverseitig festgelegt. Das verhindert laut Design keine semantisch falsche oder veraltete Erinnerung automatisch. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

## Plattform- und Sicherheitsgrenzen

Die README kennzeichnet den Kern für Windows, macOS und Linux als unterstützt, stellt aber keine vollständige Funktionsgleichheit der Harnesses in Aussicht. Für natives Windows nennt sie ausdrücklich offene Fehler des Continuous-Learning-v2-Observer-Daemons und von Memory-Vault-Schreibpfaden; optionale Shell-Funktionen benötigen teilweise Git Bash oder WSL. Diese im aktuellen README genannten Grenzen sind für die Wahl einzelner Komponenten relevant und wurden hier nicht reproduziert. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

AgentShield wird als Scanner für Agentenanweisungen, Hooks, MCP-Konfiguration, Berechtigungen und Geheimnisse beschrieben. Die README setzt einen bereits installierten, geprüften Scanner voraus; ihre Testanzahl und Sicherheitsversprechen sind keine unabhängige Gesamtprüfung. Weder ECC noch AgentShield wurden ausgeführt oder an persönliche Daten angeschlossen. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

## Verbindung zum Lernrepo

[Claude Code Best Practice](Claude%20Code%20Best%20Practice.md) eignet sich laut seiner gesonderten Recherche zum Lernen und Nachschlagen; ECC dokumentiert zusätzlich installierbare Komponenten und einen wiederholbaren Arbeitsablauf. Für [Agentic Engineering](../concepts/Agentic%20Engineering.md) sind besonders die Trennung dauerhaft geladener Regeln von situativen Skills und nachvollziehbare Review-/Übergabeartefakte relevant. Dies ist eine Auswahlhilfe aus den dokumentierten Rollen, keine gemessene Überlegenheit eines Repos. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

## Ursprung im Shorthand-Setup des Autors (Stand 2026-01)

Der Autor Affaan beschreibt in einem Artikel das Claude-Code-Setup, aus dem das Projekt hervorging. Er nennt zehn Monate tägliche Nutzung, einen Hackathon-Sieg mit Claude Code und eine Aufteilung in Skills, Befehle, Hooks, Subagenten, Regeln, MCP-Server und Plugins; das sind Selbstangaben. [tweet-2012378465664745795](../sources/tweet-2012378465664745795.md) Das Regelpaket besteht dort aus security, coding-style, testing, git-workflow, agents, patterns, performance und hooks; die Agentenliste nennt unter anderem planner, architect, tdd-guide, code-reviewer, security-reviewer, build-error-resolver, e2e-runner, refactor-cleaner und doc-updater. [tweet-2012378465664745795](../sources/tweet-2012378465664745795.md) Die späteren Zahlen (Agenten, Skills, Befehle) oben beziehen sich auf spätere Stände und dürfen nicht auf diesen Januar-Stand übertragen werden. [tweet-2012378465664745795](../sources/tweet-2012378465664745795.md)
