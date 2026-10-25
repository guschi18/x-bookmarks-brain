---
tags: [agents, trading, research]
sources: [tweet-2098941338297458746.md, tweet-1925945937366597694.md]
created: 2026-10-08
updated: 2026-10-25
---

# TradingAgents

## Rollen und Ablauf (Stand 2026-09)

[Repository](https://github.com/TauricResearch/TradingAgents): spezialisierten Fundamental-, Sentiment-, Nachrichten- und technischen Analysten folgen Bull-/Bear-Debatten, Trader und Risikomanagement. Ein Portfolio Manager entscheidet über Vorschläge für eine simulierte Börse. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

Die README beschreibt LangGraph, zahlreiche Cloud-LLMs und Ollama beziehungsweise OpenAI-kompatible lokale Endpunkte. Python-Nutzung: TradingAgentsGraph(config=...).propagate("NVDA", "2026-01-15"). [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## Zustand und Daten (Stand 2026-09)

Der dokumentierte v0.4.0-Stand nennt Point-in-time-/Look-ahead-Korrekturen für FRED, Social Sentiment und Entscheidungsgedächtnis. Der stets aktive Decision Log hält Entscheidungen und spätere Reflexionen fest; --checkpoint aktiviert getrennt davon Wiederaufnahme aus SQLite-Checkpoints. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

Für unterschiedliche Börsen nutzt das Werkzeug Yahoo-Finance-Ticker mit Börsensuffix; CLI und Docker lassen Datum, Anbieter und Forschungstiefe wählen. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## Evidenzgrenzen (Stand 2026-09)

Die README bezeichnet das Projekt als Forschungsgerüst. LLM-Sampling und wechselnde Live-Nachrichten können auch bei festem Analysezeitpunkt andere Resultate erzeugen; veröffentlichte Renditen werden ausdrücklich nicht garantiert. Die Struktur belegt keine profitable Strategie. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## Nutzerergänzung zu Financial Machine Learning (2026-10-25)

Der Nutzer ergänzte [TauricResearch/TradingAgents](https://github.com/TauricResearch/TradingAgents) ausdrücklich zum Bookmark des Papers Financial Machine Learning; der Forschungseinstieg steht unter [Financial Research Directory](../concepts/Financial%20Research%20Directory.md). Dies dokumentiert eine zusätzliche Ressource, keine historische Verbindung zwischen Paper und Repo. [tweet-1925945937366597694](../sources/tweet-1925945937366597694.md)
