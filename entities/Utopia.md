---
tags: [agents, tools, research]
sources: [tweet-2095111361181405259.md]
created: 2026-10-09
updated: 2026-10-09
---

# Utopia

## Produkt und Architektur (Stand 2026-09)

**Repository:** https://github.com/deeplethe/utopia. Die gespeicherte README von DeepLethe beschreibt eine selbst betriebene Wissensanwendung mit Systemkonsole, Graphbrowser und Ontologie-Workbench: ein Rust-Binary mit eingebetteter Tantivy-Volltextsuche und eine Postgres-Datenbank für pgvector und Job-Queue. Die Erst-Registrierung wird Systemadministrator; eine offene Wissensbasis entsteht automatisch. [tweet-2095111361181405259](../sources/tweet-2095111361181405259.md)

Dokument-Ingest umfasst unter anderem PDF, Office-Dateien, Tabellen, Markdown und HTML; Web, RSS, GitHub, Jira, Notion, WebDAV und S3 können laut README synchronisiert werden. Volltext- und Vektorsuche werden mit RRF zusammengeführt; Antworten zeigen Passagenbelege. OpenAI-kompatible lokale Modellendpunkte erlauben laut Projekt abgeschotteten Betrieb. [tweet-2095111361181405259](../sources/tweet-2095111361181405259.md)

## Zeit, Provenienz und Prüfung (Stand 2026-09)

Ein bitemporaler Graph trennt die Zeit, zu der ein Fakt in der Welt galt, von der Zeit, zu der das System ihn erfasste. Korrekturen schließen die alte Version und verknüpfen eine neue; die Herkunft bleibt sichtbar. Das ergänzt [Agentic Knowledge Graph Construction](../concepts/Agentic%20Knowledge%20Graph%20Construction.md) um versionierte laufende Pflege. [tweet-2095111361181405259](../sources/tweet-2095111361181405259.md)

Entity-Auflösung erfolgt laut README über exakten Namen/Alias, Embedding-Ähnlichkeit und Modellurteil für zweifelhafte Paare; Merges sind rücknehmbar. Ein Review sammelt unsichere Extraktionen, mögliche Duplikate und Kardinalitätskonflikte. Neue widersprechende Fakten können alte schließen, parallel erhalten bleiben oder abgelehnt werden. [tweet-2095111361181405259](../sources/tweet-2095111361181405259.md)

Ontologieaxiome können per Forward Chaining Fakten ableiten; diese Funktion ist standardmäßig aus, weil falsche Axiome falsche Ergebnisse erzeugen. Abgeleitete Fakten tragen ihre Prämissen, Validität und Konfidenz; bei Konflikten mit expliziten Fakten stehen die expliziten Fakten. Ein append-only Entscheidungsledger hält Review, Merge und Graph-Neuaufbau fest. [tweet-2095111361181405259](../sources/tweet-2095111361181405259.md)

## Agenten und Einstieg (Stand 2026-09)

Der eingebaute Agent durchsucht Dokumente, traversiert Fakten nach Datum und fragt angebundene Datenbanken ab. Dieselben Lesewerkzeuge werden über MCP bereitgestellt. Ontology2SQL schlägt Ontologie-Mappings für Tabellen vor, die Menschen bestätigen. [tweet-2095111361181405259](../sources/tweet-2095111361181405259.md)

Die README startet mit Docker: Repository klonen, docker compose --profile app up -d, http://localhost:1516 öffnen und Chat-/Embedding-Endpunkte konfigurieren. Für lokale Entwicklung nennt sie Rust 1.85+, Node 20+ und pnpm. Basis-Rollen sind Owner, Admin, Editor und Viewer; offene Bases sind deploymentsweit lesbar. [tweet-2095111361181405259](../sources/tweet-2095111361181405259.md)

## Entwicklungsstand und Grenzen (Stand 2026-09)

Die gespeicherte README nennt v0.1 mit vorwärtsgerichteten Schema-Migrationen ohne Rollback und empfiehlt Versionspinning sowie Backup von Datenbank und Datenverzeichnis vor Upgrades. Der Datenbankpasswort-Default ist utopia; ein späterer .env-Wechsel allein ändert das bestehende Passwort nicht. docker compose down -v löscht Daten. Vor Internetfreigabe verweist das Projekt auf SECURITY.md. [tweet-2095111361181405259](../sources/tweet-2095111361181405259.md)

Decision Intelligence, Execution Gates, Agent-Memory-Schreibpfade, OIDC sowie Backup-/Restore-Kommandos und Benchmarks mit 100.000 Dokumenten stehen in diesem Snapshot auf der Roadmap. Der Titel „first enterprise world model“ ist Anbieterframing; Funktionen, Sicherheitsverhalten und Offline-Eignung wurden hier nicht durch einen Betrieb geprüft. Die README nennt Apache-2.0. [tweet-2095111361181405259](../sources/tweet-2095111361181405259.md)
