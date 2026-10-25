---
tags: [tools, product-building, agents]
sources: [tweet-2098224649762984168.md]
created: 2026-10-09
updated: 2026-10-09
---

# SkillUI

## Zweck und Quellen (Stand 2026-09)

[amaancoderx/npxskillui](https://github.com/amaancoderx/npxskillui) beschreibt eine MIT-lizenzierte CLI zur Extraktion von Designsystemen ohne Modellaufrufe oder AI-API-Schlüssel. `skillui --url https://example.com`, `skillui --dir ./project` und `skillui --repo https://github.com/org/repo` lesen Website, lokalen Code oder ein geklontes öffentliches Repository. Lokale Scans suchen CSS/SCSS, JS/TS-Komponenten, Tailwind-Konfiguration und CSS-Variablen. [tweet-2098224649762984168](../sources/tweet-2098224649762984168.md)

## Ausgabe und Arbeitsablauf (Stand 2026-09)

Das Ergebnis enthält Farben-, Abstands- und Typografie-JSON, DESIGN.md, CLAUDE.md, SKILL.md, ein .skill-ZIP und je nach Modus Referenzdateien, Bilder und Fonts. Der vorgeschlagene Ablauf öffnet den Ausgabeordner in [Claude Code](Claude%20Code.md) und bittet um eine UI anhand des extrahierten Designs. Automatisches Laden aller Artefakte und exakte Reproduktion sind README-Aussagen, hier nicht praktisch geprüft. [tweet-2098224649762984168](../sources/tweet-2098224649762984168.md)

## Ultra-Modus und Grenzen (Stand 2026-09)

`--mode ultra` verwendet laut README Playwright für Scroll-Screenshots, Hover-/Focus-Diffs, Animationen, Layout und DOM-Komponenten; dafür werden Playwright und Chromium zusätzlich installiert. Als Grundvoraussetzung ist Node.js 18+ genannt. Die README beschreibt den Standardmodus als browserlose statische Analyse, erwähnt im Abschnitt How It Works für URL-Auswertung jedoch ebenfalls Playwright-DOM-Inspektion; Browserbedarf und vollständige Extraktion bleiben daher ungeprüft. [tweet-2098224649762984168](../sources/tweet-2098224649762984168.md)

[Dembrandt](Dembrandt.md) ist eine verwandte Ressource für [Design Skills for Coding Agents](../concepts/Design%20Skills%20for%20Coding%20Agents.md). SkillUI dokumentiert insbesondere lokale Code-/Repo-Scans und die Verpackung von Designkontext als Skill, weshalb die zwei Bookmarks keine identischen Arbeitsanleitungen sind. [tweet-2098224649762984168](../sources/tweet-2098224649762984168.md)
