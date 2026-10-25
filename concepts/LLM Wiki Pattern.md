---
tags: [research, tools]
sources: [tweet-2071659476994699580.md, tweet-2071105441698910415.md, tweet-2059486502401569047.md, tweet-2057924890330644925.md, tweet-2040470801506541998.md, tweet-2052361597000032594.md, tweet-2045912259210485815.md]
created: 2026-09-29
updated: 2026-10-21
---

# LLM Wiki Pattern

## Definition und Ablauf

Der gespeicherte Artikel beschreibt ein Markdown-Wiki, in dem ein Agent neue Quellen liest, Seiten über Personen und Konzepte anlegt, Wikilinks pflegt und spätere Antworten auf diese Seiten stützt. [Claude Obsidian](../entities/Claude%20Obsidian.md) wird als Beispielprojekt genannt; [Claude Code](../entities/Claude%20Code.md) arbeitet am lokalen Vault. [tweet-2071659476994699580](../sources/tweet-2071659476994699580.md)

## Voraussetzung und Grenze

Der Ablauf setzt zugängliche Quelldateien, eindeutige Seitennamen und regelmäßige Prüfung von Links und Behauptungen voraus. Der Artikel empfiehlt auch einen Index und einen kurzen Kontextspeicher für neue Sitzungen. Sein Nutzen- und Kostenversprechen ist eine Autorenbehauptung; ein kontrollierter Vergleich fehlt. [tweet-2071659476994699580](../sources/tweet-2071659476994699580.md)

## Weiterer Stack und Zuschreibungsgrenze

Ein gespeicherter Artikel kombiniert Obsidian als lokalen Markdown-Graphen mit Hermes als Agent und MiniMax M3 als Modell. Er empfiehlt, zuerst einen einzelnen Ordner und ein prüfbares Markdown-Ergebnis zu bearbeiten. Der begleitende Post nennt stattdessen Karpathy und Claude; die gespeicherte Quelle belegt diese Zuschreibung nicht unabhängig. [tweet-2071105441698910415](../sources/tweet-2071105441698910415.md)

## Briefings und Verbindungen mit Vellum

Der Obsidian/[Vellum](../entities/Vellum.md)-Artikel trennt schnelle Erfassung von nach Notiztyp sortierten Captures und späteren Verbindungsnotizen. Seine vier Prompts bearbeiten Inbox, tägliche Briefings, Wochenverbindungen und thematische Recherche anhand der tatsächlichen Notizen. [tweet-2059486502401569047](../sources/tweet-2059486502401569047.md)

Verbindungsnotizen sollen gleiche Prinzipien über Domänen hinweg, Widersprüche, Muster aus mehreren Notizen oder Antworten auf offene Fragen verlinken. Laufende Projekte werden wöchentlich im Kontextfile aktualisiert; Ergebnisse von Entscheidungen sollen in die Ursprungsnotizen zurückfließen. [tweet-2059486502401569047](../sources/tweet-2059486502401569047.md)

Dauerbetrieb, Integrationscode und die behauptete langfristige Verbesserung sind nicht geprüft. Der Artikel liefert Workflow-Prompts, aber keinen Coverage-/Attributionsvertrag für automatisch erzeugte Wissensseiten. [tweet-2059486502401569047](../sources/tweet-2059486502401569047.md)

## Direkter Interviewbeleg zum Verständnis (Stand 2026-05)

Karpathy beschreibt im gespeicherten Gespräch persönliche und organisatorische LLM-Wikis als neue Zusammenstellung vorhandener Dokumente. Fragen und unterschiedliche Projektionen derselben Informationen sollen Verständnis fördern; er betont, dass ausgelagertes Denken eigenes Verständnis nicht ersetzt. Das ist sein Anwendungsbericht ohne gemessene Lernwirkung und ein Beispiel für [Software 3.0](Software%203.0.md). [tweet-2057924890330644925](../sources/tweet-2057924890330644925.md)

## Karpathys Primärquelle (Stand 2026-04)

Das gespeicherte Gist „llm-wiki“ ist die direkte Quelle des Musters. Es grenzt das Wiki von RAG ab: Statt Wissen bei jeder Frage neu aus Chunks zusammenzusetzen, integriert das LLM jede neue Quelle in ein dauerhaftes, verlinktes Markdown-Wiki, aktualisiert Entitäts- und Themenseiten und markiert Widersprüche. [tweet-2040470801506541998](../sources/tweet-2040470801506541998.md)

