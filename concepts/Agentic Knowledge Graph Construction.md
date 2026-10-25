---
tags: [agents, research]
sources: [tweet-2079234800766816633.md, tweet-2095111361181405259.md, tweet-2088682533278077382.md, tweet-2111838109029552334.md]
created: 2026-10-02
updated: 2026-10-23
---

# Agentic Knowledge Graph Construction

## Definition (Stand 2026-07)

Ein Wissensgraph speichert Datensätze als Knoten und Beziehungen als eigene, gerichtete und typisierte Datensätze mit Eigenschaften, statt sie über Join-Tabellen herzustellen. Abfragen werden in Cypher als Muster formuliert, etwa für Empfehlungen über gemeinsame Käufe und ein negatives Muster für noch nicht gekaufte Produkte. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

Gegenüber reinem RAG werden Text-Chunks zusätzlich mit extrahierten Entitäten verbunden und zusammen mit ihnen abgerufen; Vektorsuche und Musterabfrage lassen sich kombinieren. Der Kurs begründet den Nutzen mit Genauigkeit in Anwendungen mit hohem Einsatz, ohne Vergleichsmessung. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

## Zielmodell (Stand 2026-07)

Das Kursbeispiel ist eine Ursachenanalyse von Kundenbeschwerden bei einem Möbelhersteller. Strukturierte Stücklisten aus CSV-Dateien werden zum Domain Graph, gechunkte Markdown-Reviews zum Lexical Graph; ein Subject Graph aus extrahierten Subjekt-Prädikat-Objekt-Fakten verbindet beide, wenn etwa ein erwähnter Tisch einem Produkt im Domain Graph entspricht. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

## Agentenablauf (Stand 2026-07)

- Ein User-Intent-Agent klärt im Gespräch Ziel und Art des Graphen. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)
- Ein File-Suggestion-Agent schlägt passende Dateien vor, die der Nutzer bestätigt. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)
- Für strukturierte Daten erzeugt ein Vorschlag-Kritiker-Paar iterativ einen Graph Construction Plan, also eine Bauanleitung statt des Graphen selbst. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)
- Für Text beschreiben spezialisierte Agenten, welche Entitäts- und Faktentypen extrahierbar sind (Knowledge Extraction Plan), ohne schon zu extrahieren. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)
- Ein Werkzeug führt beide Pläne aus: Domain Graph bauen, Markdown chunken und einbetten, Entitäten und Fakten extrahieren und mit den strukturierten Daten verbinden. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

## Umsetzung mit Google ADK (Stand 2026-07)

Der Kurs nutzt [Google ADK](../entities/Google%20ADK.md) mit LiteLLM als Brücke zu einem OpenAI-Modell und einen Neo4j-Wrapper, der Ergebnisse als Status-Dictionary zurückgibt. Tools sind Python-Funktionen, deren Docstring dem Modell die Funktion beschreibt; Cypher-Werte werden als Query-Parameter statt per String-Verkettung übergeben, um Injection zu vermeiden. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

Ein Root-Agent delegiert an Sub-Agenten; ein Agent kann auch als Tool eines anderen Agenten aufgerufen werden. Session-State ist ein Dictionary, das Tools über den Tool-Kontext oder Agenten über einen Output-Key schreiben; im Beispiel merkt sich ein Begrüßungstool den Nutzernamen für den Verabschiedungsagenten. [Google Agents CLI](../entities/Google%20Agents%20CLI.md) behandelt ebenfalls ADK-Agenten. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

## Grenzen (Stand 2026-07)

Das gespeicherte Transkript umfasst Einführung, Grundlagen, Architektur, die ADK-Lektion und den Abschluss; die angekündigten Lektionen zu Schema-Vorschlag, Extraktion und Graphbau fehlen darin. Das im Post genannte Kapitel „Why Graphs are the future of agentic AI“ ist im Transkript nicht auffindbar. Der Kurs ist eine Partnerschaft mit dem Datenbankanbieter Neo4j. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

Die Kurs-Wissensgraphen sind von [Agent Workflow Graphs](Agent%20Workflow%20Graphs.md) zu unterscheiden, wo der Graph den Ablauf von Agentenaufrufen beschreibt, nicht die Daten. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

## Bitemporale Produktumsetzung (Stand 2026-09)

[Utopia](../entities/Utopia.md) dokumentiert eine andere Umsetzung als das Kursbeispiel: Ein editierbares Ontologiemodell steuert Extraktion, Fakten halten Gültigkeitszeit und Erfassungszeit getrennt, und Korrekturen schließen alte Versionen, statt sie zu überschreiben. Provenienz, rücknehmbare Entity-Merges und ein Review für unsichere Fakten verbinden Graphbau mit laufender Wissenspflege. Die README beschreibt ein Produkt im Stand v0.1, keine unabhängig geprüfte Zuverlässigkeit. [tweet-2095111361181405259](../sources/tweet-2095111361181405259.md)

