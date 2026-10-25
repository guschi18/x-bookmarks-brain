---
tags: [agents, tools, marketing]
sources: [tweet-2098941338297458746.md, tweet-2052516685052285101.md]
created: 2026-10-08
updated: 2026-10-14
---

# HyperFrames

## Komposition und Rendering (Stand 2026-09)

[Repository](https://github.com/heygen-com/hyperframes): HTML, CSS, Medien und seekbare Animationen bilden die Komposition. data-start, data-duration und Tracks steuern die Zeit; Headless Chrome rendert Frames und FFmpeg kodiert MP4. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

Laut README werden GSAP, CSS, Lottie, Three.js, Anime.js, WAAPI und eigene Adapter unterstützt. Im Unterschied zum beschriebenen Remotion-Autorenmodell ist React keine Voraussetzung. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## Agenten und CLI (Stand 2026-09)

Der dokumentierte Einstieg lautet npx hyperframes init my-video, danach npx hyperframes preview und npx hyperframes render; Voraussetzungen sind Node.js 22+ und FFmpeg. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

npx hyperframes skills update installiert laut README den Kern aus Router und Domain-Skills; Erstellungsworkflows werden bei Bedarf geladen. Die vollständige Sammlung zählt 20 Skills und umfasst unter anderem Produktfilme, PR-Videos, Captions und Talking-Head-Recuts. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## Grenzen (Stand 2026-09)

Die README nennt Apache 2.0 sowie lokale und AWS-Lambda-Renderpfade. Determinismus und Produktionsnutzung sind Projektangaben, keine eigene Renderprüfung. [Agentic Video Production](../concepts/Agentic%20Video%20Production.md) behandelt den Produktionsablauf unabhängig vom Renderer. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## Story-App auf Vercel (Stand 2026-05)

James Russos gespeicherter Artikel beschreibt eine Next.js-Anwendung: Das Vercel AI SDK orchestriert Textmodelle für Story-Outline und HyperFrames-HTML, TTS liefert die Erzählspur. `<hyperframes-player>` bettet eine Browser-Vorschau der Komposition ein, bevor für den Export gerendert wird. Dies ergänzt den allgemeinen Ablauf in [Agentic Video Production](../concepts/Agentic%20Video%20Production.md) um eine konkrete Anwendungsarchitektur. [tweet-2052516685052285101](../sources/tweet-2052516685052285101.md)

Der enthaltene React-Ausschnitt lädt `@hyperframes/player` nach dem Mount dynamisch und zeigt die Vorschau aus `/api/preview`. Für MP4 nennt der Artikel Vercel Sandbox als Firecracker-Umgebung mit Chromium und FFmpeg sowie Vercel Blob für die Ausgabedatei; der Vorschaupfad benötigt diesen Videoexport nicht. [tweet-2052516685052285101](../sources/tweet-2052516685052285101.md)

Korrekturen an Text, Farben oder Layout erfolgen laut Artikel als HTML-/Code-Änderung statt erneuter Bildgenerierung. Die etwa 0,02 Dollar pro Geschichte mit günstigen Cloud-Modellen beziehungsweise rund 0,20 Dollar mit der genannten Frontier-Kombination sind historische Autorenbeispiele vom Mai 2026, keine aktuellen Preise oder hier reproduzierten Gesamtkosten. [tweet-2052516685052285101](../sources/tweet-2052516685052285101.md)

Der gespeicherte Artikel verweist sprachlich auf eine App und ein Vercel-Template, enthält aber keine strukturierten Links zu diesen Artefakten. Damit liegt ein Bauplan mit Player-Code vor, kein vollständig gespeicherter oder getesteter App-Quelltext. [tweet-2052516685052285101](../sources/tweet-2052516685052285101.md)
