---
tags: [tools, product-building, agents]
sources: [tweet-2092994294282060147.md]
created: 2026-10-10
updated: 2026-10-10
---

# UI UX Pro Max

## Designsuche und Ergebnis (Stand 2026-08; gespeicherte README)

[nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) beschreibt einen Skill für Coding-Agenten, der Produktanforderungen mit durchsuchbaren Stilen, Farben, Typografie, Landingpage-Mustern und plattformspezifischen Regeln verbindet. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

Laut README rankt BM25 Designkandidaten; Produktregeln und Anti-Patterns führen zu einem Designsystem mit Layoutmuster, Stil, Palette, Typografie, Effekten und Prüfliste. Dies ist die dokumentierte Arbeitsweise, kein gemessener Qualitätsgewinn. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

Die Python-Suche benötigt Python 3 und nach README nur die Standardbibliothek; die Suchskripte installieren keine Software und machen keine Netzwerkaufrufe. Diese Aussage betrifft die Suche, nicht jede Installation oder spätere Agentenfunktion. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

## Persistenz und Bedienung (Stand 2026-08; gespeicherte README)

`search.py "SaaS dashboard" --design-system --persist -p "MyApp"` erzeugt laut README `design-system/myapp/MASTER.md`; `--page "dashboard"` ergänzt eine Datei unter pages für abweichende Seitenregeln. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

Der dokumentierte Folgeprompt verlangt zuerst MASTER.md und dann die passende pages-Datei; deren Regeln überschreiben den Master nur dort, wo die Datei vorhanden ist. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

Domänensuche deckt unter anderem Stil, Typografie, Charts, UX und Icons ab; `--stack` wählt plattformspezifische Vorgaben und `--json` vermeidet die Kürzung langer Felder im menschenlesbaren Ergebnis. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

Die gespeicherte README nennt Installation über Marketplace oder ui-ux-pro-max-cli mit `uipro init --ai <platform>`, einschließlich [Claude Code](Claude%20Code.md) und [Codex](Codex.md); sie unterscheidet die offene UI/UX-Basis von beworbenen Premium-Funktionen für Marken- und Assetgestaltung. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

## Prüfregeln und Katalogstände (Stand 2026-08; Online-Abgleich 2026-10-10)

Die README-Prüfliste nennt Textkontrast, sichtbaren Tastaturfokus, reduced-motion, Umbruch ohne Clipping und responsive Breiten; sie verlangt native Semantik und zugängliche vollständige Labels bei kompakten UI-Elementen. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

Tweet, tatsächlicher Screenshot und gespeicherte README zeigen verschiedene Katalogstände: Tweet 79 Stile/95 Paletten/56 Schriftpaare, Screenshot 57/95/56, README 79 durchsuchbare Stile mit 50 aktiven, 192 Paletten und 74 Schriftpaaren. Diese Zahlen werden nicht als konsistenter August-Snapshot ausgegeben. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

Die während der Triage am 2026-10-10 gelesene [aktuelle README](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) bestätigt 192 Paletten und 74 Schriftpaare; Tweet-Stars und Downloads sind unbestätigte Popularitätsangaben. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

Die beiden weiteren Raw-Kataloge mit identischer README sind keine unabhängigen Belege und wurden hier nicht ingestiert; dieser Werkzeugbeleg ergänzt [Design Skills for Coding Agents](../concepts/Design%20Skills%20for%20Coding%20Agents.md). [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

Es wurde kein Skill installiert und kein UI-Ergebnisvergleich durchgeführt; eine Regel- und Referenzdatenbank ersetzt keine Prüfung des konkreten Produktdesigns. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)