## GraphRAG-Verfahren und fünf Vorlagen (Stand 2026-08)

Der Artikel beschreibt Ingest, Extraktion, Entity Resolution, Speicherung, kombinierte Retrieval-Wege, Agentensteuerung, Verifikation und laufende Pflege. Er verlangt Schema-Treue, Belegtexte und zeitlich markierte Änderungen statt stiller Überschreibung. Die Kimi-K3-Modellpräferenz und behaupteten Leistungsgewinne sind Empfehlungen des Autors ohne eigenen Vergleichslauf. [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

Die folgenden vollständigen englischen Vorlagen stammen aus dem gespeicherten Artikel und bleiben modellunabhängig nutzbar; Platzhalter werden mit eigenen Daten gefüllt. [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

### 1. Extraktion

```text
Extract all organizations, people, products, and events
from the text below.
For each entity return:
- canonical_name
- type
- description
- source_location
For each relationship return:
- source_entity
- relation_type
- target_entity
- evidence (exact quote from source)
- confidence_score (0-1)
Rules:
- Only extract relationships explicitly stated or
  directly implied by the text
- Do not infer relationships from general knowledge
- If a relationship is uncertain, lower the confidence
  score rather than omitting it
- Return valid JSON only
Text:
[paste your document]
```

Quelle: [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

### 2. Entity Resolution

```text
Compare the following entities and determine whether
they refer to:
- the same entity
- related but distinct entities
- unrelated entities
Entities:
[list your candidates]
For each pair, return:
- verdict (same / related / unrelated)
- canonical_name if same
- reasoning
- confidence
Rules:
- Do not merge entities without clear evidence
- Similar names are not sufficient evidence
- When uncertain, mark as "related" rather than "same"
- Flag any case where merging would be destructive
```

Quelle: [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

### 3. Cypher-Abfrage

```text
Translate the user question into a Cypher query
for our graph.
Schema:
[paste your node labels, relationship types,
and properties]
User question:
[the actual question]
Rules:
- Use only labels and relationship types present
  in the schema
- Do not invent properties
- Prefer path queries over single-node lookups when
  the question implies causation or connection
- Return the query, then a plain-English explanation
  of what it retrieves and why
```

Quelle: [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

### 4. Belegte Antwort

```text
Answer the question using only the graph paths provided
below.
Retrieved paths:
[paste subgraph]
Question:
[the question]
For every claim in your answer:
- cite the specific nodes and relationship path
  that support it
- state your confidence
- flag any step where you're inferring rather than
  reading directly from the graph
Rules:
- Do not use knowledge outside the provided paths
- Do not infer causation from co-occurrence
- If the graph doesn't contain enough to answer,
  say exactly what's missing
```

Quelle: [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

### 5. Graphpflege

```text
Compare these new facts against the existing graph.
New facts:
[extracted triples]
Existing related subgraph:
[current state]
Classify each new fact as:
- new (add it)
- duplicate (skip)
- contradiction (flag for review, do not overwrite)
- update (supersedes an existing fact — timestamp
  the old one, don't delete it)
- uncertain (needs human review)
For contradictions, show both versions and the
evidence for each.
Never silently overwrite an existing fact.
```

Quelle: [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

### Grenzen und Verifikation

Die Extraktionsvorlage lässt direkt implizierte Beziehungen zu und empfiehlt bei Unsicherheit niedrigere Konfidenz. Vor automatischer Übernahme sind solche Beziehungen zu prüfen; Konfidenzwerte ersetzen keine Belege. Graphpfade belegen zudem keine Kausalität allein durch Nachbarschaft. Generated Cypher wird vor Ausführung gegen das tatsächliche Schema geprüft, und Retrieval-Tiefe sowie Kosten werden an eigenen Testfragen gemessen. [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

Das begleitende Video behandelt Ablaufgraphen unter [Agent Workflow Graphs](Agent%20Workflow%20Graphs.md); Wissensgraph- und Workflow-Graph-Behauptungen werden nicht gleichgesetzt. [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

## Lokaler Projektgraph als eigener Werkzeugpfad (Stand 2026-10)

[Graphify](../entities/Graphify.md) ergänzt den dokumentierten Daten-/GraphRAG-Aufbau um eine Dateiordner-Perspektive: Code wird laut gespeichertem Anbieterprofil lokal mit tree-sitter extrahiert; Dokumente und Medien erhalten eine modellgestützte Verarbeitung. Dieser Werkzeugpfad ist weder dieselbe Implementierung noch ein unabhängiger Leistungsbeleg für die bestehenden GraphRAG-Beispiele. [tweet-2111838109029552334](../sources/tweet-2111838109029552334.md)
