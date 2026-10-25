---
tags: [tools, llm-training, research]
sources: [tweet-2098941338297458746.md]
created: 2026-10-08
updated: 2026-10-08
---

# VoxCPM

## Modell und Steuerung (Stand 2026-09)

[Repository](https://github.com/OpenBMB/VoxCPM): tokenizer-freie diffusion-autoregressive Sprachsynthese. Der gespeicherte VoxCPM2-Stand nennt 2B Parameter, 30 Sprachen und 48-kHz-Ausgabe; Modell-/Qualitätszahlen sind Angaben des Projekts. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

Voice Design steuert die Stimme per Beschreibung, Controllable Cloning nutzt Referenzaudio plus Stilhinweise, Ultimate Cloning zusätzlich dessen exaktes Transkript. Die Python-API stellt generate und generate_streaming bereit. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## Betrieb und Anpassung (Stand 2026-09)

Die README nennt Python 3.10 bis unter 3.13, PyTorch ab 2.5 und CUDA ab 12 für den GPU-Pfad; Web-Demo und CLI sind vorhanden. Nano-vLLM, vLLM-Omni und llama.cpp-omni/GGUF sind alternative dokumentierte Serving-/Gerätepfade. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

SFT und LoRA sind dokumentiert; das Projekt behauptet Anpassung mit fünf bis zehn Minuten Audio. VoxCPM2, VoxCPM1.5 und VoxCPM-0.5B haben unterschiedliche Fähigkeiten und Ressourcenangaben und sind keine austauschbaren Stände. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## Grenzen (Stand 2026-09)

Die README warnt vor schwankender Stil-/Stimmsteuerung und empfiehlt gegebenenfalls mehrere Versuche. Benchmarks und Laufzeitangaben sind keine eigene Reproduktion; Apache-2.0-Code und Gewichte belegen keine gleichmäßige Qualität in allen Sprachen. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)
