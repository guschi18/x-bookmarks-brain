---
tags: [agents, tools]
sources: [tweet-2108591328732856655.md, tweet-2109336873449455883.md]
created: 2026-10-12
updated: 2026-10-24
---

# Claude Managed Agents

## Dynamic Workflows (Stand 2026-10)

ClaudeDevs kündigt Dynamic Workflows für Claude Managed Agents am 09.10.2026 als öffentliche Beta an. Ein Lead-Agent erstellt einen Plan, lässt mehrere Agenten in Phasen arbeiten und kombiniert abschließend deren Ergebnisse. Das ist eine Herstellerankündigung, keine hier getestete Orchestrierung. [tweet-2108591328732856655](../sources/tweet-2108591328732856655.md)

## Mechanismus und Quellenlage (Stand 2026-10)

Die am 12.10.2026 ergänzend gelesene [offizielle Orchestrierungsdokumentation](https://platform.claude.com/docs/en/managed-agents/multiagent-orchestration) unterscheidet Delegation an Subagents von Dynamic Workflows: Bei letzteren schreibt der Agent ein Programm, das viele Agenten im Hintergrund ausführt und deren Rückgaben zusammenführt. Dieser aktuelle Doku-Nachtrag ist nicht als Artikel in Raw gespeichert. [tweet-2108591328732856655](../sources/tweet-2108591328732856655.md)

Die Erweiterung konkretisiert [Agent Workflow Graphs](../concepts/Agent%20Workflow%20Graphs.md) als Produktfunktion. Der Tweet nennt keine Einrichtung, Kosten oder belastbaren Vergleich; das gespeicherte Demo-Video hat kein Transkript und wurde visuell nicht geprüft. [tweet-2108591328732856655](../sources/tweet-2108591328732856655.md)

## Cookbook zum Lernen (Stand 2026-10)

Daniel San (dani_avila7) veröffentlicht https://github.com/davila7/claude-managed-agents-cookbook mit sieben Modulen: Basics, Multi-Turn, Tools und Permissions, Files, Session Control, Subagents, Dynamic Workflows. Jedes Modul gibt es als Python-SDK-Notebook und als CLI-Variante mit `ant`. [tweet-2109336873449455883](../sources/tweet-2109336873449455883.md)

Die Notebooks rufen die echte API auf und kosten Geld: Module 01-05 laut README je wenige Cent, Module 06 und 07 laufen mit Budgetgrenzen von $3 und $5 pro Session. Zwei PDF-Guides (Englisch, Spanisch) liegen im Repo. Drittanbieter-Material, kein Anthropic-Dokument; die Kostenangaben sind nicht nachgemessen. [tweet-2109336873449455883](../sources/tweet-2109336873449455883.md)
