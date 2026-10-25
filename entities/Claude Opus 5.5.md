---
tags: [agents, tools]
sources: [tweet-2103552376380457454.md, tweet-2102436540488315361.md, tweet-2103378606986863103.md, tweet-2102481940742115352.md, tweet-2102491840612380934.md]
created: 2026-10-03
updated: 2026-10-08
---

# Claude Opus 5.5

## Überblick

Anthropic stellt Opus 5.5 als erstes Modell der Claude-5.5-Familie vor; es arbeite für die meisten Aufgaben auf dem Niveau von [Fable](Fable.md) 5.1 und koste je Aufgabe etwa 40 Prozent weniger als Opus 5 (Herstellerangabe; Workload-Schätzung, je Token sind es 20 Prozent). [tweet-2102436540488315361](../sources/tweet-2102436540488315361.md)

## Preise und Kosten

Der Kostenartikel nennt API-Listenpreise von 4 Dollar je Million Input, 20 Dollar je Million Output und 0,20 Dollar je Million Cache-Reads; Input und Output sind 20 Prozent, Cache-Reads 60 Prozent günstiger als bei Opus 5. [tweet-2103552376380457454](../sources/tweet-2103552376380457454.md) Die 40 Prozent sind laut Artikel eine Workload-Schätzung bei Default-Einstellungen, die weniger Token je Aufgabe annimmt. [tweet-2103552376380457454](../sources/tweet-2103552376380457454.md) Ein Output-Token kostet 100 Cache-Reads; Thinking wird als Output abgerechnet, daher bewegt Effort die Rechnung stark. [tweet-2103552376380457454](../sources/tweet-2103552376380457454.md) Im Beispiel kosten 2,8M Input-Token ohne Cache 11,20 Dollar, bei 90 Prozent Trefferrate 1,62 Dollar; weniger Turns senken die Kosten, weil jeder Turn die ganze Unterhaltung erneut sendet. Siehe [Prompt Caching](../concepts/Prompt%20Caching.md) und [AI Coding Cost Claims](../concepts/AI%20Coding%20Cost%20Claims.md). [tweet-2103552376380457454](../sources/tweet-2103552376380457454.md)

## Effort

Bei gleicher Stufe denkt Opus 5.5 mehr als Opus 5, besonders bei xhigh und max; empfohlen wird, bei medium zu starten. Details zur Leiter bei [Model Selection Evals](../concepts/Model%20Selection%20Evals.md). [tweet-2103552376380457454](../sources/tweet-2103552376380457454.md)

## Berichtete Einsätze

- Refactoring-Analyse eines ganzen Repos mit parallelen read-only Agenten: [Fan-Out Refactor Review](../concepts/Fan-Out%20Refactor%20Review.md). [tweet-2103378606986863103](../sources/tweet-2103378606986863103.md)
- Projektverbesserung aus der lokalen Sitzungshistorie: [Session History Review](../concepts/Session%20History%20Review.md). [tweet-2102481940742115352](../sources/tweet-2102481940742115352.md)
- Ein strukturierter Build-Prompt mit Abschnitten von discovery über security_and_data und verification bis refactor_loop; die Behauptung, er erzeuge die beste Codebase, ist unbelegt. [tweet-2102436540488315361](../sources/tweet-2102436540488315361.md)

Verwandt: [Claude Code](Claude%20Code.md). [tweet-2103552376380457454](../sources/tweet-2103552376380457454.md)

## Ergänzungen (Stand 2026-09)

Der gespeicherte Hersteller-Playbook empfiehlt ganze Aufgaben mit Done- und Check-in-Kriterien, Nachsteuern laufender Aufgaben, persistente Aufgabenlisten und überprüfte Subagenten-Ergebnisse. Resultatkontrolle soll Diff-Review und explizit unbestätigte Recherchepunkte umfassen. [tweet-2102491840612380934](../sources/tweet-2102491840612380934.md)

Der Artikel berichtet, das Modell denke vor jeder Antwort; zusätzliche „think carefully“-Zeilen hätten in Herstellerprüfungen Latenz erhöht, ohne klaren Qualitätsgewinn. Bildverständnis, längere autonome Läufe und bessere Artefakte sind Herstellerangaben ohne hier gespeicherte Vergleichsdaten. [tweet-2102491840612380934](../sources/tweet-2102491840612380934.md)
