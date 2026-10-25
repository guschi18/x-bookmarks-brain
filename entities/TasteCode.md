---
tags: [agents, tools, product-building]
sources: [tweet-2100842257804841326.md]
created: 2026-10-07
updated: 2026-10-08
---

# TasteCode

## Rolle und Bezug (Stand 2026-09)

[TasteCode](https://github.com/Leonxlnx/tastecode) ist laut README ein lokaler Desktop-Arbeitsraum für [Codex](Codex.md), [Claude Code](Claude%20Code.md) und Grok. Leon Lin kündigt das Open-Source-Projekt als gemeinsame Arbeit mit @blueemi99 an; er ist auch Autor von [Taste Skill](Taste%20Skill.md). [tweet-2100842257804841326](../sources/tweet-2100842257804841326.md)

## Funktionen und Voraussetzungen (Stand 2026-09)

Die README beschreibt providerabhängige Modelle, Berechtigungen und Session-Steuerung; Projektsuche, Umbenennen und Anpinnen; Terminal, Browser-Vorschau, Anhänge, Git-Kontext, Diffs und Checkpoints sowie Design Mode zum Prüfen und Bearbeiten von Weboberflächen. Nicht unterstützte Provider-Funktionen werden laut Projekt ausgeblendet oder eingeschränkt. [tweet-2100842257804841326](../sources/tweet-2100842257804841326.md)

Für die regulären Installer nennt die Quelle Windows 10/11 x64 oder macOS auf Apple Silicon, mindestens eine installierte und angemeldete Provider-CLI und Git für Checkpoints/Worktrees. [Releases](https://github.com/Leonxlnx/tastecode/releases) enthalten Installer, Checksummen und Updatehinweise; Linux ist im gespeicherten Release-Stand eine separate Vorschau. [tweet-2100842257804841326](../sources/tweet-2100842257804841326.md)

## Lokales Modell und Grenzen (Stand 2026-09)

Der lokale Server verwaltet laut README Zustand und Orchestrierung, Provider-Prozesse laufen auf dem Rechner, Zugangsdaten bleiben beim Provider beziehungsweise im Betriebssystem-Speicher und werden nicht roh an den Renderer gegeben. Dies ist die Projektbeschreibung, kein hier durchgeführter Sicherheitsaudit. [tweet-2100842257804841326](../sources/tweet-2100842257804841326.md)

Der gespeicherte Stand ist frühe Beta 0.1.1 mit angekündigten Fehlern und Änderungen. Windows-Builds sind unsigniert, macOS-Builds laut Release signiert und notarisiert. Die README (Stand 2026-10-08) listet Downloads nur für Windows x64 und macOS Apple Silicon; eine Linux-Vorschau ist dort nicht mehr erwähnt. Veröffentlichung von Tests oder Installern ersetzt keinen eigenen Kompatibilitätstest. [tweet-2100842257804841326](../sources/tweet-2100842257804841326.md)
