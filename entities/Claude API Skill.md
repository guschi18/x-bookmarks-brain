---
tags: [agents, tools, llm-training]
sources: [tweet-2097369738968195513.md, tweet-2096668098422272007.md, tweet-2104676099083190435.md]
created: 2026-10-03
updated: 2026-10-08
---

# Claude API Skill

## Überblick

Die claude-api-Skill liegt im Repository anthropics/skills und ist laut Artikel auch in Claude Code eingebaut. Ihre Befehle richten sich auf Kosten und Leistung von Anwendungen auf der Claude Platform. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

## Befehle

- `/claude-api prompt-audit`: prüft Prompts, Skills, Tool-Beschreibungen und Konfiguration im Arbeitsverzeichnis, einschließlich Anwendungscode mit Claude-API-Aufrufen und CLAUDE.md, auf Anti-Muster für neue Modelle. Eine Nutzerin setzt ihn beim Upgrade auf [Fable](Fable.md) 5.1 ein; er schlage einen Diff vor und funktioniere auch ohne API-Nutzung. Siehe [Instruction Debt Audit](../concepts/Instruction%20Debt%20Audit.md). [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md) [tweet-2096668098422272007](../sources/tweet-2096668098422272007.md)
- `/claude-api cost-optimize`: ermittelt, wohin Tokens fließen (Usage-Reports mit Admin-API-Schlüssel, Usage-Objekte der Antworten oder Schätzung aus dem Code), und reiht Einsparungen: Prompt-Caching, schlankere Requests samt prompt-audit, begrenzte Ausgabe und Batching unbeaufsichtigter Arbeit. Mit einer Evaluation berechnet er Kosten und Leistung über Effort-Stufen und Modelle. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)
- `/claude-api hillclimb`: teilt eine Evaluation in Train- und Testmenge, schlägt Konfigurationsänderungen vor und liest fehlgeschlagene Train-Fälle, um sie zu beheben. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

## Berichtete Ergebnisse (Anthropic, nicht unabhängig geprüft)

- cost-optimize (Stand 2026-09-08) mit Sonnet 5 als Basis auf vier öffentlichen Benchmarks: LegalBench etwa 58 Prozent weniger Kosten (Thinking-Tokens 102.779 auf 8.284, Pass-Rate im Rauschen), tau2-bench retail etwa 73 Prozent (der Fließtext nennt 72 Prozent), OfficeQA Pro etwa 52 Prozent (136,20 auf 64,87 Dollar), SWE-bench Verified etwa 55 Prozent durch Effort medium und knappe Ausgabe (Median 29 auf 17 Schritte, Prompt-Tokens 75,2 Mio. auf 33,7 Mio.). [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)
- hillclimb (Stand 2026-09-08) auf einem Kundensupport-Benchmark: Opus 5 mit niedrigem Effort und prompt-audit erreichte 98,9 Prozent Train-Genauigkeit bei 2,6 Cent pro Ticket; Sonnet 5 niedrig fiel auf 88,9 Prozent bei 1 Cent und kehrte nach ergänzten Routing- und Erstattungsgrenzen-Regeln auf 98,9 Prozent zurück. Auf 14 zurückgehaltenen Tickets: 90,5 gegen 78,6 Prozent beim Ausgangssetup bei rund einem Fünftel der Kosten. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

## Grenzen

Die Zahlen stammen vom Hersteller, aus wenigen Benchmarks und teils sehr kleinen Testmengen (14 Tickets). Wie sich die Befehle auf eigene Setups auswirken, ist offen. Siehe [Prompt Caching](../concepts/Prompt%20Caching.md), [Model Selection Evals](../concepts/Model%20Selection%20Evals.md) und [Claude Code](Claude%20Code.md). [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

## Eval-Aufbau und kontrollierte Optimierung (Stand 2026-09)

Der zusätzliche Herstellerartikel nennt nach claude update die Befehle /claude-api build-eval und /claude-api hillclimb; der Skill liegt unter https://github.com/anthropics/skills/tree/main/skills/claude-api. build-eval lässt Eingaben und Grader vom Nutzer bestätigen, erzeugt Fälle, Runner, JSONL-Ergebnisse und vollständige Transcripts sowie eine lokale Ergebnisansicht. [tweet-2104676099083190435](../sources/tweet-2104676099083190435.md)

Als Eingaben priorisiert der beschriebene Workflow Produktionstraces, Bugreports, fünf bis zehn handgeschriebene Fälle und danach synthetische Codebase-Fälle. Für feste Ausgaben nutzt er programmatische Checks, für offene Ausgaben einen getrennten Judge mit prüfbaren Kriterien; Paarvergleiche sollen anonymisiert und zufällig angeordnet sein. [tweet-2104676099083190435](../sources/tweet-2104676099083190435.md)

Beim Hillclimbing werden erlaubte Änderungsflächen und Ziel festgelegt, Fälle auf Train/Test verteilt und pro Runde ein Patch geprüft. Regressionen und Train-Gewinne ohne Test-Gewinn führen laut Anleitung zur Rücknahme; nach zwei bis drei stagnierenden Runden werden Fehler nach Ursachen gruppiert. Gewinne innerhalb des Laufrauschens rechtfertigen laut Artikel keinen Merge. Die Eval-Kriterien stehen auf [Model Selection Evals](../concepts/Model%20Selection%20Evals.md). [tweet-2104676099083190435](../sources/tweet-2104676099083190435.md)
