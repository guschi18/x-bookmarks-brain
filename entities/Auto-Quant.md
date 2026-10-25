---
tags: [trading, crypto, agents]
sources: [tweet-2071435350065532941.md]
created: 2026-09-29
updated: 2026-09-29
---

# Auto-Quant

## Rolle und Mechanismus

[Auto-Quant](Auto-Quant.md) ist laut GitHub-README ein Prototyp, der einen [LLM Autoresearch Loop](../concepts/LLM%20Autoresearch%20Loop.md) auf FreqTrade-Kryptostrategien überträgt. Der Agent ändert Strategiedateien, lässt Backtests laufen und entscheidet anhand der Ergebnisse über Behalten, Verändern oder Verwerfen. [tweet-2071435350065532941](../sources/tweet-2071435350065532941.md)

## Dokumentierte Ergebnisse und Grenzen

Das Repository beschreibt eine Testreihe mit 99 Backtests und eine Sharpe-Grenze von 1,44 bei behaltenen Strategien. Sehr hohe Sharpe-Werte verwirft der Agent laut README als Ausnutzung der Bewertungsmetrik. Die Ergebnisse sind Projektangaben auf historischen Daten. [tweet-2071435350065532941](../sources/tweet-2071435350065532941.md)

Die README bezeichnet als Erfolgskriterium einen ausführbaren Loop mit interpretierbarer results.tsv, ausdrücklich keinen profitablen Live-Handel. Gebühren, Zeiträume und Strategiekapazität sind Teil des beschriebenen Backtest-Vertrags; realer Handel wird nicht belegt. [tweet-2071435350065532941](../sources/tweet-2071435350065532941.md)