- **Drei Schichten:** unveränderliche Rohquellen, ein vollständig vom LLM gepflegtes Wiki und eine Schema-Datei wie CLAUDE.md oder AGENTS.md mit Struktur, Konventionen und Abläufen. [tweet-2040470801506541998](../sources/tweet-2040470801506541998.md)
- **Operationen:** Ingest (eine Quelle kann zehn bis fünfzehn Seiten berühren), Query mit Zitaten und Rückspeichern guter Antworten als neue Seiten, Lint auf Widersprüche, veraltete Aussagen, Waisen, fehlende Seiten und Querverweise. [tweet-2040470801506541998](../sources/tweet-2040470801506541998.md)
- **Navigation:** index.md als inhaltlicher Katalog und log.md als append-only Chronik mit einheitlichem Präfix wie „## [2026-04-02] ingest | Article Title“, das sich mit grep auswerten lässt. [tweet-2040470801506541998](../sources/tweet-2040470801506541998.md)
- **Werkzeuge:** optional qmd als lokale Hybrid-Suche mit CLI und MCP, Obsidian Web Clipper, lokal gespeicherte Bilder, Graph-Ansicht, Marp und Dataview; das Wiki ist ein Git-Repository. [tweet-2040470801506541998](../sources/tweet-2040470801506541998.md)

Karpathy begründet den Ansatz damit, dass die Buchhaltung, nicht Lesen oder Denken, Wikis scheitern lässt und LLMs diese Pflege fast kostenlos übernehmen. Der zitierte Ursprungspost nennt ein eigenes Wiki mit rund 100 Artikeln und 400.000 Wörtern, bei dem Index und Kurzsummaries ohne aufwendiges RAG genügten; das ist ein Erfahrungswert, keine Messung. [tweet-2040470801506541998](../sources/tweet-2040470801506541998.md)

Er veröffentlicht das Muster bewusst abstrakt als „Idea File“, das der Agent des Empfängers konkret ausbaut; die konkrete Umsetzung hängt vom eigenen Bereich ab. Das passt zu seiner Beschreibung von [Software 3.0](Software%203.0.md), in der Prompt und Kontext zum Programmiermittel werden. [tweet-2040470801506541998](../sources/tweet-2040470801506541998.md)

## Persönlicher Denkpartner mit Internet Vin (Stand 2026-05)

Im gespeicherten Interview mit Greg Isenberg beschreibt Internet Vin eigene [Claude Code](../entities/Claude%20Code.md)-Befehle auf einem Obsidian-Vault. `/context` lädt Projekt-/Personenkontext und verfolgte Links; `/today` verbindet Kalender, Aufgaben, Nachrichten und Tagesnotizen; `/close-day` zieht Aufgaben, Verbindungen und zu prüfende Überzeugungen aus dem Tag. Es sind eigene Arbeitsabläufe, keine eingebauten Obsidian-Kommandos; ein vollständiges Skill-Paket ist nicht gespeichert. [tweet-2052361597000032594](../sources/tweet-2052361597000032594.md)

- `/ghost` leitet ein persönliches Stimmenprofil aus dem Vault ab und prüft die Ähnlichkeit; `/challenge` sucht Gegenbelege und Widersprüche zu eigenen Überzeugungen; `/emerge` benennt implizite Ideen aus verstreuten Prämissen. [tweet-2052361597000032594](../sources/tweet-2052361597000032594.md)
- `/drift` vergleicht erklärte Absichten mit tatsächlichem Verhalten über 30–60 Tage; `/trace` rekonstruiert die Entwicklung einer Idee aus datierten Notizen; `/connect` sucht Verbindungen zwischen zwei Bereichen anhand der Notizen und ihrer Links. Diese Zeitfenster sind Vins beschriebene Verfahren, keine gemessenen optimalen Parameter. [tweet-2052361597000032594](../sources/tweet-2052361597000032594.md)
- `/ideas` durchsucht Tagesnotizen und den Linkgraphen nach bereichsübergreifenden Ideen. Der im Gespräch entwickelte `/graduate`-Ablauf sucht Kandidaten in Tagesnotizen, gleicht sie mit vorhandenen Seiten ab und lässt zwischen neuer eigenständiger Notiz, Ergänzung oder Verwerfen wählen. [tweet-2052361597000032594](../sources/tweet-2052361597000032594.md)

Vin hält persönliche Notizen bewusst getrennt von automatisch geschriebenen Ergebnissen: Andernfalls könnte ein späterer Mustervergleich Aussagen des Agenten als seine eigenen Ansichten auswerten. Aktuelle Kontextdateien beschreiben Ziele und Hypothesen; breite Vault-Lektüre kostet im gezeigten Ablauf mehrere Minuten. Das sind persönliche Arbeitsweisen und Erfahrungen, kein nachgewiesener Lern- oder Produktivitätsgewinn. [tweet-2052361597000032594](../sources/tweet-2052361597000032594.md)

