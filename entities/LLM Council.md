---
tags: [agents, tools]
sources: [tweet-2086850058021196072.md]
created: 2026-10-12
updated: 2026-10-12
---

# LLM Council

## Implementierung (Stand 2026-08; gespeicherte README)

[karpathy/llm-council](https://github.com/karpathy/llm-council) ist eine lokale Web-App, die eine Anfrage über OpenRouter an mehrere Modelle sendet. Sie konkretisiert den unter [Practical LLM Usage](../concepts/Practical%20LLM%20Usage.md) vorhandenen Grundsatz, mehrere Anbieter zu befragen, als dreistufigen Ablauf. [tweet-2086850058021196072](../sources/tweet-2086850058021196072.md)

## Drei Stufen

Zuerst beantworten alle Council-Modelle die Frage unabhängig; die Oberfläche zeigt ihre Ergebnisse in getrennten Tabs. Danach erhält jedes Modell anonymisierte Antworten der anderen und bewertet Genauigkeit und Einsicht. Ein festgelegtes Chairman-Modell fasst abschließend die Antworten zusammen. Anonymisierung soll Bevorzugung bestimmter Modellnamen reduzieren, garantiert aber keine korrekten Urteile. [tweet-2086850058021196072](../sources/tweet-2086850058021196072.md)

## Betrieb

Die README nennt FastAPI/Python 3.10+, async httpx, React/Vite und lokale JSON-Konversationen. Ein OPENROUTER_API_KEY und kostenpflichtige Credits sind nötig; backend/config.py legt Council und Chairman fest. uv verwaltet Python, npm das Frontend; die Oberfläche läuft auf localhost:5173. Die gespeicherten Modellnamen sind Konfigurationsbeispiele dieses README-Stands, keine aktuelle Modellwahlempfehlung. [tweet-2086850058021196072](../sources/tweet-2086850058021196072.md)

## Grenzen

Karpathy bezeichnet das Projekt ausdrücklich als weitgehend vibegecodeten Saturday-Hack, stellt es ohne Support bereit und kündigt keine Pflege an. Fioravantis Behauptung großer Wirkung in komplexen Domänen ist keine Evaluation; zusätzliche Antworten und Bewertungsrunden erzeugen zusätzliche API-Arbeit, ohne einen garantierten Qualitätsgewinn zu belegen. [tweet-2086850058021196072](../sources/tweet-2086850058021196072.md)
