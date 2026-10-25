---
tags: [tools, llm-training, agents]
sources: [tweet-2095906342154424750.md]
created: 2026-10-03
updated: 2026-10-03
---

# Magnitude

## Überblick (Stand 2026-09)

Magnitude ist laut README ein quelloffener Inferenzserver (Apache 2.0), der die besten lokalen Modelle für die vorhandene Hardware ausführt und in den bereits genutzten Agenten einbindet. Er läuft auf macOS und Linux, unter Windows über WSL. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)

## Ablauf (Stand 2026-09)

Installation mit `npm i -g @magnitudedev/cli`, dann `magnitude setup`: Die Einrichtung profiliert Chip, Speicher und Bandbreite, empfiehlt passende Modelle mit geschätzten Token/s, lädt die Auswahl herunter, stimmt Spekulatives Decoding und Parallelität ab und verbindet das Harness. Modelle werden bei Bedarf geladen und bei Leerlauf oder Speicherdruck entladen. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)

Unterstützt werden laut README Pi, OpenCode, Hermes, OpenClaw, [Codex](Codex.md), [Claude Code](Claude%20Code.md), Oh My Pi und Cline sowie ein eingebautes Harness; die Einrichtung kann auch per Agenten-Prompt laufen. Der Post nennt Ranking nach Tempo, Genauigkeit, Intelligenz und Speicherbedarf. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)

## Begründung (Stand 2026-09)

Die README-FAQ argumentiert, ein Agent würde Ollama blind einrichten, weil er Hardware, passende Quantisierung und Tempo nicht kenne; Magnitude liefere stattdessen Empfehlungen für die konkrete Maschine. Hintergrund ist der Artikel in [Local Agent Inference](../concepts/Local%20Agent%20Inference.md). [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)

## Grenzen (Stand 2026-09)

Die Empfehlungen und Tempoangaben sind in den gespeicherten Daten nicht gemessen oder unabhängig geprüft; der Autor wirbt um GitHub-Sterne. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)
