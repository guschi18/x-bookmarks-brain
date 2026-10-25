---
tags: [marketing, agents, tools, product-building]
sources: []
created: 2026-10-10
updated: 2026-10-10
---

# Aaron Marketing Skills

## Quelle und Rolle (Stand 2026-10-10)

Diese Seite entstand auf ausdrücklichen Nutzerwunsch aus einer eigenständigen Repository-Recherche, ohne X-Bookmark. `sources: []` bedeutet, dass keine Tweet-Quelle beansprucht wird; die folgenden Aussagen tragen direkte GitHub-Belege. Geprüfter Stand ist Commit `67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6`, Bundle-Version 20.1.0. Die abgerufenen Primärdokumente sind unter output/aaron-marketing-* gesichert. [README](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/README.md)

Das Repo beschreibt ein Marketing-Team aus Markdown-Skills mit ergänzenden Bash-/Python-Runtimes für Validierung, Scoring, Ereignisregister und optionale Connectoren. Im gepinnten Git-Baum wurden 120 kanonische SKILL.md-Dateien gezählt: sieben Disziplinen mit jeweils sechzehn Skills plus acht Protokoll-Skills. Das erweitert die historische [SEO and GEO Skills Library](SEO%20and%20GEO%20Skills%20Library.md) zu einem umfassenderen System; der alte SEO/GEO-Standalone-Stand bleibt als v9.9.12 erhalten. [Katalog](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/references/system-catalog.json), [Repo-Familie](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/docs/repo-family.md)

## Disziplinen und gemeinsame Steuerung

| Bereich | Wiederkehrender Ablauf | Beispiele und Audit |
| --- | --- | --- |
| Narrative | Trace → Architect → Land → Evaluate | Positionierung, Message-System, Belegpakete; TALE |
| SEO/GEO | Survey → Implement → Tune → Evaluate | Keywords, Content, technische Prüfung; CORE-EEAT und CITE |
| Social | Explore → Craft → Host → Observe | Kanalwahl, Kalender, Kurzvideos; ECHO |
| Email | Setup → Engage → Nurture → Deliver | Segmente, Sequenzen, Zustellprüfung; SEND |
| Paid Ads | Research → Orchestrate → Activate → Scale | Kampagnen, Creatives, Budget und Attribution; ROAS |
| Influencer | Scout → Target → Activate → Report | Creator-Suche, Fit, Briefing und Reporting; STAR |
| Launch | Research → Assemble → Mobilize → Prove | Launch-Plan, Assets, Readiness und Rückblick; RAMP |

Die Tabelle fasst den versionierten Katalog zusammen. Die Framework-Namen sind projekteigene Qualitätsverfahren und keine unabhängig belegten Ranking-, Conversion- oder ROI-Prädiktoren. Die vier Architekturebenen sind Narrative, laufende Kanäle, zeitgebundener Launch und gemeinsames Protokoll. [Architektur](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/docs/system-architecture.md)

Sieben Register halten Entities, Creator, Claims/Angebote, Consent, Launches, Kanäle und Narrative als Ereignisströme mit daraus abgeleiteten Projektionen. Writer schlagen neue Claims vor; nur ein Principal mit Host-Capability darf sie kanonisch annehmen. Das gelesene offer-claims-registry verlangt exakten Wortlaut, Beleg, Datum, Bedingungen und offene Evidenzlücken statt erfundener Substantiierung. [Registry-Skill](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/protocol/offer-claims-registry/SKILL.md)

## Konkreter Content-Ablauf

Der gelesene content-writer unterscheidet neue Texte und Refresh bestehender Seiten. Er liest Brief, Zielkeyword sowie akzeptierte Narrative-/Claims-Projektionen, kennzeichnet fehlende Belege und übergibt einen stabilen Page-/Content-/Hash-/Change-Bezug. Bei Refresh kommen Traffic-/Rankinghistorie und der vorherige Textstand hinzu. Ohne Analytics darf er anhand der Seite weiterarbeiten, muss die Diagnose dann als Schätzung markieren. [Content Writer](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/seo-geo/implement/content-writer/SKILL.md)

