---
tags: [tools, agents]
sources: [tweet-2114401602450706524.md]
created: 2026-10-27
updated: 2026-10-27
---

# Chrome DevTools MCP

## Überblick (Stand 2026-10)

chrome-devtools-mcp (Repo ChromeDevTools/chrome-devtools-mcp) lässt Coding-Agenten wie Claude, Cursor oder Copilot einen laufenden Chrome steuern und inspizieren. Es gibt ihn als MCP-Server und als CLI. [tweet-2114401602450706524](../sources/tweet-2114401602450706524.md)

## Fähigkeiten laut README (Stand 2026-10)

- Performance: Traces aufzeichnen und Einsichten ableiten. [tweet-2114401602450706524](../sources/tweet-2114401602450706524.md)
- Debugging: Netzwerkanfragen, Screenshots und Konsolenmeldungen mit Source-Map-Stacktraces. [tweet-2114401602450706524](../sources/tweet-2114401602450706524.md)
- Automation über puppeteer mit automatischem Warten auf Ergebnisse. [tweet-2114401602450706524](../sources/tweet-2114401602450706524.md)
- Laut Tweet analysiert das neueste Update Heap-Snapshots ohne Live-Chrome-Verbindung, etwa für Speicherlecks. [tweet-2114401602450706524](../sources/tweet-2114401602450706524.md)

## Installation laut Tweet

`/plugin marketplace add ChromeDevTools/chrome-devtools-mcp`, danach `/plugin install chrome-devtools-mcp@chrome-devtools-plugins`. [tweet-2114401602450706524](../sources/tweet-2114401602450706524.md)

## Grenzen und Risiken

Die README warnt: Der MCP-Client sieht Inhalte der Browserinstanz und kann Daten in Browser und DevTools ändern; sensible Daten nicht teilen. Offiziell unterstützt sind nur Chrome und Chrome for Testing. Performance-Tools können Trace-URLs an die CrUX-API senden (abschaltbar mit `--no-performance-crux`); Nutzungsstatistik ist standardmäßig an (abschaltbar mit `--no-usage-statistics`). Die Empfehlung "immer installieren" ist eine Einzelmeinung des Tweet-Autors. Verwandt: [Claude Code](Claude%20Code.md). [tweet-2114401602450706524](../sources/tweet-2114401602450706524.md)
