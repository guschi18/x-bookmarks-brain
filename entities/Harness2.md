---
tags: [agents, research]
sources: [tweet-2112141663833317775.md]
created: 2026-10-23
updated: 2026-10-23
---

# Harness2

## Rolle (Stand 2026-10)

[Harness2](https://github.com/google-research/harness2) ("Recursive Agent Harnessing for an Open World") ist ein Plug-and-play-Framework von Google Research zur Optimierung des Systems um ein Modell (Prompts, Tools, Memory, Skills, Orchestrierung) bei festen Modellgewichten. Der Post enthält nur den Repository-Link. [tweet-2112141663833317775](../sources/tweet-2112141663833317775.md)

Zwei Rekursionsebenen laut README: Task-Level-Rekursion verfeinert den Ausführungs-Harness für die aktuelle Aufgabe über einen kontrastiven Propose-Probe-Compose-Schritt (Änderungen vorschlagen, ihre Wirkung an derselben Aufgabe testen, aus Verhaltenskontrasten einen verbesserten Harness komponieren), ohne Ground-Truth-Feedback. Harnessing-Level-Rekursion pflegt einen persistenten Improvement-Harness mit übernommenen Harnesses und belegten Lektionen. [tweet-2112141663833317775](../sources/tweet-2112141663833317775.md)

Acht editierbare Komponenten: System-Prompt, Guardrails, Memory, Tool-Anleitung, Subagents, Skills, Skripte und Plugins. Unterstützt werden parallele und sequenzielle Rekursion, OpenCode- und Codex-Executor sowie die Benchmarks JobBench, LAB und WorkBuddy-Bench. [tweet-2112141663833317775](../sources/tweet-2112141663833317775.md)

## Installation und Evidenzgrenzen

Benötigt Linux, Python 3.12 und uv; `harness2-demo --output runs/demo --k 2` läuft lokal ohne Modell-Zugangsdaten. Modellgestützte Benchmarks brauchen Node.js 20+, Google Cloud CLI (Vertex AI) und je nach Benchmark Pandoc, Poppler oder Docker. [tweet-2112141663833317775](../sources/tweet-2112141663833317775.md)

Die README berichtet für einen Harness2-Schritt Gewinne gegenüber den Basis-Harnesses von GLM-5 und Gemini 3.5 Flash (bis 11,5 Punkte auf WorkBuddy-Bench, 4,5 auf JobBench, 11,8 Prozentpunkte bei LAB partial pass). Das sind Angaben der Autoren; sie wurden hier nicht reproduziert und nichts wurde installiert. Verwandter Ansatz: [AutoHarness](AutoHarness.md). [tweet-2112141663833317775](../sources/tweet-2112141663833317775.md)
