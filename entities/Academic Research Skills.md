---
tags: [agents, tools, research]
sources: [tweet-2050830036052086968.md]
created: 2026-10-15
updated: 2026-10-15
---

# Academic Research Skills

## Projekt und unterschiedliche Stände (Poststand 2026-05; README bis 2026-09)

[Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) ist laut gespeicherter README eine Sammlung für Recherche, wissenschaftliches Schreiben, Review und Überarbeitung mit [Claude Code](Claude%20Code.md). Der Post vom 03.05.2026 und sein Screenshot zeigen v3.6.7; der später erfasste README-Text enthält Änderungen bis v3.22.2 vom 25.09.2026. Die folgenden späteren Details dürfen nicht als Funktionsumfang des Mai-Screenshots gelesen werden. [tweet-2050830036052086968](../sources/tweet-2050830036052086968.md)

## Einstieg (gespeicherter README-Stand 2026-09)

Die README nennt für die Plugin-Installation die folgenden Befehle und schlägt danach /ars-plan oder /ars-lit-review vor. Die Installation wurde hier nicht ausgeführt. [tweet-2050830036052086968](../sources/tweet-2050830036052086968.md)

```text
/plugin marketplace add Imbad0202/academic-research-skills
/plugin install academic-research-skills
```

Claude Code ist Voraussetzung; Pandoc für DOCX sowie tectonic und passende Fonts für PDF sind optional. Die Kern-Skills sind promptbasiert, einzelne Schutz- und Zusatzfunktionen benötigen Python. Der dokumentierte Funktionsumfang hängt vom Installationskanal ab. [tweet-2050830036052086968](../sources/tweet-2050830036052086968.md)

Die README verlinkt einen eigenen [Codex-Ableger](https://github.com/Imbad0202/academic-research-skills-codex) mit academic-research-suite und ars-Aliasnamen; Pi und Claude-Science-Import werden ebenfalls beschrieben. Ein Import von Methodeninhalten überträgt laut README nicht automatisch Claude-Code-Hooks, Commands und Subagent-Orchestrierung. [tweet-2050830036052086968](../sources/tweet-2050830036052086968.md)

## Forschungs- und Schreibablauf (gespeicherter README-Stand 2026-09)

Vier Skill-Gruppen decken Deep Research, Academic Paper, Academic Paper Reviewer und Academic Pipeline ab. Genannte Modi sind Literaturreview, PRISMA-Review, Faktenprüfung, sokratische Planung, Gliederung, Schreiben, Revisionsbegleitung, Zitationsprüfung, Abstracts und Formatkonvertierung. Der Orchestrator verbindet sie über dokumentierte Artefakte und menschliche Bestätigungen. [tweet-2050830036052086968](../sources/tweet-2050830036052086968.md)

Ein Material Passport hält Eingaben und Provenienz fest. Die README beschreibt verpflichtende Integritätsprüfungen vor und nach Review, optionale modellübergreifende Gegenprüfung, Herkunfts- und Locator-Angaben für Zitate sowie eine Zuordnung von Reviewer-Bedenken zu Änderungsbehauptungen und erneuter Prüfung. Experimente werden nicht durch die Suite als empirisch korrekt nachgewiesen; extern erstellte Ergebnisse werden mit ihrer deklarierten Provenienz aufgenommen. [tweet-2050830036052086968](../sources/tweet-2050830036052086968.md)

Die späteren Erweiterungen umfassen ein Run-Ledger für Anweisungen, Kontrollfragen, Nutzerantworten und Dateihashes sowie eine deterministische Akronymprüfung. Die README trennt synthetische Tests dieser Hilfsmittel von einer noch nicht gemessenen Wirksamkeit der Promptregeln. [tweet-2050830036052086968](../sources/tweet-2050830036052086968.md)

## Grenzen, Kalibrierung und Lizenz (gespeicherter README-Stand 2026-09)

Die Suite beschreibt sich als Unterstützung menschlicher Forschung: Fragestellung, Methodenwahl, Interpretation und Verantwortung bleiben beim Menschen. Kontrollpunkte sind teilweise Promptprotokolle und keine Laufzeitgarantie. Quellenexistenz, Zitatausrichtung und konsistente Prozessberichte belegen weder authentische Rohdaten noch tatsächlich ausgeführte Experimente oder Reproduzierbarkeit; konsistent berichtete Erfindungen können solche Prüfungen passieren. [tweet-2050830036052086968](../sources/tweet-2050830036052086968.md)

Die README bezeichnet laufende Reviews als NOT_CALIBRATED und erklärt, dass ein kalibriertes Kandidatenprofil noch nicht in Live-Reviews angewendet wird. Ein früher Showcase verbleibt ein historischer Lauf: Ein separater nachträglicher Audit fand bei 21 von 68 Referenzen trotz vorheriger Integritätsrunden Probleme. Das ist ein dokumentiertes Gegenbeispiel zur Annahme garantierter Zitierzuverlässigkeit, keine aktuelle Fehlerrate der Suite. [tweet-2050830036052086968](../sources/tweet-2050830036052086968.md)

Die gespeicherte Lizenz ist CC BY-NC 4.0: Weitergabe und Anpassung mit Namensnennung, jedoch keine kommerzielle Nutzung unter dieser Lizenz. Verlinkte Datenflüsse, Setup- und Architekturhinweise sowie alle 80 Original-Artikellinks stehen vollständig auf der Source. Installation, Kosten und Ergebnisqualität wurden hier nicht unabhängig geprüft. [tweet-2050830036052086968](../sources/tweet-2050830036052086968.md)
