---
tags: [trading, crypto, tools]
sources: [tweet-2062422541512179871.md]
created: 2026-09-30
updated: 2026-09-30
---

# Polymarket Trading Bot

## Projekt und dokumentierter Betrieb

https://github.com/MrFadiAi/Polymarket-bot dokumentiert v3.1 als automatisierten Trading-Bot mit Dashboard für Polymarket. Die README nennt Node.js ab 18, Wallet-Zugang und einen privaten Schlüssel; ihr Einstieg verwendet DRY_RUN=true. Dies beschreibt den gespeicherten Projektstand, keine geprüfte Betriebsbereitschaft. [tweet-2062422541512179871](../sources/tweet-2062422541512179871.md)

## Strategien

Die README beschreibt Kauf beider Marktseiten bei YES+NO unter 1 Dollar, DipArb für abrupte Kursrückgänge in kurzen Kryptomärkten, Copy-Trading gefilterter Trader und direkte Orders mit FOK, Stop-Loss und Take-Profit. Sie bezeichnet Arbitrage als garantierten mathematischen Gewinn, liefert aber keine Ausführungsdaten. [tweet-2062422541512179871](../sources/tweet-2062422541512179871.md)

## Risikogrenzen laut README

Täglicher Verlust von 5 % soll eine 60-minütige Pause auslösen, monatlich 15 % eine 30-tägige Pause, 25 % Drawdown eine siebentägige Pause und 40 % Gesamtverlust einen Halt bis zum manuellen Neustart. Die Kapitalvariable ist laut Anleitung das Risikobudget, nicht der Wallet-Saldo. [tweet-2062422541512179871](../sources/tweet-2062422541512179871.md)

Die Basisposition beträgt laut README 2 % des Kapitals; Verlustserien reduzieren und Gewinnserien erhöhen sie bis höchstens 5 %. Traderfilter verlangen unter anderem 60 % Gewinnquote, Profit Factor 1,5 und Konsistenz. Die Beispiele der README sind nicht durch Trades oder Tests belegt. [tweet-2062422541512179871](../sources/tweet-2062422541512179871.md)

## Grenzen

Es fehlen Codeprüfung, Backtest und Live-Ergebnisse. Die beworbene garantierte Exit-Fähigkeit ab 1,50 Dollar sowie Risikoklassifikationen bleiben Projektbehauptungen; die README selbst schließt eine Profitgarantie aus. [tweet-2062422541512179871](../sources/tweet-2062422541512179871.md)
