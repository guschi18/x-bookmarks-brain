---
tags: [tools, product-building]
sources: [tweet-2087873421094896122.md]
created: 2026-10-12
updated: 2026-10-12
---

# Diagram Design

## Rolle und Versionen (Stand 2026-08; gespeicherter README-Stand)

[cathrynlavery/diagram-design](https://github.com/cathrynlavery/diagram-design) ist ein Agent-Skill für editoriale HTML/SVG-Diagramme. Der August-Tweet nennt 29 Typen; die gespeicherte README beschreibt spätere 2.x-Erweiterungen einschließlich weiterer Layoutgrammatiken. Diese Aussagen sind verschiedene Dokumentstände, kein gesicherter historischer Featureumfang. [tweet-2087873421094896122](../sources/tweet-2087873421094896122.md)

## Gestaltung und Wiederverwendung

Die README bietet helle, dunkle und editoriale Varianten, semantische Verhaltensmuster getrennt vom Layout und statische Ausgabe als Standard. Brand-Onboarding extrahiert Palette und Schrift eines Referenzauftritts; benannte Profile und eine .diagram-design-Projektmarkierung trennen mehrere Marken. [tweet-2087873421094896122](../sources/tweet-2087873421094896122.md)

Der Import aus draw.io, Mermaid und Excalidraw zeichnet Inhalte mit eigener Gestaltung neu; Format, Zielgröße, Detail und Publikum steuern das Ergebnis. Ein Fidelity Ledger nennt zusammengeführte und ausgelassene Elemente. PNG-Export nutzt Playwright, SVG bleibt editierbar. [tweet-2087873421094896122](../sources/tweet-2087873421094896122.md)

## Prüfung und Grenzen

Dokumentiert sind Skin-/Geometrieprüfungen, gerenderte Clipping-Kontrolle, zugängliche SVG-Namen und Beschreibung sowie Reduced-Motion-Verhalten für optionale Animation. Ein installiertes self_check.py prüft erzeugte Diagramme; diese Checks sind dokumentierte Mechanismen, keine hier reproduzierte Qualitätsgarantie. [tweet-2087873421094896122](../sources/tweet-2087873421094896122.md)

Für Routinen sollen nur der gewählte Typ und nötige Referenzen geladen werden. Die README verlangt eine inhaltliche Begründung für Diagramme und empfiehlt bei einfachen Listen oder Vergleichen Text beziehungsweise Tabellen; Netzwerkfreiheit hat im dokumentierten Ablauf eine Ausnahme für Google Fonts. [tweet-2087873421094896122](../sources/tweet-2087873421094896122.md)

[Design Skills for Coding Agents](../concepts/Design%20Skills%20for%20Coding%20Agents.md) ordnet das Werkzeug neben andere Gestaltungs-Skills ein; Sterne und Werbesprache sind keine unabhängige Bewertung. [tweet-2087873421094896122](../sources/tweet-2087873421094896122.md)
