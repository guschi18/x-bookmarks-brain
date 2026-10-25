---
tags: [agents, tools]
sources: [tweet-2082164248697069935.md, tweet-2097242863964958760.md, tweet-2113698001889927608.md]
created: 2026-10-02
updated: 2026-10-25
---

# Model Context Protocol

## Definition (Stand 2026-07)

Der Claude-Blog beschreibt das Model Context Protocol (MCP) als offenen Standard, um KI-Agenten mit Anwendungen, Werkzeugen und Daten zu verbinden. MCP 2026-07-28 ist laut Artikel die fünfte Spec-Version. [tweet-2082164248697069935](../sources/tweet-2082164248697069935.md)

## Änderungen in 2026-07-28 (Stand 2026-07)

- **Zustandsloser Kern:** MCP wechselt von einem bidirektionalen, zustandsbehafteten Protokoll zu Request/Response; Server sollen dadurch auf Serverless- und Edge-Infrastruktur laufen. [tweet-2082164248697069935](../sources/tweet-2082164248697069935.md)
- **Standardisierte Extensions:** MCP Apps (interaktive UIs) und Tasks (lang laufende Arbeit) laufen in einem versionierten Extensions-Rahmen, ohne den Kern zu ändern. [tweet-2082164248697069935](../sources/tweet-2082164248697069935.md)
- **Auth-Härtung:** Die Autorisierung folgt produktiven OAuth-2.0- und OIDC-Setups, sodass Server sich ohne Umwege an Identitätssysteme wie Entra oder Okta anbinden lassen. [tweet-2082164248697069935](../sources/tweet-2082164248697069935.md)

## Umsetzung in Claude (Stand 2026-07)

Anthropic nennt über 950 Server im Connector-Verzeichnis, MCP Apps im Chat, Enterprise-managed Auth über den Identity-Provider, ein Observability-Dashboard für Connector-Entwickler und MCP Tunnels als Research Preview für Server in privaten Netzen ohne eingehende Firewallregeln. Der Support wird laut Artikel schrittweise ausgerollt. [tweet-2082164248697069935](../sources/tweet-2082164248697069935.md) MCP Tunnels sind laut Dokumentation (Stand 2026-10-08) weiter Research Preview und nur für Claude-Enterprise-Organisationen auf Anfrage verfügbar. [tweet-2082164248697069935](../sources/tweet-2082164248697069935.md)

## Grenzen (Stand 2026-07)

Die Zahl von über 400 Millionen monatlichen SDK-Downloads und die Zitate von Figma, Intuit, Netlify, Zoom und weiteren Firmen sind Herstellerangaben aus einem Ankündigungsartikel; die Spec selbst ist nur verlinkt, nicht gespeichert. Ein konkreter MCP-Server im Wiki ist etwa [Codebase Memory MCP](../entities/Codebase%20Memory%20MCP.md). [tweet-2082164248697069935](../sources/tweet-2082164248697069935.md)

## MCP gegenüber CLI und Skills (Stand 2026-09)

Der InsForge-Artikel beschränkt MCP auf die Zustandsabfrage (ein Metadaten-Aufruf von etwa 500 Tokens) und überlässt Wissen den Skills und Operationen der CLI mit JSON-Ausgabe; ein zitierter Scalekit-Benchmark nennt für CLI plus Skills 10- bis 35-fach bessere Tokeneffizienz bei Einzelnutzer-Arbeitsabläufen. Der Wert ist nur aus zweiter Hand gespeichert. Details: [InsForge](../entities/InsForge.md). [tweet-2097242863964958760](../sources/tweet-2097242863964958760.md)

## MCP Tasks und Elicitations in Claude (Stand 2026-10)

ClaudeDevs kündigt am 2026-10-23 Unterstützung für MCP Tasks und Elicitations in Claude an. Tasks lassen Plugins langlaufende Aufträge wie Deep Research an Claude übergeben und melden das Ergebnis nach Abschluss zurück. [tweet-2113698001889927608](../sources/tweet-2113698001889927608.md) Zu Elicitations nennt die Quelle keine Einzelheiten, und das Video ohne Transkript liegt nur als Datei vor. [tweet-2113698001889927608](../sources/tweet-2113698001889927608.md) Zum Plugin-Kontext siehe [Claude Plugins](../entities/Claude%20Plugins.md).
