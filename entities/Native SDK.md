---
tags: [tools, product-building]
sources: [tweet-2052907884728467699.md]
created: 2026-10-13
updated: 2026-10-13
---

# Native SDK

## Historischer Einstieg als zero-native (Stand 2026-05)

Chris Tate stellt zero-native als Verbindung von Web-Oberfläche und Zig-Runtime vor. Das geprüfte Bild zeigt Next.js, Vite, React, Svelte und Vue sowie WKWebView, WebKitGTK, WebView2 und optional Chromium/CEF; Desktop und Mobile werden beworben. [tweet-2052907884728467699](../sources/tweet-2052907884728467699.md)

`npm i -g zero-native` ist der im Mai-Bild dokumentierte historische Installationsbefehl. Kleine Binärdateien und niedriger Speicherverbrauch sind Projektbehauptungen ohne gespeicherte Messwerte. [tweet-2052907884728467699](../sources/tweet-2052907884728467699.md)

## Ergänzender Primärquellenabgleich (Stand 2026-10; geprüft 2026-10-13)

Die frühere [Repository-Adresse](https://github.com/vercel-labs/zero-native) führt inzwischen zu [vercel-labs/native](https://github.com/vercel-labs/native). Die am 13.10.2026 ergänzend gelesene README beschreibt Native SDK als experimentelles Toolkit für native Desktop-Anwendungen mit TypeScript und Native-Markup; Zig-Kerne und eingebetteter Webinhalt sind zusätzliche Optionen. Der neue Einstieg ist nicht identisch mit dem historischen Webview-Launch. [tweet-2052907884728467699](../sources/tweet-2052907884728467699.md)

Die geprüfte README verlangt Node.js 24+ und nennt `npm install -g @native-sdk/cli`, danach `native init my_app`, `cd my_app` und `native dev`. `native check` prüft das Projekt, `native build` erzeugt ein Release-Binary. Dies sind dokumentierte Befehle, kein eigener Installations- oder Build-Test. [tweet-2052907884728467699](../sources/tweet-2052907884728467699.md)

## Grenzen

Plattformfähigkeiten unterscheiden sich; Mobile-Unterstützung entwickelt sich laut ergänzender README weiter. Die pauschale Mai-Plattformliste darf nicht als heutige vollständige Unterstützung gelesen werden; dafür verweist das Projekt auf seine [Plattformmatrix](https://native-sdk.dev/docs/platform-support). Historischer Raw-Beleg und spätere Dokumentation sind auf der Source getrennt. [tweet-2052907884728467699](../sources/tweet-2052907884728467699.md)
