---
tags: [agents, tools]
sources: [tweet-2052306848221680015.md]
created: 2026-10-13
updated: 2026-10-13
---

# CodeBurn

## Zweck und Einstieg (Stand 2026-05; gespeicherte README)

[getagentseal/codeburn](https://github.com/getagentseal/codeburn) liest laut README vorhandene lokale Sessiondateien von Coding-Werkzeugen, darunter [Claude Code](Claude%20Code.md) und [Codex](Codex.md), und ordnet Tokenverbrauch sowie Kosten nach Werkzeug, Modell, Projekt und Aufgabe. Es sitzt nicht als Proxy vor dem Agenten; MIT-Lizenz und Kontofreiheit sind Projektangaben. [tweet-2052306848221680015](../sources/tweet-2052306848221680015.md)

Der Post dokumentiert `npx codeburn`, `npm install -g codeburn` oder Homebrew. Die gespeicherte README verlangt Node.js 22.13+ und beschreibt zusätzlich Desktop-, Browser-, Menubar- und Tray-Oberflächen. Das Tool wurde hier nicht installiert oder ausgeführt. [tweet-2052306848221680015](../sources/tweet-2052306848221680015.md)

## Diagnose und Agentenanbindung (Stand 2026-05; gespeicherte README)

`codeburn context` zerlegt Sessions in Kontextanteile wie Texte, Reasoning, Toolaufrufe und Toolergebnisse; die Blockgrößen sind Schätzungen aus Zeichenlängen, der Kontext-Gesamtwert stammt laut README aus gemeldeter Usage. `codeburn compare` vergleicht Modelle auf eigenen Sessions, mit Stichproben- und Werkzeuggrenzen. [tweet-2052306848221680015](../sources/tweet-2052306848221680015.md)

Die dokumentierte MCP-Anbindung lautet `claude mcp add codeburn -- npx -y codeburn mcp`. Der lokale Stdio-Server liefert `get_usage` und `get_savings`; Projektnamen werden laut README standardmäßig pseudonymisiert. Das ermöglicht Rückfragen zur eigenen Nutzung, ohne eine allgemeine Sparbehauptung bereits als gemessen zu behandeln; siehe [AI Coding Cost Claims](../concepts/AI%20Coding%20Cost%20Claims.md). [tweet-2052306848221680015](../sources/tweet-2052306848221680015.md)

`codeburn optimize` listet Konfigurations- und Nutzungshinweise. Das optionale `--apply` kann Konfigurationen verändern; die README beschreibt Vorschau, Backups und `codeburn act undo --last`. Vorschläge können modelliert sein und müssen von gemessenen Ergebnissen unterschieden werden. [tweet-2052306848221680015](../sources/tweet-2052306848221680015.md)

## Kosten und Datenschutzgrenzen (Stand 2026-05; gespeicherte README)

Dollarwerte sind API-äquivalente Kosten und bei Abos keine Rechnung. Manche Integrationen liefern gemessene Tokenzahlen, andere Schätzungen; `codeburn audit` soll die Herkunft sichtbar machen. Sessions werden laut README mit den beim Lesen verfügbaren Preisen bewertet, nicht zwingend mit historischen Preisen ihres Ausführungsdatums. [tweet-2052306848221680015](../sources/tweet-2052306848221680015.md)

Der Post nennt 18 Integrationen, gespeicherter Titel und README nennen 37, 40 und 41. Diese unterschiedlichen Erfassungsstände belegen keinen konsistenten aktuellen Bestand. Eine behauptete Einmal-Erfolgsrate beruht auf Edit-/Shell-Heuristiken und ist nicht gleichbedeutend mit fachlich richtiger Arbeit. [tweet-2052306848221680015](../sources/tweet-2052306848221680015.md)

Die CLI verarbeitet Sessions lokal; Preisabfragen, optionale Quotenabfragen und Installationsbefehle können laut README Netzwerkzugriffe auslösen. Desktop-App und Windows-Tray haben außerdem optionale Telemetrie, die unter anderem Werkzeug-, Skill- und Modellnamen sowie aggregierte Mengen enthalten kann. Lokale Verarbeitung darf deshalb nicht pauschal als Netzwerkfreiheit aller Oberflächen beschrieben werden. [tweet-2052306848221680015](../sources/tweet-2052306848221680015.md)
