---
tags: [agents, tools, product-building]
sources: [tweet-2098804076335218805.md]
created: 2026-10-08
updated: 2026-10-08
---

# Agency

## Arbeitsmodell (Stand 2026-09)

[Repository](https://github.com/browser-use/agency): ein aktiver Coding-Agent recherchiert nützliche Arbeit und bereitet Änderungen, Entwürfe oder Ideen als Karten vor. me.md hält ein privates Profil; eigene Layout- und Freigabe-Dateien steuern die Agentenanweisungen. [tweet-2098804076335218805](../sources/tweet-2098804076335218805.md)

Die README verlangt konkrete Ergebnisse vor der Entscheidung: Karten zeigen Problem, vorbereiteten Ausgang und exakte Aktion. Freigabeklicks stellen Arbeit an; erst ausgeführte und geprüfte Ergebnisse zählen als abgeschlossen. [tweet-2098804076335218805](../sources/tweet-2098804076335218805.md)

## Lokales Setup (Stand 2026-09)

Dokumentiert sind Node.js ab 22.13, npm ci und npm run dev -- --hostname localhost --port 3100. SQLite/D1-Zustand liegt lokal unter .wrangler; der Skill-Installer bietet --codex und --claude. [tweet-2098804076335218805](../sources/tweet-2098804076335218805.md)

Die App ist für einen vertrauten Einzelbenutzer mit nicht authentifizierten Routen ausgelegt und soll auf Loopback bleiben. Installation erzeugt weder Hintergrundarbeiter noch Zeitplan noch Kontoverbindungen; die aktive Agentensitzung koordiniert Jobs und überprüft verfügbaren Zugang. [tweet-2098804076335218805](../sources/tweet-2098804076335218805.md)

## Freigaben und Grenzen (Stand 2026-09)

Job-Ergebnisse unterscheiden completed, review und blocked; Genehmigung allein ist kein erledigter Job. Extern sichtbare Nachrichten und Änderungen benötigen laut README aktionsbezogene Freigaben; die App selbst erzwingt die Agentenpolicy nicht. [tweet-2098804076335218805](../sources/tweet-2098804076335218805.md)

Die Launchbehauptungen „100x“ und „never open Gmail, Chrome or Slack again“ sind nicht gemessen. Lokaler Zustand und autorisierte Integrationen sind Voraussetzungen, keine automatisch vollständige Lebenskontext-Erfassung. [tweet-2098804076335218805](../sources/tweet-2098804076335218805.md)
