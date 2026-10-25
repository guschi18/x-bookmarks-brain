---
tags: [agents, tools]
sources: [tweet-2059250974561051105.md]
created: 2026-09-30
updated: 2026-09-30
---

# Agentlytics

## Projekt und Start

[Agentlytics](https://github.com/f/agentlytics) bündelt laut gespeicherter README KI-Konversationen aus 17 Editoren in einer lokalen SQLite-Datenbank und einem Browser-Dashboard. Start: npx agentlytics; das Dashboard läuft auf localhost:4637. Die README nennt macOS und Node.js ≥20.19 oder ≥22.12. [tweet-2059250974561051105](../sources/tweet-2059250974561051105.md)

## Analyse und unterstützte Daten

Genannt werden Sitzungs- und Projektsuche, Tool- und Modellverteilung, Tokenstatistik, geschätzte Kosten, Editorvergleiche und Abonnementübersichten. [Claude Code](Claude%20Code.md) und [Codex](Codex.md) gehören zur Liste; nicht jeder Adapter liefert alle Datenarten. Devin, Devin Next und Antigravity müssen beim Scan laut README laufen. [tweet-2059250974561051105](../sources/tweet-2059250974561051105.md)

## Relay und Datenfluss

Der optionale Relay läuft separat auf Port 4638; Clients teilen ausgewählte Projektsitzungen alle 30 Sekunden, und ein MCP-Endpunkt erlaubt deren Abfrage. Die README empfiehlt vertrauenswürdige lokale Netze und optional RELAY_PASSWORD. Dieser Modus überträgt Sitzungsdaten und ist deshalb getrennt von der beworbenen lokalen Einzelplatzanalyse zu betrachten. [tweet-2059250974561051105](../sources/tweet-2059250974561051105.md)

## Grenzen

Windows/Linux-Unterstützung und Offline-Auslesen bestimmter Editoren stehen in der gespeicherten Roadmap. Dashboard-Demo und Local-only-Werbung ersetzen weder eine Datenschutzprüfung noch einen reproduzierten Kostenvergleich. [tweet-2059250974561051105](../sources/tweet-2059250974561051105.md)
