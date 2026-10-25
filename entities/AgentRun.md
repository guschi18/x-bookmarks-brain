---
tags: [agents, tools]
sources: [tweet-2102061534956662818.md]
created: 2026-10-25
updated: 2026-10-25
---

# AgentRun

## Ursprünglicher Post und Kostenchart (Stand 2026-09)

AJ Asver beschreibt ein Harness, das wiederkehrende Arbeit von LLM-Aufrufen in Code überführt und [Jev](Jev.md) für Entscheidungen nutzt. Er behauptet über 290.000 gegenüber unter 26.000 USD für 100.000 Compliance-Alerts. Der Chart zeigt rund 1.000 Alerts mit 50 Alerts je Datenpunkt, vier akzeptierte Workflow-Versionen und 2,95 → 0,25 USD pro Alert. [tweet-2102061534956662818](../sources/tweet-2102061534956662818.md)

Die beiden Originalziele agent.run und der X-Artikel sind nicht abrufbar. Das Bild belegt den dargestellten Autorenvergleich, weder gleiche Prüfqualität noch einen reproduzierbaren Vollkostenbenchmark. Der Ingest dieser verfügbaren Inhalte wurde mit der dokumentierten Quellenlücke freigegeben; siehe [AI Coding Cost Claims](../concepts/AI%20Coding%20Cost%20Claims.md). [tweet-2102061534956662818](../sources/tweet-2102061534956662818.md)

*Bildhinweis: AgentRun-Kostenchart: 50 Alerts je Punkt, vier Workflow-Versionen (Bild nicht mitgeliefert).* [tweet-2102061534956662818](../sources/tweet-2102061534956662818.md)

## Ergänzende Repo-Recherche (Stand 2026-10-25)

Die [commitgebundene README](https://github.com/Parcha-ai/agentrun/blob/d05c778a48cd34b3a49d8dac51eaec5d3a8ea26a/README.md) von [Parcha-ai/agentrun](https://github.com/Parcha-ai/agentrun) beschreibt explizite Workflows mit [Jev](Jev.md)-Urteilen, Code und Agenten-Fallback. Der Host behält Tools, Modellzugang, Rechte und Budget. Das ist eine spätere Primärquelle, kein rekonstruierter Septemberartikel. [tweet-2102061534956662818](../sources/tweet-2102061534956662818.md)

JSON oder TypeScript/Zod definieren Schemas und Abläufe; der Interpreter prüft Zwischenzustände. Adapterschnittstellen heißen runEffect, runNode und runJudge. Die Struktur ist verwandt mit [Agent Workflow Graphs](../concepts/Agent%20Workflow%20Graphs.md) und [Typed Decision Layer](../concepts/Typed%20Decision%20Layer.md). [tweet-2102061534956662818](../sources/tweet-2102061534956662818.md)

Der Einstieg lautet npm install @parcha/agentrun-dsl@beta und npx @parcha/agentrun-dsl@beta demo, bei Node ab 22.19. Die Demo verwendet geskriptete Antworten; Live-Jev benötigt einen eigenen API-Key. [tweet-2102061534956662818](../sources/tweet-2102061534956662818.md)

Das Supportbeispiel verlangt Antwort und Quelle, anschließend yes mit mindestens 0,8 Konfidenz. Sonst folgt ein Agentenversuch, danach erneute Prüfung oder Eskalation. Der Schwellwert ist Beispielkonfiguration, kein Richtigkeitsnachweis. [tweet-2102061534956662818](../sources/tweet-2102061534956662818.md)

Neben DSL, Jev-Adapter und Pi-Anbindung dokumentiert das aktuelle Repo Erweiterungen für Browser, Vision, Transport, persistente Agenten und Lernen; das Referenz-Harness ist als nicht veröffentlicht markiert. Code-Knoten haben Prozessrechte und brauchen für fremde Workflows Host-Isolation. Die Demos belegen keine Live-Kostenersparnis; nichts wurde installiert oder ausgeführt. [tweet-2102061534956662818](../sources/tweet-2102061534956662818.md)
