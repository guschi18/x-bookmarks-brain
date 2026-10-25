---
tags: [agents, tools]
sources: [tweet-2052331797640515960.md, tweet-2035065083416428999.md, tweet-2027054100807106829.md]
created: 2026-10-14
updated: 2026-10-24
---

# Claude Cowork

## Demonstrierter Ablauf (Stand 2026-05)

Das Boris-Cherny-Interview zeigt Claude Cowork als Oberfläche für einen Agenten mit ausgewählten lokalen Ordnern. Cherny gibt einen Belegordner frei, lässt Dateien nach Belegdatum umbenennen und beantwortet Rückfragen bei fehlenden Datumsangaben; anschließend regt er eine Tabelle an. Er beschreibt den Claude Agent SDK als gemeinsame Grundlage mit [Claude Code](Claude%20Code.md). [tweet-2052331797640515960](../sources/tweet-2052331797640515960.md)

Im historischen Transkript nennt er Mac-Verfügbarkeit und Windows als künftig. Das ist der damalige Demostand, keine aktuelle Verfügbarkeitsauskunft. VM-Isolation, Browser-/MCP-Zugriff und Löschschutz sind Aussagen des Interviewgasts, keine hier geprüften Sicherheitsgarantien. [tweet-2052331797640515960](../sources/tweet-2052331797640515960.md)

## Separater Plugin-Kurs (Stand 2026-05)

Der gespeicherte X-Artikel von Khairallah ist eine andere Quelle innerhalb desselben Bookmarks, nicht Teil von Boris’ Anleitung. Er behandelt einen wiederverwendbaren Rollenworkflow als [Claude Plugins](Claude%20Plugins.md)-Bundle: `.claude-plugin/plugin.json` für Identität, `skills/<task>/SKILL.md` für Ablauf, `commands/run-task.md` für Aufruf und `references/` für Vorlagen. Globale und ordnerbezogene Instruktionen sind Vorschläge dieses Artikels. [tweet-2052331797640515960](../sources/tweet-2052331797640515960.md)

## Rollenwissen in einen prüfbaren Skill übersetzen (Stand 2026-05)

1. Mit dem vollständigen Rechercheprompt beginnen: "Research the complete professional workflow for a [ROLE] in [INDUSTRY]. Include: the step-by-step process they follow, tools and data sources they use, key metrics and decision criteria, common output formats, and expert-level edge cases and pitfalls. Be comprehensive — I am building an automated workflow from this." [tweet-2052331797640515960](../sources/tweet-2052331797640515960.md)
2. Die eigene Arbeitsweise ergänzen: Abkürzungen, Qualitätskontrollen, typische Fehler und konkrete gute beziehungsweise schlechte Ergebnisse festhalten. [tweet-2052331797640515960](../sources/tweet-2052331797640515960.md)
3. In SKILL.md Überblick, nummerierte prüfbare Schritte, festes Ausgabeformat, Regeln, Sonderfälle und Qualitätscheckliste formulieren. Die Beschreibung nennt fünf bis sieben konkrete Trigger sowie ausdrückliche Nicht-Anwendungsfälle. [tweet-2052331797640515960](../sources/tweet-2052331797640515960.md)
4. Ein Command liest den Arbeitskontext, führt den Skill samt Qualitätsprüfung aus, speichert das vereinbarte Ergebnis und meldet eine Zusammenfassung. Referenzdateien enthalten fachliche Vorlagen, Daten und Beispiele. [tweet-2052331797640515960](../sources/tweet-2052331797640515960.md)
5. Das Bundle auf realen Aufgaben mit verschiedenen Eingaben testen: Schritte eingehalten, Regeln beachtet, Format korrekt, Ergebnis verwendbar? Fehler durch präzisere Regeln oder Beispiele korrigieren und erneut prüfen. Der Artikel schlägt fünf erste Durchläufe und eine wöchentliche Überarbeitung vor. [tweet-2052331797640515960](../sources/tweet-2052331797640515960.md)

Der Artikel empfiehlt weitere Skills und verkettete Abläufe erst nach einem zuverlässigen Primärworkflow. Angekündigte autonome Mitarbeiterleistung, enorme Zeitgewinne und stetige Verbesserung sind Werbeversprechen; kein Plugin wurde hier installiert und kein Testergebnis reproduziert. Die vollständigen Vorlagen bleiben im Source-Beleg erhalten. [tweet-2052331797640515960](../sources/tweet-2052331797640515960.md)

