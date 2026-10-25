---
tags: [agents, tools, product-building]
sources: [tweet-2090744569960824949.md]
created: 2026-09-29
updated: 2026-10-12
---

# Matt Pocock Skills

## Aktueller Stand (Stand 2026-10, geprüft 2026-10-12)

Diese Übersicht folgt dem [Repository am Commit 49dd158](https://github.com/mattpocock/skills/tree/49dd158d1076134a641b33efb035946536778336) vom 09.10.2026. Der [neueste veröffentlichte Release](https://github.com/mattpocock/skills/releases/tag/v1.3.1) ist v1.3.1; main enthält weitere Änderungen. Der August-Bookmark dient als Einstieg zur Primärquelle, nicht als aktuelle Anleitung. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

## Installation und Updates (Stand 2026-10)

Die [README](https://github.com/mattpocock/skills/blob/49dd158d1076134a641b33efb035946536778336/README.md) unterscheidet automatisch aktualisierte Plugins von manuell gepflegten Skill-Kopien. Pro Agent soll genau ein Installationsweg gewählt werden, damit Skills nicht doppelt erscheinen. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

| Agent | Installation laut aktueller README |
| --- | --- |
| [Claude Code](Claude%20Code.md) | claude plugin install mattpocock-skills@claude-plugins-official [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md) |
| [Codex](Codex.md) | codex plugin marketplace add mattpocock/skills; danach codex plugin add mattpocock-skills@mattpocock [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md) |
| Andere Agenten oder editierbare Dateien | npx skills@latest add mattpocock/skills -a &lt;agent&gt;; npx skills@latest update für Updates, erneut add für neue Skills. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md) |

Einmal pro Repository richtet [/setup-matt-pocock-skills](https://github.com/mattpocock/skills/blob/49dd158d1076134a641b33efb035946536778336/skills/engineering/setup-matt-pocock-skills/SKILL.md) Issue-Tracker, gegebenenfalls Triage-Labels und die Ablage für GLOSSARY.md und ADRs ein. GitHub, GitLab, lokale Markdown-Dateien und beschriebene eigene Tracker sind möglich. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

## Welchen Ablauf wählen? (Stand 2026-10)

[/ask-matt](https://github.com/mattpocock/skills/blob/49dd158d1076134a641b33efb035946536778336/skills/engineering/ask-matt/SKILL.md) ist die Orientierungshilfe. Im Arbeitsverzeichnis klärt /grill-with-docs die Idee und dokumentiert Domänensprache in GLOSSARY.md sowie Entscheidungen in ADRs; außerhalb eines Arbeitsverzeichnisses dient /grill-me der Klärung. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

Für größere Builds führt die Route über /to-spec und /to-tickets. Danach bearbeitet /implement einzelne Tickets oder /implement-spec orchestriert die gesamte Spec parallel. Für kleine Vorhaben reicht /implement in derselben Sitzung. TDD und Code-Review gehören zur Ausführung; /retro folgt anschließend. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

Eine lauffähig zu klärende Designfrage geht über /handoff in eine separate /prototype-Sitzung und mit Handoff zurück. Planung, Spec und Tickets behalten ihren gemeinsamen Kontext; einzelne Implementierungstickets starten danach frisch. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

[/wayfinder](https://github.com/mattpocock/skills/blob/49dd158d1076134a641b33efb035946536778336/skills/engineering/wayfinder/SKILL.md) ist für große, noch unklare Vorhaben. Eine Karte von Entscheidungstickets klärt den Weg; standardmäßig entstehen Entscheidungen, keine Implementierung. Danach folgt /to-spec vor der Ticket-Ausführung. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

## /implement-spec im aktuellen Stand (Stand 2026-10)

Die maßgebliche [Skill-Datei](https://github.com/mattpocock/skills/blob/49dd158d1076134a641b33efb035946536778336/skills/engineering/implement-spec/SKILL.md) liegt unter skills/engineering/implement-spec. Ziel ist die vollständig implementierte Spec auf einem Integrationsbranch; Tickets werden gemäß dem konfigurierten Tracker abgeschlossen. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

1. Spec und Abhängigkeitsgraph lesen; bei Bedarf Exploration mit gemeinsam erreichbaren Notizen. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)
2. Integrationsbranch erstellen und ausführbare Tickets parallel vergeben, jeweils mit eigenem Branch und Worktree. Kommunikation verweist auf Spec, Tickets, Notizen und Commits. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)
3. Implementer prüfen ihre Worktree-Basis, bauen per TDD und integrieren vor Abschluss den aktuellen Integrationsbranch. Ein Merger übernimmt die Arbeit; neu freigewordene Tickets starten anschließend. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)
4. Code-Review über den gesamten Integrationsbranch, Befunde beheben und Implementer-Worktrees aufräumen. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

Ein Draft-PR entsteht nur, wenn der Tracker über PRs abschließt oder der Nutzer ihn verlangt, und erst nach dem ersten Merge. Existiert ein PR, wird er reviewbereit; andernfalls werden Tickets im Tracker abgeschlossen und der Integrationsbranch gemeldet. Die frühere obligatorische PR-Erstellung vor Beginn ist ersetzt. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

## /retro und Regeln (Stand 2026-10)

Der aktuelle [/retro-Skill](https://github.com/mattpocock/skills/blob/49dd158d1076134a641b33efb035946536778336/skills/engineering/retro/SKILL.md) liest reale Sitzungen und schlägt Verbesserungen an Navigation, Checks, Regeln, Anweisungen, Werkzeugkosten und Informationszugang vor. Vorschläge werden nach Schwere präsentiert. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

Mechanisch erkennbare Fehler gehören in deterministische Lint-, Hook- oder CI-Prüfungen. [Coding Standards File](../concepts/Coding%20Standards%20File.md) ist für echte Ermessensfragen reserviert; das präzisiert die pauschale ältere Empfehlung, jeden bedeutsamen Fehler als Textregel einzutragen. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

## Aufrufmodell und Einordnung (Stand 2026-10)

User-invoked Skills wie /ask-matt, /implement-spec und /retro starten nur durch den Nutzer. Model-invoked Skills wie /tdd, /code-review, /pr und /writing-for-agents darf ein Agent bei Bedarf verwenden. Ein Skill darf keinen anderen user-invoked Skill selbst aufrufen. Die aktuelle README beschreibt diese Grenze. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)

Die Sammlung verbindet [Agentic Engineering](../concepts/Agentic%20Engineering.md), Planung und überprüfbare Ausführung; [AI Coding Dictionary](AI%20Coding%20Dictionary.md) behandelt Pococks Begriffsglossar. Der geprüfte Stand dokumentiert Anweisungen, keine unabhängig gemessenen Produktivitäts- oder Tokengewinne. Die Befehle wurden hier nicht installiert oder ausgeführt. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)
