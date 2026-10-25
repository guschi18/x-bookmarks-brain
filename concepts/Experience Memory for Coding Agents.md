---
tags: [research, agents]
sources: [tweet-2113990583241125942.md]
created: 2026-10-25
updated: 2026-10-25
---

# Experience Memory for Coding Agents

## Definition (Stand 2026-10)

Erfahrungsspeicher hält die Verläufe früherer Agentenläufe (Trajektorien) fest, damit der nächste Lauf sie nutzen kann. Das Paper "REM: What to Store, When to Recall, What to Forget in Experience Memory for Coding Agents" (NeurIPS 2026 CLEA Workshop, arXiv 2610.27377 vom 2026-10-19) behauptet, der Engpass sei nicht die Suche, sondern wie Erfahrung gespeichert und über ihren Lebenszyklus gesteuert wird. [tweet-2113990583241125942](../sources/tweet-2113990583241125942.md)

## Drei Entscheidungen (Stand 2026-10)

- Speichern: Jeder Lauf wird zu einem in Phasen gegliederten Dokument von etwa 270 Tokens verdichtet (Fehler finden, verstehen, beheben, prüfen), rund hundertmal kleiner als das Log. Das Dokument als rohes Log oder freie Zusammenfassung einzuspielen, steigerte die Lösungsquote nicht, selbst bei richtig gewähltem Lauf. [tweet-2113990583241125942](../sources/tweet-2113990583241125942.md)
- Abrufen: Die Kurzfassung kommt zu Aufgabenbeginn; die umfangreichere Änderungsaufzeichnung erscheint erst, wenn der Agent zum ersten Mal einen Check nicht besteht (eigene Tests des Agenten zählen nicht). Von Anfang an gezeigt lag die Quote bei 25,3 % gegenüber 27,6 % bei REM, bei 423K statt 374K Tokens je Aufgabe. [tweet-2113990583241125942](../sources/tweet-2113990583241125942.md)
- Vergessen: Die Aufzeichnung wird nach einmaliger Ansicht aus dem Arbeitsgedächtnis entfernt. [tweet-2113990583241125942](../sources/tweet-2113990583241125942.md)

## Befunde (Stand 2026-10)

- Benchmark SWE-ContextBench Lite (99 Fehlerbehebungen, Pool von 300 gelösten Läufen), Standardmodell Claude Sonnet 4.5, Strands-Agent mit sechs Werkzeugen in Docker, höchstens 100 Runden. [tweet-2113990583241125942](../sources/tweet-2113990583241125942.md)
- Lösungsquote 27,6 % gegenüber 24,9 % ohne Gedächtnis, in allen drei Wiederholungen höher (27/29/26 gegenüber 23/26/25 Aufgaben), bei 17 % geringeren Kosten. Die Auswahl des verwandten Laufs trifft laut Abstract zu 68,7 % gegenüber 55,6 % (match@1) besser als bisherige Systeme. [tweet-2113990583241125942](../sources/tweet-2113990583241125942.md)
- Schwächere und mittlere Modelle (bis 31,3 % ohne Gedächtnis) verloren nie und gewannen bis etwa 4 Punkte; die zwei stärksten (über 47 %) verloren in jeder Einstellung, etwa Opus 4.8 von 47,5 % auf 39,4 %. Folgerung des Posts: Gedächtnis je Modell messen und abschalten, wo es schadet. [tweet-2113990583241125942](../sources/tweet-2113990583241125942.md)

## Grenzen (Stand 2026-10)

Quelle ist ein Posting über ein Paper; Ergebnisse stammen von den Autoren, ein einzelner Benchmark mit 99 Aufgaben und drei Wiederholungen, nicht unabhängig repliziert. Die Aussagen betreffen Fehlerbehebung in Repositories. [tweet-2113990583241125942](../sources/tweet-2113990583241125942.md)

## Verwandte Seiten

[Context Engineering](Context%20Engineering.md) behandelt Kontext als knappe Ressource; [Agent History Reflection](Agent%20History%20Reflection.md) wertet Agentenverläufe dagegen für die menschliche Selbstreflexion aus. [tweet-2113990583241125942](../sources/tweet-2113990583241125942.md)
