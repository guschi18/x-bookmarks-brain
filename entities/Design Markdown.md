---
tags: [agents, tools, product-building]
sources: [tweet-2046624729403142320.md]
created: 2026-10-20
updated: 2026-10-20
---

# Design Markdown

## Format und Zweck (Stand 2026-04)

DESIGN.md beschreibt laut offiziellem Stitch-Vortrag eine visuelle Identität als dauerhaft lesbaren Agentenkontext: Farbrollen, Typografie und Gestaltungsregeln stehen zusammen mit ihrer Begründung. Stitch und andere Agenten sollen so dieselben Designentscheidungen verwenden können; der April-Post kündigt den ersten öffentlichen Spezifikationsentwurf an. [tweet-2046624729403142320](../sources/tweet-2046624729403142320.md)

## Rollen, Tokens und Komponenten (Stand 2026-04)

Das Video verbindet menschenlesbare Begründungen mit genauen Werten im YAML-Tokenbereich: Eine primary-Farbe ist eine benannte Rolle, deren aktueller Wert ein Hexcode ist; Typografierollen beschreiben Schrift und Größe. Die gemeinsame Datei soll ein Auseinanderlaufen von Styleguide und separater Token-Konfiguration vermeiden. Das ist die Begründung des Vortragenden, kein gemessener Driftvergleich. [tweet-2046624729403142320](../sources/tweet-2046624729403142320.md)

Komponenten können auf diese Rollen verweisen; die gezeigte Hover-Variante überschreibt nur den Hintergrund. Der Sprecher bezeichnet den Komponentenabschnitt ausdrücklich als in Arbeit und bittet um Feedback. Dieser Entwurfsstatus wird nicht als abgeschlossene Spezifikation umgedeutet. [tweet-2046624729403142320](../sources/tweet-2046624729403142320.md)

## Gezeigte Prüfschleife (Stand 2026-04)

Ein Agent liest die Datei, ergänzt einen Accent-Button und lässt den Entwurf per CLI prüfen. Ein Kontrastbefund zeigt eine ungeeignete Text-/Hintergrundkombination; der Agent kann sie korrigieren oder begründet überschreiben. Die Demo belegt eine Rückkopplung für dokumentierte Designwerte, keine vollständige WCAG-Prüfung der später gerenderten Anwendung. [tweet-2046624729403142320](../sources/tweet-2046624729403142320.md)

## Ergänzender Primärabgleich (Stand 2026-10, geprüft 2026-10-20)

Das [offizielle Repository](https://github.com/google-labs-code/design.md) bestätigt Tokens plus Markdown-Begründung und dokumentiert `npx @google/design.md lint DESIGN.md` für strukturierte Befunde zu Format, Referenzen und Kontrast. Dieser später gelesene Befehl wird nicht als im gespeicherten April-Transkript wörtlich enthalten ausgegeben. [tweet-2046624729403142320](../sources/tweet-2046624729403142320.md)

## Zusammenhang mit Design-Workflows (Stand 2026-04)

Die Datei liefert einen formalen Kontextbaustein für [Design Skills for Coding Agents](../concepts/Design%20Skills%20for%20Coding%20Agents.md). Die Quelle demonstriert das Format, installiert hier aber weder CLI noch Agenten-Integration und liefert keinen unabhängigen Qualitätsvergleich. [tweet-2046624729403142320](../sources/tweet-2046624729403142320.md)
