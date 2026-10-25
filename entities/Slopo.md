---
tags: [tools, agents]
sources: [tweet-2099244880413221248.md]
created: 2026-10-08
updated: 2026-10-08
---

# Slopo

## Gespeicherte Ankündigung (Stand 2026-09)

Rafal Kochanowski kündigt v0.8.0 mit verbessertem Code-Chunking an, damit Coding-Agenten doppelte Implementierungen entdecken. Der Tweet liefert keine Anleitung. [tweet-2099244880413221248](../sources/tweet-2099244880413221248.md)

## Ergänzende Primärrecherche (Stand 2026-10-08)

Die folgenden Angaben stammen aus der beim Review gelesenen [Repository-README](https://github.com/rafal-qa/slopo), nicht aus Raw: Slopo vergleicht Code-Embeddings, bündelt ähnliche Blöcke und priorisiert auch deren Entfernung im Codebestand. Ein Mensch oder Agent prüft, ob Ähnlichkeit eine vermeidbare Dublette bedeutet. [tweet-2099244880413221248](../sources/tweet-2099244880413221248.md)

Installation: uv tool install slopo; danach slopo init und ein Embedding-Modell konfigurieren. Die README unterstützt externe Anbieter oder lokale Modelle über Ollama beziehungsweise kompatible Server. slopo show-config prüft die Konfiguration; slopo index und slopo embed aktualisieren Daten; slopo analyze untersucht den Bestand, slopo review Git-Änderungen. [tweet-2099244880413221248](../sources/tweet-2099244880413221248.md)

Geprüfte Cluster lassen sich über ihre Hashes in slopo.ignore.txt ausblenden. Der beschriebene Agentenablauf eignet sich auch für [Claude Code](Claude%20Code.md) und [Codex](Codex.md). Ähnlichkeit beweist keine sichere Zusammenlegung; Qualität und Einsparungen wurden hier nicht gemessen. [tweet-2099244880413221248](../sources/tweet-2099244880413221248.md)

## Version und Grenze

[PyPI](https://pypi.org/project/slopo/) führt am Recherchetag v0.9.0 vom 24.09.2026. Die v0.8.0-Ankündigung vom 13.09.2026 bleibt historische Quelle. Keine Installation oder Codeanalyse wurde durchgeführt. [tweet-2099244880413221248](../sources/tweet-2099244880413221248.md)
