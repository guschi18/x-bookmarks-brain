---
tags: [tools, research, product-building]
sources: [tweet-2093762643639115999.md]
created: 2026-10-09
updated: 2026-10-09
---

# JoyAI-Video-Edit

## Verfahren (Stand 2026-08)

[Repository: jd-opensource/JoyAI-Video-Edit](https://github.com/jd-opensource/JoyAI-Video-Edit). Das Projekt beschreibt anweisungsgeführte Bearbeitung laufender Kamera- oder Videostreams: neue Frames werden kausal verarbeitet, ohne vorab festgelegte Gesamtlänge oder Zugriff auf zukünftige Frames. Textvorgaben steuern unter anderem Hintergründe, Objekte, Stil, Bewegung und Änderungen anhand eines Referenzbilds. [tweet-2093762643639115999](../sources/tweet-2093762643639115999.md)

Ein MLLM-Condition-Encoder, ein kausales Video-VAE und ein multimodaler Diffusionstransformer mit 16 Milliarden Parametern bilden den dokumentierten Kern; autoregressive Diffusion, Distillation und begrenzter KV-Zustand sollen Streaming-Durchsatz und zeitliche Konsistenz ermöglichen. [tweet-2093762643639115999](../sources/tweet-2093762643639115999.md)

## Einstieg und Hardware (Stand 2026-08)

Die README verlinkt [Modellgewichte](https://huggingface.co/jdopensource/JoyAI-Video-Edit), eine [Browserdemo](https://huggingface.co/spaces/wxDai/joyai-video-edit) und den [Deployment Guide](https://github.com/jd-opensource/JoyAI-Video-Edit/blob/main/DEPLOYMENT.md). Der Einstieg verwendet Conda/Python 3.10, deploy/requirements.txt, eine zu bauende CUDA-Kernelbibliothek, GPU-abhängiges SageAttention/flash-attn und MiMo-VL als externe Abhängigkeit; Start über `cd deploy` und `bash run_server.sh`. [tweet-2093762643639115999](../sources/tweet-2093762643639115999.md)

Projektangaben unterscheiden Konfigurationen: 30 FPS bei 720 × 1248 im Deployment-Benchmark; auf einer RTX 5090 mit 32 GB nennt der News-Eintrag 840 × 480 bei 24 FPS, auf einer RTX PRO 6000 zusätzlich 720p bei 16 FPS. Die Auflösungen und Hardware dürfen nicht zu einer universellen 30-FPS-Aussage kombiniert werden. [tweet-2093762643639115999](../sources/tweet-2093762643639115999.md)

## Grenzen und Einordnung (Stand 2026-08)

Lizenz laut README: Apache 2.0. Der Server bindet im gespeicherten Default an `0.0.0.0:8080`; die Startanleitung nennt SSH-Portweiterleitung für Remote-Rechner. Die vollständige Trainings-/Datenpipeline und Diffusers-Unterstützung stehen in diesem historischen README-Stand noch auf der TODO-Liste. Installation, Qualität und Benchmarks wurden hier nicht reproduziert. [tweet-2093762643639115999](../sources/tweet-2093762643639115999.md)

Verwandter Produktionsbereich: [Agentic Video Production](../concepts/Agentic%20Video%20Production.md). Das Originalbild illustriert wechselnde Anweisungen innerhalb eines Streams und Projektbenchmarks; es belegt keine unabhängige Evaluation. [tweet-2093762643639115999](../sources/tweet-2093762643639115999.md)
