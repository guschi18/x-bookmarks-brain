---
tags: [tools, agents, llm-training]
sources: [tweet-2090856982383300898.md]
created: 2026-10-12
updated: 2026-10-12
---

# FreeToken

## Laufzeit und Mechanismen (Stand 2026-08)

Repository: https://github.com/FlashML-org/FreeToken; Paper: https://arxiv.org/abs/2608.16157. Die gespeicherte README beschreibt einen Edge-MoE-Serving-Ansatz, der GPU, CPU, Hauptspeicher und Verbindungen als gemeinsame Inferenzressourcen behandelt. [tweet-2090856982383300898](../sources/tweet-2090856982383300898.md)

Genannte Mechanismen sind bandbreitenadaptive CPU-/GPU-Co-Ausführung, doppelt gepuffertes vollständiges Layer-Streaming beim Prefill, globaler LRU-Expertencache, graphkompatible Ausführung und das FTW-Gewichtsformat. [tweet-2090856982383300898](../sources/tweet-2090856982383300898.md)

Semantische Checkpoints für rekurrenten Zustand und KV-Caches sollen Kontextänderungen durch Agententools ohne vollständige Neuberechnung unterstützen. VRAM kann laut README zur Laufzeit zwischen Expertencache und KV-Speicher umverteilt werden, ohne Engine-Neustart oder erneutes Gewichts-Laden. [tweet-2090856982383300898](../sources/tweet-2090856982383300898.md)

## Einrichtung und Agentenanbindung (Stand 2026-08)

Die README nennt eine Windows-/Linux-Desktopanwendung unter https://www.flashml.ai/ sowie die CLI-Installation uv pip install "freetoken[accel]"; separate Dokumentationslinks betreffen Installation, Quickstart, unterstützte Modelle und CLI. [tweet-2090856982383300898](../sources/tweet-2090856982383300898.md)

OpenAI-/Anthropic-kompatible Schnittstellen sollen vorhandene Coding- und Tool-Agenten anbinden. Das ist ein weiterer Laufzeitansatz für [Local Agent Inference](../concepts/Local%20Agent%20Inference.md); API-Kompatibilität allein belegt keinen hier getesteten zuverlässigen Agentenbetrieb. [tweet-2090856982383300898](../sources/tweet-2090856982383300898.md)

## Aussagegrenzen (Stand 2026-08)

Datacenter-class intelligence, interaktive Geschwindigkeit für 290B+-Modelle sowie breite Hardware-/Modellunterstützung sind Repository-Claims ohne hier reproduzierte Messung. Modell-/Quantisierungslisten gehören zur gespeicherten README und sind nicht automatisch am Tweetdatum datiert. [tweet-2090856982383300898](../sources/tweet-2090856982383300898.md)

Die gespeicherte Website enthält nur Download-/Changelog-Navigation; die README nennt Apache 2.0. RAM-/VRAM-Voraussetzungen und eine Leistungszusage für die konkrete Nutzerhardware ergeben sich aus diesem kurzen Download-Reply nicht. [tweet-2090856982383300898](../sources/tweet-2090856982383300898.md)
