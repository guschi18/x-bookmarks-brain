---
tags: [agents, tools, trading, research]
sources: [tweet-2098410941104677108.md, tweet-2098179105191497755.md]
created: 2026-10-08
updated: 2026-10-09
---

# Awesome Trading Agents

## Katalog und Auswahl (Stand 2026-09)

[LLMQuant/awesome-trading-agents](https://github.com/LLMQuant/awesome-trading-agents) sammelt öffentlich verfügbare LLM-Projekte für Marktrecherche, Handelsentscheidungen und Werkzeuganbindung. Die README trennt Agents, MCPs und Skills; klassische Quant-Bibliotheken, reine Zeitreihenmodelle und RL-Bots gehören nicht zum Kern. Auswahlkriterien sind öffentliche Artefakte, sichtbares LLM-Verhalten, Aktivität, Dokumentation und eine unterscheidbare Rolle. [tweet-2098410941104677108](../sources/tweet-2098410941104677108.md)

## Agenten und Evaluierungen (Stand 2026-09)

Als Agenten-Einstieg nennt der Katalog [TradingAgents](TradingAgents.md) mit Analysten-/Debattenrollen, [virattt/ai-hedge-fund](https://github.com/virattt/ai-hedge-fund) mit Investor-Personas und [HKUDS/AI-Trader](https://github.com/HKUDS/AI-Trader) mit Skill-basierter Agentenregistrierung. Weitere Kategorien sind Single-Agent-Trader, Research-Copilots, Echtgeldexperimente, Prediction Markets und Strategiecode. Diese Kurzbeschreibungen sind Katalogangaben, keine eigenen Funktionsprüfungen. [tweet-2098410941104677108](../sources/tweet-2098410941104677108.md)

Für Evaluierungen verlinkt die README [live-trade-bench](https://github.com/ulab-uiuc/live-trade-bench), [AgenticTrading](https://github.com/Open-Finance-Lab/AgenticTrading), [vals-ai/finance-agent](https://github.com/vals-ai/finance-agent) und [DeepFund](https://github.com/HKUSTDial/DeepFund). Das Echtgeldexperiment [LLM-Trading-Lab](https://github.com/LuckyOne7777/LLM-Trading-Lab) und Strategie-Evolution mit [pwb-alphaevolve](https://github.com/paperswithbacktest/pwb-alphaevolve) sind eigene Ressourcenarten, keine Garantie zukünftiger Renditen. [tweet-2098410941104677108](../sources/tweet-2098410941104677108.md)

## Daten, Ausführung und Skills (Stand 2026-09)

Datenzugriff: [financial-datasets/mcp-server](https://github.com/financial-datasets/mcp-server) für Fundamentaldaten, Kurse und Nachrichten, [LLMQuant/data-mcp](https://github.com/LLMQuant/data-mcp) für Quant-Recherche und Marktdaten sowie [sec-edgar-mcp](https://github.com/stefanoamorelli/sec-edgar-mcp) für Filings. Handelsausführung: [Alpaca MCP](https://github.com/alpacahq/alpaca-mcp-server), [Kraken CLI](https://github.com/krakenfx/kraken-cli), [OKX Agent Trade Kit](https://github.com/okx/agent-trade-kit) und [IB_MCP](https://github.com/rcontesti/IB_MCP). Paper Trading ist separat etwa über [polymarket-paper-trader](https://github.com/agent-next/polymarket-paper-trader) aufgeführt. [tweet-2098410941104677108](../sources/tweet-2098410941104677108.md)

Wiederverwendbare Workflows: [claude-trading-skills](https://github.com/tradermonty/claude-trading-skills) für US-Aktienanalyse und Alpaca-Portfolios, [finance-skills](https://github.com/himself65/finance-skills) für mehrere Assetklassen, [vectorbt-backtesting-skills](https://github.com/marketcalls/vectorbt-backtesting-skills) für Backtests und [trading_skills](https://github.com/staskh/trading_skills) für Options-/Portfolioarbeit. Die README markiert passende MCP-/Skill-Paarungen. [tweet-2098410941104677108](../sources/tweet-2098410941104677108.md)

## Verhältnis zu anderen Katalogen und Grenzen (Stand 2026-09)

[Awesome Finance MCP](Awesome%20Finance%20MCP.md) ist ein verwandter Werkzeugkatalog; diese Sammlung ergänzt die Recherche um vollständige Agentensysteme, Experimente, Benchmarks und Strategieentwicklung. Die 195 gespeicherten strukturierten Links bleiben vollständig auf der Source erhalten; diese Seite ist eine Auswahl von Einstiegen. [tweet-2098410941104677108](../sources/tweet-2098410941104677108.md)

Projektstatus und Kurzbeschreibungen stammen aus der gespeicherten README, deren Einträge nicht einzeln datiert sind. Weder gelistete Server noch Strategien wurden hier ausgeführt, und die Aufnahme in den Katalog ist kein Nachweis von Profitabilität oder verlässlicher Handelsausführung. [tweet-2098410941104677108](../sources/tweet-2098410941104677108.md)

## OpenNews-Bedienquelle (Stand 2026-09)

[OpenNews MCP](OpenNews%20MCP.md) ergänzt den bereits im Katalog verlinkten Server um eine vollständige Setup- und API-Quelle: Tokenzugriff, Nachrichtenfilter, Coin-Scores, WebSocket-Updates und Strategiehistorie. Die angegebenen 85+ Quellen und long/short/neutral-Signale sind Herstellerangaben ohne gespeicherten Backtest; die ältere Bedienquelle ersetzt keinen neueren Katalogstand. [tweet-2098179105191497755](../sources/tweet-2098179105191497755.md)
