---
tags: [product-building, tools]
sources: [tweet-2030433563770855683.md, tweet-2100842257804841326.md]
created: 2026-10-02
updated: 2026-10-07
---

# Taste Skill

## Rolle (Stand 2026-03)

Leonxlnx/taste-skill ist laut gespeicherter README eine Sammlung portabler Agent Skills, die KI-gebaute Oberflächen bei Layout, Typografie, Motion und Abständen verbessern sollen. Autor ist Leon Lin, der sie in seinem Profilpost als seine geteilten Skills verlinkt. [tweet-2030433563770855683](../sources/tweet-2030433563770855683.md)

## Varianten (Stand 2026-03)

- design-taste-frontend (v2, experimentell): leitet die Designsprache aus dem Briefing ab, nutzt GSAP-Skelette, ein striktes Em-Dash-Verbot, ein Redesign-Audit und einen Pre-Flight-Check; v1 bleibt separat installierbar. [tweet-2030433563770855683](../sources/tweet-2030433563770855683.md)
- gpt-taste für GPT/Codex mit stärkerer Layoutvarianz, image-to-code, redesign-existing-projects, full-output-enforcement gegen abgebrochene Ausgaben sowie Stilvarianten soft, minimalist, brutalist und eine Google-Stitch-Variante. [tweet-2030433563770855683](../sources/tweet-2030433563770855683.md)
- Bildgenerierungs-Skills für Website-, Mobile- und Brandkit-Boards, deren Bilder anschließend an [Codex](Codex.md), Cursor oder [Claude Code](Claude%20Code.md) übergeben werden. [tweet-2030433563770855683](../sources/tweet-2030433563770855683.md)

## Einstellung und Installation (Stand 2026-03)

Der Haupt-Skill hat drei Regler von 1 bis 10: DESIGN_VARIANCE, MOTION_INTENSITY und VISUAL_DENSITY. Installiert wird mit npx skills add https://github.com/Leonxlnx/taste-skill, ein einzelner Skill über --skill und seinen Installationsnamen; alternativ lässt sich die SKILL.md kopieren. [tweet-2030433563770855683](../sources/tweet-2030433563770855683.md)

## Grenzen (Stand 2026-03)

Die README enthält Sponsoren- und einen Kimi-Affiliate-Link sowie eine Distanzierung von Krypto-Token im Namen des Projekts. Qualitätswirkung und Unterschiede zwischen den Varianten sind nicht unabhängig gemessen. [Design Skills for Coding Agents](../concepts/Design%20Skills%20for%20Coding%20Agents.md) ordnet die Sammlung neben anderen Design-Skills ein. [tweet-2030433563770855683](../sources/tweet-2030433563770855683.md)

## Weiteres Projekt des Autors (Stand 2026-09)

[TasteCode](TasteCode.md) ist Leon Lins separate Desktop-Oberfläche für Coding-Agenten mit eingebautem Design Mode; die gespeicherte Ankündigung nennt ihn und @blueemi99 als Entwickler. Das Projekt ist eine Anwendung, nicht eine weitere Variante der Skill-Sammlung. [tweet-2100842257804841326](../sources/tweet-2100842257804841326.md)