## Capture und Syntheserhythmus (Stand 2026-05; begleitender Artikel)

Der gespeicherte Artikel ergänzt Readwise für Texte/Highlights, Airr und Whisper für Audio, einen Telegram-Eingang und n8n als Transport in einen lokalen Markdown-Vault. Seine CLAUDE.md-Vorlage hält Person, Ziele, aktive Projekte, nächste Meilensteine und Ablageregeln fest; Projektkontext soll wöchentlich aktualisiert werden. Die Telegram-Anleitung ist eine Knoten-Skizze, kein vollständig exportierter Workflow. [tweet-2052361597000032594](../sources/tweet-2052361597000032594.md)

Der vollständige Tagesbrief-Prompt in der Source liest die letzten 24 Stunden der Inbox und sieben Tage der Notes: drei konkrete Verbindungen mit zitierten Passagen, ein übergreifendes Muster und eine offene Denkfrage; Ausgabe ist eine datierte Markdown-Datei. Der Wochenprompt prüft entstehende Thesen, Widersprüche mit beiden Seiten, Wissenslücken und eine priorisierte Handlung. Zeitplan und Dateizugriff müssen durch die tatsächliche Automation bereitgestellt werden; ein Prompt allein belegt keinen funktionierenden Dauerbetrieb. [tweet-2052361597000032594](../sources/tweet-2052361597000032594.md)

Der Artikel wirbt für automatische tägliche Ausgabe, während das Interview überwiegend explizit angefragte Denkwerkzeuge zeigt. Diese beiden Verfahren bleiben getrennte Evidenz; die Quelle belegt keinen durchgehend autonomen persönlichen Betrieb. [tweet-2052361597000032594](../sources/tweet-2052361597000032594.md)

## Gegenbeispiel: Retrievalkosten und angewandtes Wissen (Stand 2026-04)

Artem beschreibt einen persönlichen Vergleich mit 19 Wiki-Quellen, 50 NotebookLM-Quellen und zehn Fragen. In seiner Wiki-Umsetzung habe Claude trotz Index komplette Transkripte gelesen: etwa 44.000 Tokens je Frage nach rund 20 Minuten Ingest. NotebookLM habe mit Quellenzitaten ungefähr eine Minute je Antwort gebraucht. Unterschiedliche Quellenmengen, fehlende Messprotokolle und die konkrete Retrievalkonfiguration begrenzen den Vergleich; er belegt keinen allgemeinen Kostenvorteil oder eine optimale Quellenzahl. [tweet-2045912259210485815](../sources/tweet-2045912259210485815.md)

Der Autor bevorzugt NotebookLM für schnelle Themenübersichten und betrachtet langfristige tiefe Recherche, Teamwissen und Wettbewerbsanalysen als passendere Wiki-Einsätze. Seine Behauptung, ein Wiki könne nur Fragen beantworten und habe keinen Praxisbezug, beschreibt seine Bewertung des getesteten Ablaufs; sie ist keine technische Grenze des Markdown-Musters. Die oben dokumentierten anderen Praxisberichte bleiben davon getrennt. [tweet-2045912259210485815](../sources/tweet-2045912259210485815.md)

### Dalios Ablauf als täglicher Entscheidungs-Skill

Der wiederverwendbare Teil ist die Übersetzung einer Quelle in eine konkrete Routine: Ziele kennen, Probleme nicht tolerieren, Ursachen diagnostizieren, einen Plan entwerfen und ihn ausführen. Der Autor ergänzt Tagesreflexion und ein Wochenreview mit der Frage, ob dieselben Probleme oder Problemtypen wiederkehren. Das ergänzt [Personalized LLM Workflows](Personalized%20LLM%20Workflows.md) um einen dokumentierten Anwendungsfall, ohne eine gemessene Verbesserung von Entscheidungen zu belegen. [tweet-2045912259210485815](../sources/tweet-2045912259210485815.md)

Der Artikel nennt außerdem eine Übersicht aus 21 Videos zu Agentenwerkzeugen. Weder sein angekündigter NotebookLM-Skill noch der Walkthrough sind als strukturierte Links gespeichert. Angaben zu damaligen Abo-Limits, früher unbegrenzter Nutzung und Tokenkosten sind April-Erfahrungen des Autors; der Text belegt weder aktuelle Tarife noch eine automatisch funktionierende NotebookLM-Anbindung. [tweet-2045912259210485815](../sources/tweet-2045912259210485815.md)
