---
tags: [llm-training, tools, research]
sources: [tweet-2055492991918518692.md]
created: 2026-10-01
updated: 2026-10-01
---

# SANA-WM

## Aufgabe und Verfahren (Stand 2026-05)

SANA-WM erzeugt laut gespeichertem Abstract aus Bild und 6-DoF-Kameratrajektorie bis zu eine Minute 720p-Video. Der 2,6B-Backbone kombiniert frameweise Gated DeltaNet mit Softmax-Attention, zwei Kamerakontrollzweige und metrische Pose-Annotationen aus öffentlichen Videos. [tweet-2055492991918518692](../sources/tweet-2055492991918518692.md)

Die Projektseite beschreibt einen separaten 17B-Refiner als zweite Stufe. Alle dort gezeigten Videos verwenden das bidirektionale Modell plus Refiner; ihre Startbilder wurden mit externen Bildmodellen erzeugt. Deshalb ist die Galerie kein alleiniger Qualitätsbeleg für den 2,6B-Backbone. [tweet-2055492991918518692](../sources/tweet-2055492991918518692.md)

## Reproduzierbare Einstiege und Messgrenzen (Stand 2026-05)

Gespeichert sind https://github.com/NVlabs/Sana, https://nvlabs.github.io/Sana/WM/ und der Abstract https://arxiv.org/abs/2605.15178. Die Familien-README enthält auch Bildmodelle und spätere Video-/Streaming-Veröffentlichungen; deren Ergebnisse sind nicht automatisch SANA-WM-Ergebnisse. [tweet-2055492991918518692](../sources/tweet-2055492991918518692.md)

Die Autoren nennen etwa 213.000 Clips, 15 Trainingstage auf 64 H100 und 36-fachen Durchsatz im eigenen Ein-Minuten-Benchmark. 34 Sekunden auf RTX 5090 beziehen sich auf das Denoising der destillierten NVFP4-Variante, nicht pauschal auf VAE, Backbone und Refiner zusammen. Es gibt hier keinen unabhängigen End-to-End-Test. [tweet-2055492991918518692](../sources/tweet-2055492991918518692.md)

## Evidenzgrenzen (Stand 2026-05)

Roemmeles berichteter Einsatz in einer Zero-Human Company und die Übertragung auf physikalisch verlässliche Robotik-Simulationen sind nicht durch Einsatzdaten oder physikalische Validierung im Paket belegt. Das X-Video hat einen leeren Transkripteintrag und bleibt unauswertbar. [tweet-2055492991918518692](../sources/tweet-2055492991918518692.md)
