---
tags: [agents, tools]
sources: [tweet-2100980633677746295.md]
created: 2026-10-06
updated: 2026-10-06
---

# Obsidian Second Brain

## Rolle und Projekt (Stand 2026-09)

https://github.com/eugeniughelbur/obsidian-second-brain beschreibt eine dauerhafte Erinnerung für CLI-Agenten im eigenen Markdown-Vault. Das Projekt erweitert das [LLM Wiki Pattern](../concepts/LLM%20Wiki%20Pattern.md): Quellen sollen bestehende Notizen aktualisieren, Widersprüche mit Herkunft bearbeiten und neue Zusammenhänge als Synthese speichern. Es ist ein anderes Projekt als [Claude Obsidian](Claude%20Obsidian.md). [tweet-2100980633677746295](../sources/tweet-2100980633677746295.md)

## Einstieg und Arbeitsweise (Stand 2026-09)

Das README empfiehlt zuerst /obsidian-init, /obsidian-save und /obsidian-find. /obsidian-ingest verarbeitet URLs, PDFs, Audio und Bilder und verteilt belegte Inhalte auf passende Notizen; /obsidian-health prüft unter anderem veraltete Aussagen, Widersprüche und Waisen. Forschung kann vom vorhandenen Vault ausgehen und nur Wissenslücken ergänzen. [tweet-2100980633677746295](../sources/tweet-2100980633677746295.md)

Für [Claude Code](Claude%20Code.md) nennt es die Plugin-Installation mit /plugin marketplace add eugeniughelbur/obsidian-second-brain und /plugin install obsidian-second-brain@obsidian-second-brain. OBSIDIAN_VAULT_PATH zeigt auf den Vault; Plugin-Kommandos verwenden den Namespace /obsidian-second-brain:. Für [Codex](Codex.md) und OpenCode empfiehlt das gespeicherte README den Agent-Skills-Build statt der älteren eigenständigen Builds. [tweet-2100980633677746295](../sources/tweet-2100980633677746295.md)

## Suche und Wissenspflege (Stand 2026-09)

Die Suche funktioniert zunächst per Keyword. Optional ergänzt ein lokales Ollama-Modell bge-m3 oder ein kompatibler Embedding-Endpunkt semantische Suche; der Index wird inkrementell gebaut und muss mit Änderungen aktuell gehalten werden. Ohne verfügbares Modell fällt die Suche laut README auf Keywords zurück. [tweet-2100980633677746295](../sources/tweet-2100980633677746295.md)

Die Freshness-Policy nennt drei zulässige Formen: zeitlose Aussagen, datierte Aussagen oder Verweise auf die lebende Quelle. Schnell wechselnde Zahlen und Status sollen einen Stand oder einen solchen Verweis bekommen, statt undatiert kopiert zu werden. Ein Linter prüft die Regel. [tweet-2100980633677746295](../sources/tweet-2100980633677746295.md)

## Automatisierung und Grenzen (Stand 2026-09)

Das README beschreibt optionale morgendliche, nächtliche, wöchentliche und Health-Abläufe. Der Hintergrundagent ist zunächst inaktiv, hat beschränkte Dateitools und soll hinzufügen beziehungsweise aktualisieren, aber weder löschen noch mergen. Ein optionaler Recall-Hook injiziert bis zu vier kurze relevante Notizen oder enthält sich bei geringer Sicherheit. [tweet-2100980633677746295](../sources/tweet-2100980633677746295.md)

Die Kernkommandos und freie Recherchepfade benötigen laut Projekt keine zusätzlichen API-Keys; andere Forschungsfunktionen nutzen externe Dienste. Lokale Markdown-Speicherung bedeutet daher nicht, dass jeder Workflow lokal bleibt. Suchbenchmarks, automatische Widerspruchsauflösung und Wartungsqualität sind Projektangaben, hier nicht getestet; die genannten Kommandozahlen variieren innerhalb des gespeicherten README. [tweet-2100980633677746295](../sources/tweet-2100980633677746295.md)
