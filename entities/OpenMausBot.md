---
tags: [agents, tools, product-building]
sources: [tweet-2115355703682670950.md]
created: 2026-11-01
updated: 2026-11-01
---

# OpenMausBot

## Überblick (Stand 2026-10)

milind-soni/OpenMausBot ist ein unabhängiges Open-Source-Projekt (Apache 2.0), inspiriert von Grok Bot: ein Team von KI-Bots in einer Chat-App, jeder mit eigener Persönlichkeit, eigenem Modell, eigenem Computer und eigenen Apps. Früherer Name OpenGrokBot, auch MausBot. Das Projekt betont, nicht mit xAI, Meta, OpenAI oder Manus verbunden zu sein und keinen Krypto-Token zu haben. [tweet-2115355703682670950](../sources/tweet-2115355703682670950.md)

## Funktionen laut README

- Eigene Agenten mitbringen: Bots laufen auf den lokal installierten claude-, codex- und grok-CLIs mit den vorhandenen Anmeldungen, ohne Proxy; eigene CLI-Binärdatei in Settings → Engines. [tweet-2115355703682670950](../sources/tweet-2115355703682670950.md)
- Lokal zuerst: ein kleiner Harness-Server auf 127.0.0.1; Transkripte, Schlüssel und Ereignisse liegen in `~/.openmausbot`. [tweet-2115355703682670950](../sources/tweet-2115355703682670950.md)
- Computer je Bot: Cloud-Linux-Desktop, isolierte lokale VM oder der eigene Rechner (macOS und Ubuntu Xorg nach ausdrücklicher Freigabe), dazu über 500 Apps via Composio. [tweet-2115355703682670950](../sources/tweet-2115355703682670950.md)
- Modellauswahl je Bot, Wechsel mitten im Gespräch; Freigabekarten für Shell-Befehle und Dateiänderungen. [tweet-2115355703682670950](../sources/tweet-2115355703682670950.md)

Installationen: macOS (Apple Silicon und Intel), Windows x64, Ubuntu 24.04 (.deb oder AppImage, Beta). [tweet-2115355703682670950](../sources/tweet-2115355703682670950.md)

## Evidenzgrenze

Nur README gelesen; das Video im Tweet hat kein Transkript. Die Vergleichstabelle zu Grok Bot, Meta Muse, OpenAI dots, Cue und Instinct stammt vom Projekt selbst. Verwandt: [OpenBot](OpenBot.md) (andere Plattform), [GrokBot.dev](GrokBot.dev.md) (Katalog von Grok-Bot-Setups). [tweet-2115355703682670950](../sources/tweet-2115355703682670950.md)
