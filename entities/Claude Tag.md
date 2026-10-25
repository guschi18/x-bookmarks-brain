---
tags: [agents, tools, product-building]
sources: [tweet-2070235730295865661.md]
created: 2026-09-30
updated: 2026-09-30
---

# Claude Tag

## Rolle und Auslöser

ClaudeDevs stellt Claude Tag als proaktiven Mehrnutzer-Agenten auf Basis von [Claude Code](Claude%20Code.md) mit Identität und Gedächtnis vor. Laut Video kann er Nachrichten beobachten, zeitgesteuerte Arbeit einrichten und auf Service-Ereignisse reagieren; die Arbeitsmuster ergänzen [Loop Engineering](../concepts/Loop%20Engineering.md). [tweet-2070235730295865661](../sources/tweet-2070235730295865661.md)

Ein leichter Klassifikator entscheidet nach Kanalinstruktionen über das Aufwachen; Erwähnungen oder laufende Interaktion im Thread wecken den Agenten laut Hersteller immer. Ein Thread besitzt eine Agenteninstanz mit eigener Sandbox für Repository-Klonen, Code, Tests und PRs; zusätzliche Nachrichten steuern diese Instanz weiter. [tweet-2070235730295865661](../sources/tweet-2070235730295865661.md)

## Gedächtnis, Zugänge und Teamkontext

Jeder Kanal erhält eigene Instruktionen, Erinnerungen und Rechte. Admins provisionieren Service-Zugangsdaten, um Agentenaktionen auditierbar zu machen; in DMs soll der Agent die persönlichen MCPs und Connectoren des Nutzers verwenden können. Das ist die behauptete Zugangsarchitektur, keine unabhängige Sicherheitsprüfung. [tweet-2070235730295865661](../sources/tweet-2070235730295865661.md)

Das Video empfiehlt angeheftete „please remember“-Instruktionen, explizite Regeln für automatische Antworten, Statusmeldungen in einem Pin und Emoji-Status pro Untersuchung. Git dient als Übergabe zwischen asynchronen PRs und lokaler Arbeit; Screenshots, Aufnahmen und HTML-Berichte sollen mobile Reviews erleichtern. [tweet-2070235730295865661](../sources/tweet-2070235730295865661.md)

## Beispiele und Grenzen

Genannte Aufgaben sind PR-Betreuung, Fehlertriage per Webhook, tägliche Main-Zusammenfassungen, Terminabstimmung und persönliche Wochenberichte. Rund 65 Prozent der intern eröffneten Anthropic-PRs werden dem Agenten zugeschrieben; eine Zählgrundlage und unabhängige Wirkungsmessung fehlen. Das automatische Transkript erkennt Claude wiederholt als Cloud; die Produktbenennung folgt dem gespeicherten Post. [tweet-2070235730295865661](../sources/tweet-2070235730295865661.md)
