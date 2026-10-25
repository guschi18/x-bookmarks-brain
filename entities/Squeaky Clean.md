---
tags: [agents, tools]
sources: [tweet-2079569829120377139.md]
created: 2026-10-02
updated: 2026-10-02
---

# Squeaky Clean

## Überblick (Stand 2026-07)

Squeaky Clean ist laut Projektseite ein meinungsstarkes, halbdeterministisches Open-Source-Werkzeug: Aus einer deklarativen ProblemSpec soll eine baubare, testbare Anwendung nach Clean Architecture, SOLID sowie GoF- und DDD-Mustern entstehen. Robert C. Martin verlinkte es, ohne es selbst ausprobiert zu haben. [tweet-2079569829120377139](../sources/tweet-2079569829120377139.md)

## Mechanismus laut Projekt (Stand 2026-07)

- Architekten-Agenten erzeugen einen Mehrmodulplan in der DSL Squib, einer eingefrorenen, maschinenprüfbaren Grammatik mit etwa 200 Zeichen pro Klasse; je Datei arbeitet ein musterspezialisierter atomarer Agent auf kleinen Modellen. [tweet-2079569829120377139](../sources/tweet-2079569829120377139.md)
- Ein Validator erzwingt die Dependency Rule: Domain importiert nichts, Application nur Domain, Infrastructure implementiert Domain-Ports. [tweet-2079569829120377139](../sources/tweet-2079569829120377139.md)
- Der Musterkatalog umfasst 34 GoF- und DDD-Muster in vier Kategorien; eine Contract Registry prüft Feldformen zwischen Produzent und Konsument etwa eines Kafka-Topics. [tweet-2079569829120377139](../sources/tweet-2079569829120377139.md)
- Agentic Architecture Recovery arbeitet rückwärts in fünf Phasen: Recover, Analyze, Triage, Refactor, Regenerate; Python wird per AST, Java, JavaScript und TypeScript per Regex eingelesen. [tweet-2079569829120377139](../sources/tweet-2079569829120377139.md)

## Installation (Stand 2026-07)

Installation laut Projektseite: pip install git+https://github.com/garciaalan186/squeaky-clean.git und ein gesetzter ANTHROPIC_API_KEY; die Roadmap liegt unter https://github.com/garciaalan186/squeaky-clean/blob/main/docs/roadmap.md. [tweet-2079569829120377139](../sources/tweet-2079569829120377139.md)

## Grenzen (Stand 2026-07)

Niedrigere Kosten, weniger Halluzinationen und Energieersparnis durch kleine Kontexte sind Projektbehauptungen; die Seite nennt ein Meta-Evaluationsframework, aber keine gespeicherten Messwerte. Das Werkzeug wurde hier nicht installiert oder getestet. [tweet-2079569829120377139](../sources/tweet-2079569829120377139.md)

Verwandt: [Agentic Engineering](../concepts/Agentic%20Engineering.md) für Martins Prüfgauntlet, [Agent Workflow Graphs](../concepts/Agent%20Workflow%20Graphs.md) für Fan-out auf günstigere Modelle. [tweet-2079569829120377139](../sources/tweet-2079569829120377139.md)
