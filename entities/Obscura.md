---
tags: [agents, tools, security]
sources: [tweet-2094114217229946976.md]
created: 2026-10-09
updated: 2026-10-09
---

# Obscura

## Engine und Rolle (Stand 2026-08)

[h4ckf0r0day/obscura](https://github.com/h4ckf0r0day/obscura) ist laut gespeicherter README ein unabhängiger Headless-Browser in Rust mit V8 für JavaScript und eigenem Rendering. Das Projekt zielt auf Web-Scraping und Agentenautomatisierung; sein Chrome DevTools Protocol erlaubt Anbindungen über Puppeteer und Playwright, ohne Chromium zu starten. Anders als [Browser Use](Browser%20Use.md) ist dies eine Browser-Engine, nicht lediglich ein Agenten-Harness über einem bestehenden Browser. [tweet-2094114217229946976](../sources/tweet-2094114217229946976.md)

## Einrichtung und Steuerung

Die README nennt vorkompilierte Release-Archive für Linux, macOS und Windows sowie ein Docker-Image; die Windows-ZIP wird manuell entpackt. Für paralleles Scraping müssen obscura und obscura-worker zusammen im Verzeichnis bleiben. Der Quellbau benötigt Rust; Stealth-Builds zusätzlich CMake, Clang und libclang/LLVM. Die Open-Source-Engine trägt Apache-2.0. [tweet-2094114217229946976](../sources/tweet-2094114217229946976.md)

`obscura fetch https://example.com --eval "document.title"` führt eine Seitenabfrage aus; `--dump` liefert unter anderem Text, HTML, Links, Markdown oder den binären Originalkörper. `obscura serve --port 9222` öffnet den CDP-Server; Clients verbinden sich mit dessen WebSocket-Endpunkt. `obscura scrape` verarbeitet mehrere URLs mit einstellbarer Parallelität. [tweet-2094114217229946976](../sources/tweet-2094114217229946976.md)

Die gespeicherte README dokumentiert native Screenshots, Live-Screencast und PDF-Export. Für CLI-Screenshots gibt es `--screenshot`; CDP bietet Page-Capture/Screencast, der mitgelieferte MCP-Server unter anderem Navigation, Snapshot, Screenshot, PDF, Klicks, Eingaben und JavaScript-Auswertung. MCP läuft per stdio oder mit `obscura mcp --http --port 8080`. [tweet-2094114217229946976](../sources/tweet-2094114217229946976.md)

## Netzwerk und Grenzen

Private/interne IP-Ziele sind laut README standardmäßig gegen SSRF gesperrt; `--allow-private-network` öffnet lokale Entwicklungsziele ausdrücklich. Das Docker-Beispiel publiziert den CDP-Port nur über `127.0.0.1:9222:9222`. Die optionale Stealth-Variante randomisiert Fingerprints und blockiert Tracker; sie ist eine Herstellerbeschreibung, keine Garantie gegen Erkennung. [tweet-2094114217229946976](../sources/tweet-2094114217229946976.md)

Die README bewirbt niedrigeren Speicherverbrauch und schnellere Seitenläufe als Chrome und verlinkt [obscura-benchmark](https://github.com/h4ckf0r0day/obscura-benchmark). Diese Vergleiche wurden hier nicht reproduziert. Lange CSS-Randfälle, manche Web-APIs, Medienwiedergabe, Compositor-Effekte und Font-Rasterisierung können ausdrücklich von Chromium abweichen; die behauptete Austauschbarkeit über CDP ist daher keine vollständige Browserparität. Obscura Cloud wird in der gespeicherten Quelle erst als geplantes Hostingangebot beschrieben. [tweet-2094114217229946976](../sources/tweet-2094114217229946976.md)
