---
tags: [llm-training, research]
sources: [tweet-2072285732526264474.md, tweet-2097369738968195513.md, tweet-2103552376380457454.md, tweet-2104679128020754457.md, tweet-2104676099083190435.md]
created: 2026-09-29
updated: 2026-10-08
---

# Model Selection Evals

## Entscheidung anhand eigener Aufgaben

Der gespeicherte Vortrag empfiehlt, Modelle auf repräsentativen Aufgaben nach Ergebnisqualität, Latenz und Kosten pro erfolgreichem Ergebnis zu vergleichen. Ein Eval-Fall soll Eingabe, Erfolgskriterien, Endergebnis und nötige Zwischenschritte abdecken; wiederholte Läufe helfen, Rauschen von stabilen Unterschieden zu trennen. [tweet-2072285732526264474](../sources/tweet-2072285732526264474.md)

## Diagnose und Stellschrauben

Der Sprecher unterscheidet Modellfehler von API- und Werkzeugfehlern, warnt vor gesättigten Tests und rät zum Lesen vollständiger Traces. Als Stellschrauben nennt er Modellwahl, Thinking/Effort, Prompt-Caching und knappe Werkzeugantworten; die im Vortrag genannten Einsparungen sind berichtete interne Beispiele. [tweet-2072285732526264474](../sources/tweet-2072285732526264474.md)

## Widerspruch im Quellenpaket

Der zusätzlich gespeicherte X-Artikel (Stand 2026-07) empfahl Sonnet 5 als Standard und Opus 4.8 für schwierige Fälle. Diese Modellempfehlung, die genannten Preise und die Einführungsfrist sind überholt: Seit Opus 5.5 und Sonnet 5.5 gelten die Empfehlungen weiter unten ([tweet-2103552376380457454](../sources/tweet-2103552376380457454.md), [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)). Das Vortragsvideo liefert für Modellwahl keine Prüfung und betont stattdessen eigene Evals je Aufgabenprofil. [tweet-2072285732526264474](../sources/tweet-2072285732526264474.md)

## Effort als Stellschraube (Stand 2026-09)

Der Anthropic-Kostenartikel berichtet: [Fable](../entities/Fable.md) 5 erreicht auf FrontierCode Diamond (die schwersten 50 Aufgaben) bei niedrigem Effort 11,5 Prozent für 5,35 Dollar pro Aufgabe und bei maximalem 30,9 Prozent für 19,00 Dollar, also etwa das 2,7-Fache der Leistung für das 3,5-Fache der Kosten. Fable 5.1 erreicht bei Humanity's Last Exam ohne Tools etwa 53 Prozent für etwa 0,30 Dollar pro Frage bei niedrigem und etwa 61 Prozent für etwa 2,23 Dollar bei maximalem Effort; der letzte Schritt bringt etwa 0,5 Punkte für 46 Prozent Mehrkosten und liegt im Laufrauschen. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

Fehlkalibrierung geht in beide Richtungen: Zu hoher Effort führt zu Übergrübeln, zu niedriger zu Antworten aus unvollständiger Evidenz. Als Hebel nennt der Artikel, ein stärkeres Modell mit niedrigem Effort zu testen (auf CursorBench 3.2 erreiche Fable 5.1 niedrig die Leistung von Fable 5 hoch bei einem Drittel der Kosten; Cache-Reads kosten 0,25 statt 1,00 Dollar je Million Token) und eine Effort-Stufen-Messung für die eigene Aufgabe zu fahren; eine flache Kurve auf einer nicht gesättigten Evaluation bedeute, dass mehr Effort nichts bringt. Alle Zahlen sind Herstellerangaben. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

Werkzeug dafür: `/claude-api hillclimb` aus [Claude API Skill](../entities/Claude%20API%20Skill.md). [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

## Effort-Leiter für Opus 5.5 (Stand 2026-09)

Ein Post empfiehlt für [Claude Opus 5.5](../entities/Claude%20Opus%205.5.md) die Leiter low für mechanische Edits, medium für klar umrissene Alltagsarbeit, high wenn medium stockt und xhigh/max nur bei gemessenem Gewinn; eine für Opus 5 gewählte Stufe solle nicht übernommen werden, weil Opus 5.5 bei gleicher Stufe mehr denkt. [tweet-2103552376380457454](../sources/tweet-2103552376380457454.md)

## Coordinator und Threads getrennt einstellen (Stand 2026-09)

[Claude Projects](../entities/Claude%20Projects.md) beschreibt getrennte Modell- und Effortwahl für Coordinator und Workerthreads. Post und Bild empfehlen Opus 5.5 / Sonnet 5.5; der Artikel nennt zusätzlich Opus in beiden Rollen mit medium sowie Sonnet 5 für einfachere Projekte. Die Kombinationen sind Autorenpraxis ohne vergleichende Messung; Usage je Rolle ist der vorgeschlagene Kontrollpunkt. [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)

## Eval-Qualität und Overfitting (Stand 2026-09)

Der Eval-Design-Artikel nennt vier Prüfpunkte: Aufgaben spiegeln die Zielpraxis, stärkere Modelle beziehungsweise mehr Denken sollten sinnvolle Verbesserungen zeigen, es gibt lösbare Restaufgaben statt einer gesättigten Messung und die Varianz bleibt niedrig. Unlösbare oder mehrdeutige Aufgaben und Graderwidersprüche sollen von Modellfehlern getrennt werden. [tweet-2104676099083190435](../sources/tweet-2104676099083190435.md)

Harte Fälle sollen begründbar schwierig sein; nur die Fehlfälle eines einzelnen Modells zu sammeln kann dessen spezifisches Fehlerprofil messen. Produktionsverkehr kann umgekehrt zu leicht sein, wenn Nutzer nur erwartbar lösbare Aufgaben stellen. [tweet-2104676099083190435](../sources/tweet-2104676099083190435.md)

Der Workflow prüft denselben Grader zweimal auf identischem Output, API-/Timeout-/Trunkierungsfehler und zurückgelassenen Umgebungszustand. Erst wenn Laufrauschen kleiner als ein handlungsrelevanter Gewinn ist, lohnt Optimierung; ansonsten sind mehr Fälle oder Wiederholungen vorgeschlagen. [tweet-2104676099083190435](../sources/tweet-2104676099083190435.md)

Train-Fälle und gehaltene Testfälle werden getrennt, Antworten außerhalb des Modellzugriffs gehalten und Fehltranscripts nicht in den Prompt kopiert. Der Artikel warnt auch vor Harness-Erweiterungen, die nur für Eval-Sonderfälle nützen. [Claude API Skill](../entities/Claude%20API%20Skill.md) setzt diese Vorgaben als geführten Ablauf um; die Herstellerbeispiele sind keine eigene Replikation. [tweet-2104676099083190435](../sources/tweet-2104676099083190435.md)
