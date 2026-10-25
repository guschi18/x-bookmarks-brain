---
tags: [tools, product-building]
sources: [tweet-2113997690845503966.md]
created: 2026-10-25
updated: 2026-10-25
---

# FilmCraft

## Überblick (Stand 2026-10)

FilmCraft (GitHub storytold/filmcraft, vom ArtCraft-Team) ist ein nichtlinearer Videoeditor in reinem Rust für macOS, Windows und Linux sowie als WebAssembly-Build im Browser. Der Post nennt 16K Sterne und Apache-2.0. [tweet-2113997690845503966](../sources/tweet-2113997690845503966.md)

## Funktionen laut README (Stand 2026-10-25)

Die folgenden Angaben stammen aus dem README, das der Nutzer als Quelle genannt hat; sie sind Projektangaben und wurden nicht getestet. [tweet-2113997690845503966](../sources/tweet-2113997690845503966.md)

- Lizenz: MIT oder Apache-2.0 nach Wahl; der Post nennt nur Apache-2.0. [tweet-2113997690845503966](../sources/tweet-2113997690845503966.md)
- Schnitt und Farbe: Drei-Punkt-Schnitt, Trim-Werkzeuge, Marker, Nesting, Undo; Farbkorrektur in linearem 32-Bit-Float, mehr als 90 Effekte und etwa 30 Übergänge. [tweet-2113997690845503966](../sources/tweet-2113997690845503966.md)
- Zeit: ganzzahlige Ticks (254.016.000.000 je Sekunde), daher exakte Bildraten wie 23,976 und 29,97. [tweet-2113997690845503966](../sources/tweet-2113997690845503966.md)
- Codecs: H.264, HEVC, ProRes, AAC, VP8, VP9, Opus und AV1 laut Projekt selbst nach öffentlichen Spezifikationen geschrieben; MP3, FLAC, ALAC und Vorbis laufen über die symphonia-Bibliothek. [tweet-2113997690845503966](../sources/tweet-2113997690845503966.md)
- Austausch: FCP7 XML, FCPXML, OpenTimelineIO, EDL, AAF und OMF. [tweet-2113997690845503966](../sources/tweet-2113997690845503966.md)

## Agentensteuerung per MCP (Stand 2026-10-25)

Jede Aktion der Oberfläche ist ein Command (laut README mehr als 650). UI, CLI, ein JSON-Kontrollkanal über TCP und ein MCP-Server nutzen dieselbe Command-Registry, ein Agent handelt also über dieselben Pfade wie ein Mensch (Beispiele `engine.execute`, `timeline.place`, `effects.setParam`). Die Oberfläche lässt sich zusätzlich per Maus, Tastatur und Screenshot (`ui.screenshot`) automatisieren. Headless startet der MCP-Server mit `cargo run --release -p filmcraft-cli -- mcp`, mit Desktop-App zusätzlich `--control 9876`. Siehe [Model Context Protocol](../concepts/Model%20Context%20Protocol.md). [tweet-2113997690845503966](../sources/tweet-2113997690845503966.md)

## Reifegrad und Grenzen (Stand 2026-10-25)

Das Projekt nennt sich Alpha mit etwa 86 % Funktionsbreite und etwa 56 % Produktionsreife. Selbst genannte Lücken: Farbkorrektur, Keys und Export laufen noch auf der CPU; kein nativer .prproj-Import; kein VST3, Audio Units oder OpenFX; H.264 ist der einzige Software-Delivery-Codec, H.265-Export nur über Hardware-Encoder, kein AV1-Export; wenig KI-Funktionen. Windows und Linux sind weniger getestet als macOS; bekannt sind GPU-Abstürze auf manchen AMD-Systemen. Der Post spricht von einem "professionellen" Editor mit "jedem Codec"; das README relativiert das. Der Release v0.12.0 enthält nur Changelog-Einträge und streicht FreeBSD aarch64. [tweet-2113997690845503966](../sources/tweet-2113997690845503966.md)
