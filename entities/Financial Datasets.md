---
tags: [tools, trading, research]
sources: [tweet-2053048136294440961.md]
created: 2026-10-13
updated: 2026-10-13
---

# Financial Datasets

## Rolle und Zugang (Stand 2026-05)

Financial Datasets stellt laut gespeicherter Herstellerdokumentation Kurse, Finanzberichte, SEC-Filings und Nachrichten über einen MCP-Server bereit; der Post zeigt die Nutzung mit [Claude Code](Claude%20Code.md). [tweet-2053048136294440961](../sources/tweet-2053048136294440961.md)

## Einrichtung mit Claude Code (Stand 2026-05; bestätigt 2026-10-13)

Der folgende Ablauf aus dem Post ist auch in der am 13.10.2026 gelesenen [Herstellerdokumentation](https://docs.financialdatasets.ai/mcp-server#claude-code) enthalten: [tweet-2053048136294440961](../sources/tweet-2053048136294440961.md)

```sh
claude mcp add --transport http financial-datasets https://mcp.financialdatasets.ai/
```

Anschließend in Claude Code `/mcp` aufrufen, im Browser per OAuth anmelden und die Verbindung mit `claude mcp list` prüfen. Interaktive Clients benötigen laut Dokumentation keinen manuell eingetragenen API-Key. [tweet-2053048136294440961](../sources/tweet-2053048136294440961.md)

Für Skripte und eigene MCP-Integrationen nennt die Dokumentation dagegen `https://mcp.financialdatasets.ai/api` mit einem API-Key aus dem [Konto-Dashboard](https://financialdatasets.ai/). OAuth und API-Key sind unterschiedliche Zugangswege. [tweet-2053048136294440961](../sources/tweet-2053048136294440961.md)

## Beispiele und Aussagegrenzen (Stand 2026-05)

Die Beispielaufgaben fragen nach Apples KGV und Marktkapitalisierung, Teslas letzten vier Quartalsberichten und Bitcoins Kursentwicklung. Die visuell geprüfte Demo fragt NVDA-Analystenschätzungen ab; sie zeigt einen Datenzugriff, keine geprüfte Prognosequalität. [tweet-2053048136294440961](../sources/tweet-2053048136294440961.md)

Die 17.000+ Aktien, der 60-Sekunden-Aufwand und die Gleichsetzung mit einem Bloomberg Terminal sind Werbeaussagen des Posts. Das Setup wurde hier nicht installiert; Zugang ohne eigenen API-Key bedeutet keine bestätigte kostenlose Datennutzung. [tweet-2053048136294440961](../sources/tweet-2053048136294440961.md)
