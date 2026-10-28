---
tags: [agents, product-building]
sources: [tweet-2114420226725204453.md]
created: 2026-10-27
updated: 2026-10-27
---

# Subagent Consolidation

## Idee (Stand 2026-10)

Av1dlive zitiert einen Tweet, nach dem ein Agent mit Skills Multi-Agent-Aufbauten oft bei Qualität, Kosten und Tempo schlage. Genannt werden etwa doppelt so schnelle Läufe bei einem Kunden, ein über 80 % kleinerer Claude-Code-System-Prompt bei neueren Modellen und Werkzeugwahl, die jenseits von 30 bis 50 Tools bricht. Die Zahlen stammen aus dem zitierten Tweet und werden dort Anthropic-Tests zugeschrieben; eine Primärquelle ist nicht gespeichert. [tweet-2114420226725204453](../sources/tweet-2114420226725204453.md)

## Audit-Prompt in fünf Schritten

1. MAP: Subagenten mit Prompt, Tools und Aufrufzeitpunkt auflisten; Ketten, gemeinsame Daten und gemeinsame Läufe markieren. [tweet-2114420226725204453](../sources/tweet-2114420226725204453.md)
2. SKILLS: Subagenten-Anweisungen in Skills mit Einzeiler-Beschreibung umwandeln, volle Schritte erst bei Bedarf laden. [tweet-2114420226725204453](../sources/tweet-2114420226725204453.md)
3. TOOLS: API-Aufrufe nach Nutzerziel bündeln, insgesamt unter 30. [tweet-2114420226725204453](../sources/tweet-2114420226725204453.md)
4. TESTS: vor Änderungen zehn Testaufgaben für jede Agentenkette und jede Pflichtregel schreiben. [tweet-2114420226725204453](../sources/tweet-2114420226725204453.md)
5. FOLD: einzeln einfalten, jede Aufgabe zweimal laufen lassen; Subagent behalten, wenn die gefaltete Version schlechter abschneidet, frischen Kontext für Parallelarbeit braucht oder den Hauptkontext aufbläht. Plan zuerst zeigen, vor Änderungen auf Freigabe warten. [tweet-2114420226725204453](../sources/tweet-2114420226725204453.md)

## Sechs AGENTS.md-Regeln (Stand 2026-10)

Das Bild des Folgetweets nennt: vor Code für unwahrscheinliche Randfälle Nutzen, Wahrscheinlichkeit und Zeilenzahl nennen; Außendaten einmal am Eingang validieren; einmalige Logik inline, try/catch nur bei echtem behandelbarem Fehler; Funktionen ganz lassen, außer Aufteilung dient Wiederverwendung oder Lesbarkeit; überflüssige UI-Labels streichen und stattdessen das Layout reparieren; nur liefern, was Nutzern, Entwicklern und Agenten nützt und nichts bricht. [tweet-2114420226725204453](../sources/tweet-2114420226725204453.md)

## Grenzen

Av1dlives 50-%-Ersparnis ist eine ungemessene Einzelbehauptung (siehe [AI Coding Cost Claims](AI%20Coding%20Cost%20Claims.md)). Der Prompt belegt nicht, dass Falten immer besser ist; er nennt selbst Ausnahmen. Verwandt: [Agentic Engineering](Agentic%20Engineering.md), [Claude Skills Guide](Claude%20Skills%20Guide.md). [tweet-2114420226725204453](../sources/tweet-2114420226725204453.md)