Der content-quality-auditor bewertet separat achtzig CORE-EEAT-Items. Applicable, aber unbeobachtete Evidenz bleibt Unknown; sie wird nicht als N/A behandelt oder aus den Gewichten herausgerechnet. Ohne Scorer, Validator und Katalog muss der Skill `NOT_SCORED` liefern, statt einen Score oder eine Freigabe zu erfinden. Die möglichen Audit-Verdicts heißen SHIP, FIX, BLOCK und UNDECIDED; laut Skill sind Scores Beratung, keine Ranking-/Zitationsvorhersage. [Auditor](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/seo-geo/tune/content-quality-auditor/SKILL.md)

Der gemeinsame Vertrag begrenzt automatische Weitergaben auf einen eindeutigen nächsten Skill, eine besuchte Menge und höchstens drei Handoffs nach dem Ursprung. Evidence, Annahmen, offene Punkte und nächster Schritt werden ausdrücklich übergeben; ein Verweis auf einen Auditor allein autorisiert dessen Ausführung nicht. [Skill Contract](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/references/skill-contract.md)

## Installation und reale Grenzen der Pakete

Die README nennt für [Claude Code](Claude%20Code.md) Marketplace-Registrierung plus Plugin-Installation und für portable Skill-Hosts `npx skills add aaron-he-zhu/aaron-marketing-skills`. Ein einzelner Einstieg ist `npx skills add aaron-he-zhu/aaron-marketing-skills -s keyword-research`. Diese Befehle sind dokumentiert, wurden hier aber nicht ausgeführt; die Sammlung wurde nicht in die lokalen Agenten installiert. [Installationswege](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/README.md#install)

Portable Lite enthält statische Skills und Referenzen, aber keine ausführbaren Repo-Runtimes, Hooks, Controller oder MCP-Registrierung. Grok-/Hermes-Bot-Pakete teilen 120 Skills auf sieben Spezialisten und aaron-chief auf; Grok verlangt halbmanuelle Einrichtung. Diese statischen Bots bleiben bei Audits NOT_SCORED und Registern propose-only. Alle Grok-Bots eines Accounts teilen einen Cloud-Computer: Bot-Namen isolieren Dateien, Browser-Sitzungen oder Logins nicht. [Bot-Installation und Grenzen](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/docs/ai-staff-install.md)

Skills arbeiten laut Doku mit eingefügten Daten ohne zwingende APIs; zusätzliche Connectoren sind optional. Die öffentliche OSS-Fläche liefert kein gehostetes Marketing-Dashboard oder Usage-Gateway. Ein lokaler skill-dashboard.py projiziert eigene Run-Artefakte in eine HTML-Seite. Versand, Veröffentlichung und externe Änderungen bleiben eigene autorisierungspflichtige Aktionen; Social-Posting-, Engagement- und DM-Automation wird in der README ausgeschlossen. [README](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/README.md), [Connectoren](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/CONNECTORS.md)

## Evidenz und praktische Einordnung

Die README beschreibt Engineering-Prüfungen und simulierte Provider-Fixtures, erklärt reale Projektergebnisse aber weiterhin als unvalidiert. Lite bleibt der Default; Governed ist kein Beweis besserer Geschäftsergebnisse. Auch vorhandene CI, Scoring-Schemata und umfangreiche Regeln belegen weder Suchranking noch Marketing-Ertrag. Die Lizenz ist Apache-2.0. [Validierungsgrenzen](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/README.md#more), [Lizenz](https://github.com/aaron-he-zhu/aaron-marketing-skills/blob/67e7bb2c8d5a21496dcf9c4c6f3cebfab89814a6/LICENSE)

Für die Wissensbasis sind insbesondere die Trennung von Schreiben und Audit, versionierte Claim-Provenienz und explizite fehlende Evidenz wiederverwendbar. Ein kleiner Einstieg mit Brief und einem Schreib-/Prüfpfad erscheint leichter beurteilbar als sofortige Einrichtung aller acht Bots; dies ist die Einordnung dieser Recherche. [Generative Search Optimization](../concepts/Generative%20Search%20Optimization.md) bleibt der getrennte Maßstab für die bereits dokumentierten Google-Anforderungen.

Gelesen wurden README, Katalog, Architektur, gemeinsamer Vertrag, Repo-Familie, Bot-Anleitung, Connector-/Privacy-/Security-Dokumentation sowie konkrete Content-Writer-, Content-Auditor- und Claims-Registry-Dateien. Die 120-Datei-Zählung ist geprüft; nicht alle Skill-Prompts wurden einzeln bewertet. Installation, Runtime, Connectoren und reale Marketingwirkung wurden nicht getestet.
