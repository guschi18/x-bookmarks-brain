---
tags: [agents, tools, research]
sources: [tweet-2052474052841984110.md]
created: 2026-10-13
updated: 2026-10-13
---

# TinyFish

## Gezeigter Workflow (Stand 2026-05)

Der Autor berichtet, OpenClaw- und Hermes-Agenten auf TinyFish umgestellt zu haben. Die visuell geprüften Videoframes zeigen Search plus Fetch als Standard: Suchtreffer liefern Titel, URLs, Ausschnitte und Rangfolge, Fetch liest anschließend die Originalseiten. [tweet-2052474052841984110](../sources/tweet-2052474052841984110.md)

Die gezeigte Fallback-Reihenfolge nutzt eingebautes `web_search` beziehungsweise `web_extract`, wenn TinyFish ausfällt oder Gemini-Grounding benötigt wird, und Brave zuletzt. Das ist eine persönliche Konfiguration, keine allgemeine Qualitätsrangliste. [tweet-2052474052841984110](../sources/tweet-2052474052841984110.md)

## GitHub-Nachtrag und MCP-Zugang (Stand 2026-10-13)

Der Nutzer ergänzte die [GitHub-Organisation tinyfish-io](https://github.com/tinyfish-io). Als konkrete Einstiege wurden bei der Primärquellenprüfung [tinyfish-mcp-server](https://github.com/tinyfish-io/tinyfish-mcp-server) und das [Cookbook mit Beispielanwendungen](https://github.com/tinyfish-io/tinyfish-cookbook) ermittelt; diese Nachträge stammen nicht aus dem ursprünglichen Tweet. [tweet-2052474052841984110](../sources/tweet-2052474052841984110.md)

Die aktuell gelesene MCP-README empfiehlt für Remote-HTTP-Clients den gehosteten Endpunkt `https://agent.tinyfish.ai/mcp`. Das npm-Paket `@tiny-fish/mcp` ist ein lokaler Proxy zum gehosteten Dienst, keine selbst gehostete Suchmaschine. [tweet-2052474052841984110](../sources/tweet-2052474052841984110.md)

Für API-Key-Zugriff dokumentiert die README Node.js ab 22, `npx @tiny-fish/mcp`, die Umgebungsvariable `TINYFISH_API_KEY` und den lokalen HTTP-Endpunkt `http://127.0.0.1:3711/mcp`. Der Prozess muss separat laufen; lokale Prozesse können den Zugang nutzen und kostenpflichtige Aufträge auslösen. [tweet-2052474052841984110](../sources/tweet-2052474052841984110.md)

## Preise und Grenzen (Stand 2026-10-13)

Die am 13.10.2026 gelesene [Preisseite](https://www.tinyfish.ai/pricing) nennt Search kostenlos mit 30 Anfragen pro Minute und 500 pro Stunde sowie Fetch kostenlos mit 150 URLs pro Minute und 1.000 pro Tag. Agent kostet 0,016 Dollar pro Schritt, Browser 0,002 Dollar pro Minute. Die pauschale Aussage des Mai-Posts über 0 Dollar gilt damit nicht für sämtliche Produkte oder unbegrenzte Nutzung. [tweet-2052474052841984110](../sources/tweet-2052474052841984110.md)

Die Fallbacks wurden visuell aus der Demo gelesen; Durchsatz, Ergebnisse und Integration wurden hier nicht praktisch getestet. [tweet-2052474052841984110](../sources/tweet-2052474052841984110.md)
