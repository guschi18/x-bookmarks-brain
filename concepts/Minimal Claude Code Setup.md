---
tags: [agents, tools]
sources: [tweet-2101411232771113143.md]
created: 2026-10-03
updated: 2026-10-08
---

# Minimal Claude Code Setup

## Definition (Stand 2026-09)

alex getman entfernt aus [Claude Code](../entities/Claude%20Code.md) fast alles und behält nur read, inspect und write. Er orientiert sich an Pis minimalistischem Ansatz und will so den Verbrauch eines Abos begrenzen. [tweet-2101411232771113143](../sources/tweet-2101411232771113143.md)

## Mechanismus

- Startkontext unter 2k Token; der Screenshot zeigt Claude Code v2.1.278 im Projekt signal-forge mit 1,8k von 200k Token (1 Prozent) bei Opus 5 (Stand 2026-09-19). [tweet-2101411232771113143](../sources/tweet-2101411232771113143.md)
- Das Kontextfenster ist auf 200k Token begrenzt, damit früher kompaktiert wird, statt mit aufgeblähtem Kontext Limits zu verbrauchen; der Screenshot zeigt die Auto-Compact-Einstellung 200k. [tweet-2101411232771113143](../sources/tweet-2101411232771113143.md)
- Betrieb im 20-Dollar-Claude-Pro-Plan mit Opus 5 auf niedrigem Effort, laut Autor für ihn die einzig sinnvolle Konfiguration für echte Arbeit. Das gilt für Opus 5; Opus 5.5 denkt bei gleicher Stufe mehr, siehe [Model Selection Evals](Model%20Selection%20Evals.md). [tweet-2101411232771113143](../sources/tweet-2101411232771113143.md)

## Repository (Stand 2026-09)

Auf ausdrücklichen Hinweis des Wiki-Besitzers: Das zugehörige Repository ist https://github.com/alexgetmancom/claudecut. Sein Inhalt wurde nicht geprüft; ob es die im Post beschriebene Konfiguration enthält, ist nicht belegt. [tweet-2101411232771113143](../sources/tweet-2101411232771113143.md)

## Grenzen

Welche Werkzeuge und Prompts entfernt wurden und wie, nennt der Post nicht. Wie weit sich das Abo damit strecken lässt, will der Autor erst in einem Folgebericht zeigen; es gibt keine Messung. Verwandt: [Context Engineering](Context%20Engineering.md). [tweet-2101411232771113143](../sources/tweet-2101411232771113143.md)
