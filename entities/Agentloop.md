---
tags: [agents, tools]
sources: [tweet-2114392468313563567.md]
created: 2026-10-27
updated: 2026-10-27
---

# Agentloop

## Überblick (Stand 2026-10)

agentloop (github.com/smhanov/agentloop) ist laut README eine Go-Bibliothek für den Tool-Calling-Loop jedes Agenten: Prompt senden, angeforderte Tool-Aufrufe ausführen, Ergebnisse zurückgeben, bis eine Endantwort entsteht. Dazu kommen Budgets, Hooks, Skills und Tracing. Autor smhanov destillierte nach eigener Angabe Erkenntnisse aus openclaw, hermes, crush, piclaw und dem DeepSeek-Harness. [tweet-2114392468313563567](../sources/tweet-2114392468313563567.md)

## Eigenschaften laut README (Stand 2026-10)

- Anbieterzugriff über das Schwesterprojekt llmhub (OpenAI, Anthropic, Gemini, Ollama, xAI, OpenRouter, Z.AI oder eigener Provider). [tweet-2114392468313563567](../sources/tweet-2114392468313563567.md)
- Begrenzungen je Lauf: Tool-Call-Budgets, Inferenz-Obergrenzen, Erkennung doppelter Aufrufe, Stream-Watchdogs und context.Context. [tweet-2114392468313563567](../sources/tweet-2114392468313563567.md)
- Hooks-Struktur für Logging, Streaming-UIs, Freigabe-Gates, Kostenlimits, Steuerung und Kontextkompression. [tweet-2114392468313563567](../sources/tweet-2114392468313563567.md)
- Skills als Ordner mit kleinem Katalog, bei Bedarf über ein abgeschottetes Lese-Tool geladen. [tweet-2114392468313563567](../sources/tweet-2114392468313563567.md)
- Jeder Aufruf liefert Endtext plus vollständigen Trace mit Tool-Ausgaben, Dauer, Transkript und Token-/Kosten. [tweet-2114392468313563567](../sources/tweet-2114392468313563567.md)
- Statisches Binary (CGO_ENABLED=0), etwa 7 MB RAM; Installation per go get github.com/smhanov/agentloop. [tweet-2114392468313563567](../sources/tweet-2114392468313563567.md)
- Zwei Referenz-Agenten: Suchagent über serper und Coding-Agent nach mini-swe-agent. [tweet-2114392468313563567](../sources/tweet-2114392468313563567.md)

## Grenzen

Alle Angaben sind Projektbeschreibung des Autors; nichts wurde installiert oder gemessen. Die Aussage zu mehreren Firmen mit 10.000 $ MRR auf einem 20-$-Stack ist ein Autorenclaim ohne Beleg. Ein begleitendes Buch (Building AI Agents from Scratch) wird verlinkt. Verwandt: [Agentic Engineering](../concepts/Agentic%20Engineering.md). [tweet-2114392468313563567](../sources/tweet-2114392468313563567.md)
