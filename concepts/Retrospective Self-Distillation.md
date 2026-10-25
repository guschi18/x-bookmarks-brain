---
tags: [research, agents, llm-training]
sources: [tweet-2113509229298602311.md]
created: 2026-10-24
updated: 2026-10-24
---

# Retrospective Self-Distillation

## Definition (Stand 2026-10)

Retrospective Self-Distillation (RSD) ist ein mehrrundiges Verfahren aus dem arXiv-Paper 2610.27495 ("Self-Evolving Agents through Privileged Retrospective Distillation", eingereicht 20.10.2026). Es macht aus Agenten-Erfahrung dichte Trainingssignale, wenn weder Musterlösungen noch Verifier-Rewards vorliegen. [tweet-2113509229298602311](../sources/tweet-2113509229298602311.md)

## Mechanismus (Stand 2026-10)

Für jede Trajektorie ist dasselbe Modell Schüler und Lehrer. Der Lehrer bewertet die tatsächlichen Aktionen neu, mit privilegiertem Kontext: frühere Fälle, Lehren, Reflexion je Zug und Rückblick auf den Ausgang. Die Lehrerverteilung wird per On-Policy-Selbstdestillation in die Policy zurückgeführt. Mit jeder Runde wächst der Erfahrungsspeicher. Ein stärkeres Frontier-Modell darf den Aufbau des Kontexts begrenzt verändern. [tweet-2113509229298602311](../sources/tweet-2113509229298602311.md)

## Ergebnisse und Grenzen (Stand 2026-10)

Laut Abstract: bis zu 59,7 % relative Verbesserung gegenüber dem Basismodell (ALFWorld, ScienceWorld, SearchQA; Qwen3-8B und 14B), die Kontext-Evolution bringt bis zu 44,7 % obendrauf. Das sind Autorangaben aus dem Abstract; Volltext, Baselines und Reproduktion wurden nicht gelesen. [tweet-2113509229298602311](../sources/tweet-2113509229298602311.md)
