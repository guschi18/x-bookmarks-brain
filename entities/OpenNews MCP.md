---
tags: [tools, agents, trading, crypto]
sources: [tweet-2098179105191497755.md]
created: 2026-10-09
updated: 2026-10-09
---

# OpenNews MCP

## Datenzugriff (Stand 2026-09)

[6551Team/opennews-mcp](https://github.com/6551Team/opennews-mcp) beschreibt einen MIT-lizenzierten MCP-Client für den 6551-Dienst. Die gespeicherte README nennt 85+ Echtzeitquellen: News, Listings, OnChain, Meme, Market und Prediction. Ein Token von https://6551.io/mcp ist erforderlich; ein offener Client bedeutet nicht unabhängige lokale Bereitstellung aller Daten. [tweet-2098179105191497755](../sources/tweet-2098179105191497755.md)

## Setup und Abfragen (Stand 2026-09)

Für [Claude Code](Claude%20Code.md) nennt die Anleitung `claude mcp add opennews -e OPENNEWS_TOKEN=<your-token> -- uv --directory /path/to/opennews-mcp run opennews-mcp`. Umgebungsvariablen haben Vorrang vor config.json; Standard-REST-Ziel ist ai.6551.io. Für OpenClaw wird der mitgelieferte Skill kopiert. [tweet-2098179105191497755](../sources/tweet-2098179105191497755.md)

Werkzeuge erschließen Quellen, suchen Nachrichten nach Wort, Coin, Quelle und Kategorie und kombinieren Filter. Weitere dokumentierte Abfragen betreffen Unternehmen, Filings, Transkripte, Marktereignisse, US-House-PTR und verzögerte SEC-13F-Offenlegungen sowie OnChain-Holdings. Diese Offenlegungen sind keine aktuelle Gesamtpositionsliste einer Institution. [tweet-2098179105191497755](../sources/tweet-2098179105191497755.md)

## Ratings, Streams und Strategien (Stand 2026-09)

Der Hersteller beschreibt Scores von 0 bis 100 und long/short/neutral-Signale pro Coin; der oberste aiRating.score ist der höchste Coin-Score. WebSocket news.subscribe filtert news.update und news.ai_update. Strategiehits werden dem authentifizierten Eigentümer separat zugestellt; get_strategy_list/get_strategy_hits liefern Strategiehistorie. Die README nennt dafür ein geeignetes Abo und für den Push Max; diese Bedingungen sind gespeicherter Stand, kein aktueller Tarifvergleich. [tweet-2098179105191497755](../sources/tweet-2098179105191497755.md)

## Einordnung und Evidenzgrenze (Stand 2026-09)

[Awesome Trading Agents](Awesome%20Trading%20Agents.md) verlinkt das Repository bereits als Datenressource. Diese Bedienquelle ergänzt konkrete Abfragen und Streamformate, liefert aber keinen Backtest oder unabhängigen Nachweis für die Verlässlichkeit der Ratings und Handelssignale. Quellenzahlen und Datenumfang sind Herstellerangaben; nicht alle Einträge der langen Tabelle sind eigenständig datiert. [tweet-2098179105191497755](../sources/tweet-2098179105191497755.md)