## Fünf Plugin-Prompts (Stand 2026-03)

Der Artikel von Corey Ganim beschreibt Plugins als Bundle aus Skills, Connectoren, Slash-Commands und Subagenten. Die fünf vollständigen Formulierungen sind wiederverwendbare Ausgangspunkte, keine getesteten Integrationen. [tweet-2035065083416428999](../sources/tweet-2035065083416428999.md)

1. Anpassung: "Customize this plugin to match how my team actually works. We use [tools]. Our process for [workflow] is [description]. Update the skills and commands accordingly." [tweet-2035065083416428999](../sources/tweet-2035065083416428999.md)
2. Aufbau: "I want to build a plugin for [your workflow]. Walk me through creating the plugin structure, skills, and commands. My workflow involves [describe the steps]." [tweet-2035065083416428999](../sources/tweet-2035065083416428999.md)
3. Kundenupdates: "Build me a client management plugin that pulls active projects from Notion, writes weekly status updates using my communication style, and drafts them in Gmail. Include a /send-updates command." [tweet-2035065083416428999](../sources/tweet-2035065083416428999.md)
4. Wiederverwertung: "Build a content repurposing plugin with skills for: turning podcast transcripts into LinkedIn posts, creating Twitter threads from articles, and extracting clips suggestions from video scripts." [tweet-2035065083416428999](../sources/tweet-2035065083416428999.md)
5. Recherche: "Build a competitive research plugin that searches the web, organizes findings into a structured brief, and saves it to my Google Drive. Include /research-company and /market-analysis commands." [tweet-2035065083416428999](../sources/tweet-2035065083416428999.md)

Der ältere Artikel zeigt plugin.json direkt im Wurzelverzeichnis; die oben dokumentierte spätere Anleitung verwendet .claude-plugin/plugin.json. Die alte Skizze ersetzt diese spätere Struktur nicht. Das beworbene Zehn-Minuten-Onboarding ist kein gespeichertes Plugin-Artefakt; sein Video liefert auch nach erneutem Abruf keinen Transkripttext. [tweet-2035065083416428999](../sources/tweet-2035065083416428999.md)

## Tier-Liste der 21 Plugins (Stand 2026-02)

Ein X-Artikel von Nav Toor ordnet nach vier Wochen täglicher Nutzung die 21 Cowork-Plugins (11 am 30. Januar, 10 weitere am 24. Februar 2026) in Stufen; es ist das Urteil eines Anwenders, kein Test. [tweet-2027054100807106829](../sources/tweet-2027054100807106829.md)

- S-Tier: Data Analysis (/data:explore fasst einen CSV-Datensatz zusammen und schlägt Analysen vor, /data:write-query erzeugt SQL), Productivity (/productivity:start ordnet den Tag und die Aufgaben) und Sales (/sales:call-prep, /sales:battlecard). [tweet-2027054100807106829](../sources/tweet-2027054100807106829.md)
- A-Tier: Legal, Product Management (/product-management:write-spec), Marketing (Markenstimme aus brand-voice.md) und Finance samt Financial Analysis (Excel-zu-PowerPoint-Ablauf). [tweet-2027054100807106829](../sources/tweet-2027054100807106829.md)
- B-Tier: Customer Support, HR, Engineering, Operations und Design; sie gelten als Vorlagen, die 30-60 Minuten Anpassung an die eigene Firma brauchen. C-Tier: Enterprise Search, Bio-Research und das Meta-Plugin zum Erstellen von Plugins. [tweet-2027054100807106829](../sources/tweet-2027054100807106829.md)

Der Artikel beschreibt ein Plugin als Ordner aus Skills, Slash-Commands, Connectors (MCP) und Sub-Agenten und rät, nach dem Einsatz der S-Tier-Plugins eines für die eigene Rolle mit Firmenkontext anzupassen. [tweet-2027054100807106829](../sources/tweet-2027054100807106829.md)

Marktaussagen (285 Mrd. Dollar Börsenwert, Thomson Reuters -18 %, "SaaSpocalypse") und Zeitersparnisse (z. B. 90 auf 10 Minuten Gesprächsvorbereitung) sind Angaben des Autors ohne belegte Quelle. Einordnung der offiziellen Plugin-Sammlung: [Knowledge Work Plugins](Knowledge%20Work%20Plugins.md). [tweet-2027054100807106829](../sources/tweet-2027054100807106829.md)
