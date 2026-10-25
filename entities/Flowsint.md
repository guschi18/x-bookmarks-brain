---
tags: [tools, security]
sources: [tweet-2098941338297458746.md]
created: 2026-10-08
updated: 2026-10-08
---

# Flowsint

## Graph und Enricher (Stand 2026-09)

[Repository](https://github.com/reconurge/flowsint): Graphoberfläche für OSINT-Beziehungen zwischen Domains, IPs, Organisationen, Personen, E-Mails, Social-Profilen und Crypto-Wallets. Enricher übernehmen DNS, WHOIS, ASN, Website-/Tracker-Erfassung, Social-Suche und weitere Zuordnungen. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

Die dokumentierte Architektur trennt FastAPI, Core/Orchestrator, Enricher, Typmodelle und Frontend; PostgreSQL, Neo4j und Redis gehören zum Docker-Stack. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## Lokaler Einstieg und Netzbetrieb (Stand 2026-09)

Unter Windows werden .env-Dateien aus .env.example angelegt und docker compose -f docker-compose.prod.yml up -d gestartet; erstes Konto unter localhost:5173/register, keine Standard-Zugangsdaten. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

Für Netzbetrieb verlangt die README neue AUTH_SECRET-, MASTER_VAULT_KEY_V1- und NEO4J_PASSWORD-Werte sowie den eigenen Host in der nginx-Allowlist. Datenbankdienste bleiben an Loopback; für HTTPS ist ein Reverse Proxy dokumentiert. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## Grenzen (Stand 2026-09)

Das Projekt bezeichnet sich als frühe Entwicklung mit unvollständigen Tests. Enricher liefern Recherchehinweise, keine automatisch bestätigten Identitäten oder Beziehungen; Leistungs- und Datenschutzangaben der README wurden nicht praktisch geprüft. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)
