---
tags: [agents, tools]
sources: [tweet-2104687805876367793.md]
created: 2026-10-06
updated: 2026-10-06
---

# Claude Sonnet 5.5

## Aufgabenprofil (Stand 2026-09)

Der gespeicherte Anthropic-Leitfaden ordnet Sonnet 5.5 klar umrissenen Coding-Aufgaben, wiederholten Agentenaufträgen und Dokument-/Designarbeit zu; [Claude Opus 5.5](Claude%20Opus%205.5.md) wird für schweres, lang laufendes Arbeiten empfohlen. Das sind Herstellerempfehlungen, keine eigenen Vergleichstests. [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)

## Migration von Sonnet 5 (Stand 2026-09)

Der Leitfaden nennt claude-sonnet-5-5 als API-Modellkennung und /claude-api migrate this project to claude-sonnet-5-5 aus [Claude API Skill](Claude%20API%20Skill.md) als Migrationshilfe. Die Anleitung liegt unter https://platform.claude.com/docs/en/models/sonnet-5-5/migration-guide . [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)

- Thinking ist laut Quelle standardmäßig adaptiv; thinking.type disabled wird abgelehnt. between_tools deaktiviert das Denken vor dem ersten Tool-Aufruf, unterstützt nur low/medium/high und keine Zusatzfelder wie budget_tokens. Effort darf damit im Gespräch nicht wechseln. [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)
- Erzwungenes tool_choice any/tool wird laut Quelle abgelehnt; Ersatz ist auto, strict: true, additionalProperties: false in jedem Object-Schema und eine klare Tool-Anweisung. [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)
- Thinking-Blöcke sind an Modell und Gespräch gebunden; der Verlauf soll nur angehängt werden. Sonnet 5.5 könne Sonnet-5-Blöcke lesen, andere Modelle nicht seine neuen Blöcke. [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)
- Auf Claude API und Google Cloud soll Computer Use über computer_toolset_20260801 laufen, mit Anpassungen für Toolset-Ergebnisse und Batch-Aktionen. Amazon Bedrock akzeptiere weiterhin computer_20251124; alte Betaheader können mit Toolsets Konflikte auslösen. [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)
- Advisor-Paarungen mit Opus 4.8, Opus 4.7 und Sonnet 5 werden laut Leitfaden abgelehnt; Opus 5.5, Opus 5 und Sonnet 5.5 seien erlaubt. Advisor-Antworten kommen als verschlüsselter advisor_redacted_result. [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)
- Zwischenstände können als Thinking-Blöcke statt Text kommen. Antworten deshalb nach Blocktyp lesen, nicht content[0].text voraussetzen; für sichtbare Zwischenstände nennt die Quelle display summarized beziehungsweise das Beta-display updates. [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)

## Effort, Checks und Cache (Stand 2026-09)

Die Effort-Stufen seien neu kalibriert: bei gut spezifizierter Agentenarbeit medium testen, bei schwieriger Arbeit high, xhigh/max nur bei gemessenem Gewinn. Thinking zählt gegen max_tokens; für lange Coding-Aufgaben nennt der Artikel 128000 und Streaming. Vergleichsmaßstab sind eigene [Model Selection Evals](../concepts/Model%20Selection%20Evals.md). [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)

Bei niedrigem Effort empfiehlt der Leitfaden ausdrücklich einen echten Test, Build, Typecheck oder den geänderten Befehl vor einer Fertigmeldung; reine Syntaxprüfung oder ein nicht gestarteter Check zählen nicht. Alte Sonnet-5-Workarounds sollen entfernt und die Evals erneut ausgeführt werden. [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)

Die gespeicherte Doku nennt 512 Token als Cacheminimum; top-level Effortwechsel invalidiere den Cache, per-message Effort könne ihn erhalten. Hohe Bildauflösung koste mehr Bildtokens, deshalb bei unnötiger Detailtiefe vorher verkleinern. Siehe [Prompt Caching](../concepts/Prompt%20Caching.md). [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)

## Claude Code und Evidenzgrenze (Stand 2026-09)

Ab [Claude Code](Claude%20Code.md) v2.1.284 soll /model sonnet Sonnet 5.5 mit medium wählen; Thinking lasse sich dort nicht abschalten und ein Fast Mode sei nicht vorhanden. Modellkennung, Parameter und Verfügbarkeit sind der gespeicherte Herstellerstand; die Migration wurde hier nicht ausgeführt. Das 39,5-Sekunden-Video hat kein auswertbares gespeichertes Transkript. [tweet-2104687805876367793](../sources/tweet-2104687805876367793.md)
