---
tags: [agents, tools]
sources: [tweet-2115326446084493673.md]
created: 2026-11-01
updated: 2026-11-01
---

# Claude Video Effects

## Überblick (Stand 2026-10)

Vibha-Ramprakash/claude-video-effects ist ein Claude-Code-Skill für Talking-Head-Videos: Video in den Chat ziehen, `/effects <name>` tippen, fertig. Beispiele: `/effects orbit from 3 to 6 seconds`, `/effects spotlight when I say "kill the lights"`, `/effects comment-box at the end, typing CLAUDE`. Mehrere Effekte lassen sich in einer Anfrage stapeln. [tweet-2115326446084493673](../sources/tweet-2115326446084493673.md)

Zeitangaben in normaler Sprache ("when I say ...") werden von Claude auf die genaue Sekunde gelegt. Vor dem Rendern prüft der Skill einige Frames und verschiebt alles, was das Gesicht verdecken würde, hinter den Kopf. Ausgabe: `<video>_effects.mp4` neben dem Original, Audio unverändert, 1080p (4K auf Anfrage). [tweet-2115326446084493673](../sources/tweet-2115326446084493673.md)

## Effekte

Die README listet 45 Effekte (Repository-Titel: 36; Tweet: 45), darunter noise, lineup, locked-on, orbit, backdrop-word, spotlight, checklist, liquid-glass-graph, carousel-spin, led-sign, slow-push, messages und place-in-grid, plus Bonus-Varianten wie glitter-spotlight. [tweet-2115326446084493673](../sources/tweet-2115326446084493673.md)

## Installation und Grenzen

`git clone https://github.com/Vibha-Ramprakash/claude-video-effects ~/.claude/skills/effects` (Windows: `$HOME\.claude\skills\effects`), danach Claude Code neu starten. Beim ersten Lauf richtet sich der Skill selbst ein (etwa zwei Minuten) und installiert fehlendes ffmpeg und Python. Gesichtserkennung nutzt OpenCV YuNet, Personenfreistellung den MediaPipe Selfie Segmenter. [tweet-2115326446084493673](../sources/tweet-2115326446084493673.md)

Die Autorin nennt es "starter versions": keine Sounds oder Untertitel, Ergebnis vor dem Posten prüfen, am besten bei vertikalen Handyvideos mit der Person im Bild. Kennzahlen in Effekten sollen echte Zahlen sein. Nicht ausgeführt. Einordnung: [Agentic Video Production](../concepts/Agentic%20Video%20Production.md). [tweet-2115326446084493673](../sources/tweet-2115326446084493673.md)
