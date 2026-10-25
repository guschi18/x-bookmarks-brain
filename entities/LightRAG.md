---
tags: [tools, research]
sources: [tweet-2037907310136484036.md]
created: 2026-10-22
updated: 2026-10-22
---

# LightRAG

## Überblick

[LightRAG](https://github.com/HKUDS/LightRAG) (HKUDS) ist ein Open-Source-Framework für Retrieval-Augmented Generation. Die README führt den Titel "LightRAG: Simple and Fast Retrieval-Augmented Generation" mit dem Zusatz EMNLP2025. Der Post vom 28.03.2026 nennt es als Repository für Claude-Code-Projekte; ein Claude-Code-spezifischer Einsatz ist in der README nicht belegt. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)

## Funktionen laut README (Stand der gespeicherten Seite, jüngster Eintrag 2026-07)

- Speicher-Backends: PostgreSQL und MongoDB als Komplettlösung, später OpenSearch als einheitliches Backend für alle vier Speicherarten. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
- Abfrage: Reranker-Unterstützung, laut README als Standard für gemischte Abfragen; Quellenangaben (Citations) und Rückgabe der abgerufenen Kontexte; Auswertung mit RAGAS und Tracing mit Langfuse. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
- Dokumentpflege: Dokumente löschen mit automatischer Neuerzeugung des Wissensgraphen. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
- Indexierung: vier wählbare Chunking-Strategien (Fix, Recursive, Vector, Paragraph); rollenspezifische LLM-Konfiguration für EXTRACT, QUERY, KEYWORDS und VLM; Multimodalität über RAG-Anything (MinerU/Docling); Erkennung von Überschriften in Word-Dokumenten. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
- Betrieb: ein Setup-Assistent für lokale Bereitstellung von Embedding, Reranking und Speicher per Docker. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)

## Grenzen

Alle Angaben stammen aus der README des Herstellerteams; Leistung, Qualität und Aufwand wurden nicht geprüft. Die README listet Funktionen mit Datum, aber keine Vergleichsmessung. Ein Bezug zu [Agentic Knowledge Graph Construction](../concepts/Agentic%20Knowledge%20Graph%20Construction.md) besteht über den Graph-Ansatz, ist in der Quelle aber nicht ausgeführt. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
