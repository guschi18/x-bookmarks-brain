---
tags: [agents, trading, tools]
sources: [tweet-2104899490151092254.md]
created: 2026-10-06
updated: 2026-10-20
---

# Minara

## Rolle im gespeicherten Experiment (Stand 2026-09)

Der gesponserte Artikel stellt Minara als Daten-, Coding-, Backtest- und Ausführungsumgebung für [Claude Opus 5.5](Claude%20Opus%205.5.md) dar. Er nennt Chat, Markets, Strategy Studio, Data Studio, Automations und einen Strategie-Marketplace; die Integration und der Betrieb wurden hier nicht getestet. [tweet-2104899490151092254](../sources/tweet-2104899490151092254.md)

## Research und Akzeptanzkriterien (Stand 2026-09)

Erst Sektoren auf relative Stärke, Momentum und Katalysatoren untersuchen, ohne bereits eine Strategie zu empfehlen. Danach vier verschiedene Hypothesen mit Universum, Sizing, Entry/Exit, Rebalance, Kosten und vermutetem Edge spezifizieren. [tweet-2104899490151092254](../sources/tweet-2104899490151092254.md)

Vor Optimierung festlegen: SPY nach Kosten im letzten Jahr schlagen, doppelte Gebühren und Slippage überstehen, Drawdown unter 30 Prozent, Sharpe über 1,0, keine Aktie mit mehr als 40 Prozent Renditebeitrag sowie identische Ergebnisse bei zwei Läufen. [tweet-2104899490151092254](../sources/tweet-2104899490151092254.md)

Der Artikel berichtet fünf verworfene Varianten und anschließend einen Faktor-Mix aus Momentum, idiosynkratischem Risiko und Cashflow-Qualität mit Gewichten 60/25/15. Der vollständige Python-Code und die Research-Prompts stehen in der Source. [tweet-2104899490151092254](../sources/tweet-2104899490151092254.md)

## Prüfung und wiederkehrende Arbeit (Stand 2026-09)

Der vorgeschlagene Gegencheck lautet, die Strategie als überangepasst zu behandeln und Fehlerbedingungen zu suchen: doppelte Kosten, wiederholte Läufe, Entfernung der stärksten Aktie und verschiedene Marktphasen. Ein Wochenprompt prüft Sektoren, erzeugt drei Hypothesen und meldet nur Varianten, die alle Kriterien überstehen. Das ergänzt [LLM Autoresearch Loop](../concepts/LLM%20Autoresearch%20Loop.md). [tweet-2104899490151092254](../sources/tweet-2104899490151092254.md)

## Grenzen und verwandte Quelle (Stand 2026-09)

Die behaupteten Backtest-Ergebnisse, Sharpe 1,36 und Zeitersparnis sind nicht unabhängig reproduziert; weder ein abgetrennter Out-of-Sample-Test noch Live-Ertrag sind hier belegt. Gleiche Wiederholungsergebnisse prüfen Determinismus, nicht Überanpassung. [tweet-2104899490151092254](../sources/tweet-2104899490151092254.md)

Das beigefügte Bild zeigt ein anderes Projekt: [TradingAgents](TradingAgents.md) mit spezialisierten Analyse-, Bull-/Bear-, Risiko- und Traderrollen; sein Abstract nennt https://github.com/TauricResearch/TradingAgents. Der Screenshot belegt keine Gleichsetzung dieses Frameworks mit Minara. [tweet-2104899490151092254](../sources/tweet-2104899490151092254.md)
