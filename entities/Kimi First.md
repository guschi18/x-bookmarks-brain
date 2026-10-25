---
tags: [agents, tools]
sources: [tweet-2077826623320023303.md]
created: 2026-10-01
updated: 2026-10-01
---

# Kimi First

## Rollen und Herkunft (Stand 2026-07)

Die gespeicherte README https://github.com/boringmarketer/kimi-first beschreibt einen [Claude Code](Claude%20Code.md)-Skill, der feste Implementierungsaufträge an Kimi Code CLI/k3 übergibt. Claude behält Spec, Architektur, Review und Merge; Kimi bearbeitet etwa Migrationen, Testergänzungen und CI-Reparaturen. Der Skill ist ein Port von https://github.com/steipete/agent-scripts/blob/main/skills/codex-first/SKILL.md. [tweet-2077826623320023303](../sources/tweet-2077826623320023303.md)

## Übergabe und unabhängige Prüfung (Stand 2026-07)

Ein temporärer Auftragstext enthält Ziel, Pfade, Grenzen, Nichtziele und verlangte Belege, weil Kimi ohne Elternkontext startet. Nach kimi -p prüft Claude vollständigen Diff und Tests selbst; nach zwei erfolglosen Runden übernimmt Claude. Design, winzige Änderungen, Produktionseingriffe und Review werden laut README nicht delegiert. [tweet-2077826623320023303](../sources/tweet-2077826623320023303.md)

## CLI- und Evidenzgrenzen (Stand 2026-07)

Die README berichtet Tests mit CLI v0.26.0: headless -p genehmigt Tool Calls automatisch, --yolo wird damit nicht kombiniert und --continue nimmt die letzte Sitzung desselben Arbeitsverzeichnisses auf. Daher verlangt sie Repositories ohne erreichbare Produktionsgeheimnisse und keine konkurrierenden Sessions im gleichen Verzeichnis. [tweet-2077826623320023303](../sources/tweet-2077826623320023303.md)

Pauschale Kimi-3-/Opus-Benchmarks, Sonnet-5-Preise und Flat-Rate-Kostenvorteile sind hier nicht gemessen. Das Artefakt belegt den Rollenvertrag, nicht einen universellen Modellgewinner; [Model Selection Evals](../concepts/Model%20Selection%20Evals.md) hält solche Leistungsentscheidungen an konkrete Aufgaben gebunden. [tweet-2077826623320023303](../sources/tweet-2077826623320023303.md)
