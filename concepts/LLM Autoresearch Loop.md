---
tags: [agents, research, trading]
sources: [tweet-2071435350065532941.md, tweet-2104899490151092254.md]
created: 2026-09-29
updated: 2026-10-06
---

# LLM Autoresearch Loop

## Mechanismus

Im [Auto-Quant](../entities/Auto-Quant.md)-Beispiel erhält ein LLM-Agent eine begrenzte Strategiedatei als Arbeitsraum und einen festgelegten FreqTrade-Backtest als Prüfung. Er erzeugt Varianten, liest Kennzahlen, hält oder verwirft Änderungen und protokolliert Entscheidungen in results.tsv. [tweet-2071435350065532941](../sources/tweet-2071435350065532941.md)

## Voraussetzungen und Grenze

Konfiguration, Datenvorbereitung und Backtest-Code sollen während der Agenteniteration fest bleiben; sonst ist die Auswertung nicht vergleichbar. Die README zeigt zugleich, wie eine reine Sharpe-Optimierung durch Kennzahlentricks fehlleiten kann. Backtests bleiben historische Experimente und beweisen keinen Live-Ertrag. [tweet-2071435350065532941](../sources/tweet-2071435350065532941.md)

## Vorab definierte Backtest-Kriterien (Stand 2026-09)

Das [Minara](../entities/Minara.md)-Beispiel definiert vor Optimierung Benchmarkrendite nach Kosten, verdoppelte Kosten, Drawdown, Sharpe, Konzentration und Determinismus als Akzeptanzkriterien und protokolliert verworfene Varianten. Die vorgestellten Stresschecks und Prompts sind direkt nachvollziehbare Verfahrensvorgaben; die berichteten Resultate bleiben gesponserte Autorenangaben ohne unabhängig reproduzierten Live-Ertrag. [tweet-2104899490151092254](../sources/tweet-2104899490151092254.md)
