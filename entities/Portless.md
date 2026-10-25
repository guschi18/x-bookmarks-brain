---
tags: [tools, product-building, agents]
sources: [tweet-2048868170195144805.md]
created: 2026-10-16
updated: 2026-10-16
---

# Portless

## Zweck und Einstieg (Stand 2026-04)

[vercel-labs/portless](https://github.com/vercel-labs/portless) ersetzt wechselnde localhost-Portnummern durch benannte lokale URLs. Der Post nennt npm install -g portless für Menschen und npx skills add vercel-labs/portless für Agenten. [tweet-2048868170195144805](../sources/tweet-2048868170195144805.md)

## Routing und parallele Arbeit (gespeicherter README-Stand)

Ein lokaler Proxy ordnet Namen einem freien Anwendungsport zu; portless myapp next dev beziehungsweise portless run next dev starten die Anwendung. PORT und erkannte Framework-Flags verbinden Prozess und Proxy. Verknüpfte Git-Worktrees erhalten ein Branch-Präfix als Subdomain, sodass parallele Checkouts getrennte URLs verwenden. [tweet-2048868170195144805](../sources/tweet-2048868170195144805.md)

Die README dokumentiert Monorepo-Erkennung und optionale portless.json-/package.json-Konfiguration. Nicht erkannte oder zusammengesetzte Skripte behalten ihre eigene Portlogik; automatische Flag-Injektion ist keine Garantie für beliebige Startbefehle. [tweet-2048868170195144805](../sources/tweet-2048868170195144805.md)

## HTTPS, Freigabe und Diagnose

Der gespeicherte spätere Stand nennt HTTPS/HTTP2, eine lokale CA im Betriebssystem-Vertrauensspeicher und Loopback-Bindung als Standard. LAN-Modus sowie Tailscale/Funnel/ngrok sind gesonderte Freigabepfade mit unterschiedlichen Reichweiten. portless doctor prüft unter anderem Proxy, Routing, DNS und Zertifikatvertrauen; Proxy-Weiterleitung zwischen Portless-Apps benötigt einen passenden Host-Header. [tweet-2048868170195144805](../sources/tweet-2048868170195144805.md)

## Voraussetzungen und Grenzen

Die gespeicherte README nennt Node.js 24+ und macOS/Linux/Windows. CA-Vertrauen, Hosts-Datei und optionale Autostart-Dienste können Systemänderungen benötigen; diese späteren README-Angaben sind kein gesicherter Funktionsstand des April-Posts. Installation, Zertifikate und tatsächliches Routing wurden hier nicht ausgeführt. [tweet-2048868170195144805](../sources/tweet-2048868170195144805.md)
