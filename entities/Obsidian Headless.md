---
tags: [tools]
sources: [tweet-2053764479641338083.md]
created: 2026-10-02
updated: 2026-10-08
---

# Obsidian Headless

## Überblick (Stand 2026-05)

Obsidian Headless ist laut Obsidian-Hilfe ein eigenständiger Kommandozeilen-Client (Open Beta, bestätigt am 2026-10-08) für Obsidian-Dienste ohne Desktop-App. Er bietet Headless Sync mit der Ende-zu-Ende-Verschlüsselung von Obsidian Sync und Headless Publish. Voraussetzung ist Node.js 22 oder neuer; das npm-Paket heißt obsidian-headless, die Anmeldung erfolgt per `ob login` mit optionaler 2FA. [tweet-2053764479641338083](../sources/tweet-2053764479641338083.md)

## Einsatzzwecke

Die Hilfe nennt automatische Remote-Backups, automatische Website-Veröffentlichung, Vault-Zugriff für Agenten-Tools ohne Zugriff auf den gesamten Rechner, einen geteilten Team-Vault auf einem Server und geplante Automatisierungen wie Wochenzusammenfassungen aus Tagesnotizen. Ein Praxisbeispiel aus dem Post: Headless Sync als systemd-Dienst. [tweet-2053764479641338083](../sources/tweet-2053764479641338083.md)

## Abgrenzung

Obsidian CLI steuert die laufende Desktop-App aus dem Terminal; Obsidian Headless läuft unabhängig davon. Für agentengepflegte Vaults nach dem [LLM Wiki Pattern](../concepts/LLM%20Wiki%20Pattern.md) ist das eine mögliche Synchronisationsschicht, die Quelle prüft diese Nutzung aber nicht. [tweet-2053764479641338083](../sources/tweet-2053764479641338083.md)
