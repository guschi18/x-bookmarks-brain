---
tags: [agents, tools, product-building]
sources: [tweet-2093344589788643702.md]
created: 2026-10-10
updated: 2026-10-10
---

# Diffusion Studio

## Rolle und Dokumentmodell (Stand 2026-08; gespeicherte README)

[diffusionstudio/editor](https://github.com/diffusionstudio/editor) beschreibt einen Videoeditor, dessen Dokumente SolidJS-/JSX-Module sind. Änderungen im Canvas werden in den Code zurückgeschrieben; Codeänderungen aktualisieren die Editor-Knoten. Menschen können dadurch die Ausgabe eines Agenten unmittelbar in der Oberfläche weiterbearbeiten. Das ist ein eigener Werkzeugpfad für [Agentic Video Production](../concepts/Agentic%20Video%20Production.md). [tweet-2093344589788643702](../sources/tweet-2093344589788643702.md)

## Dokumentierter Ablauf

Die README nennt den Skill-Befehl `npx skills add diffusionstudio/skills` und `/editor` für Schnitt, Motion Graphics, Untertitel und Kurzclips. Die CLI `dapi` öffnet Projektordner, untersucht Medien, erfasst Vorschauframes, prüft Szenenstrukturen und rendert Ausgaben; ein Headless-Runtime-Paket ist im Repository dokumentiert. [tweet-2093344589788643702](../sources/tweet-2093344589788643702.md)

```text
/editor edit the footage in /path/to/folder
/watch In three bullets, explain what starts the conflict. Include timestamps. <video URL>
dapi media probe clip.mp4
dapi media grab clip.mp4 -t 0 12 45
dapi media transcribe interview.wav
dapi check
```

Diese Beispiele sind dokumentierte Einstiegspunkte, keine in diesem Vault ausgeführten Tests. Die gespeicherte Quelle bewahrt außerdem vollständige Prompts für Produktpromos, physikalisch genaue Animationen und vertikale Highlight-Clips. [tweet-2093344589788643702](../sources/tweet-2093344589788643702.md)

## Betrieb und Grenzen

Der lokale Entwicklungsweg verlangt Node ab 20, npm, eine apps/web/.env und den Dev-Prozess. Die README nennt MPL-2.0, nimmt Markenassets jedoch von dieser Lizenz aus. Der Tweet verspricht Windows ab 2.000 und Mobile ab 15.000 Stars; diese historische Zusage bestätigt keine heutige Plattformverfügbarkeit. [tweet-2093344589788643702](../sources/tweet-2093344589788643702.md)

CLI, Rendering, automatischer Schnitt und Generierungsmodelle wurden nicht ausgeführt; die README belegt die Architektur und vorgesehene Bedienung, keine garantierte Filmqualität. [tweet-2093344589788643702](../sources/tweet-2093344589788643702.md)
