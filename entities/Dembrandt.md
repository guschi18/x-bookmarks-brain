---
tags: [tools, product-building]
sources: [tweet-2097134648270766520.md]
created: 2026-10-09
updated: 2026-10-09
---

# Dembrandt

## Extraktion (Stand 2026-09)

[dembrandt/dembrandt](https://github.com/dembrandt/dembrandt) beschreibt eine MIT-lizenzierte CLI, die eine Website in Playwright rendert und berechnete DOM-Stile auswertet: Farben, Typografie, Abstände, Rahmen, Schatten, Bewegung, Komponenten und Breakpoints. Gruppierung und Konfidenzbewertung sollen beobachtete Muster als Design-Tokens aufbereiten. [tweet-2097134648270766520](../sources/tweet-2097134648270766520.md)

## Einrichtung und Ausgaben (Stand 2026-09)

Die README nennt `npm install -g dembrandt`, anschließend zwingend `dembrandt install-browser`, dann `dembrandt example.com`. Auch bei npx ist der Browserdownload separat nötig, weil playwright-core keine Browser mitliefert; Voraussetzung ist Node.js 18+. [tweet-2097134648270766520](../sources/tweet-2097134648270766520.md)

`--dtcg` exportiert W3C/DTCG-Tokens, `--design-md` Agentenkontext und `--tailwind` beobachtete Werte als Tailwind-v4-Theme. `--crawl 10` führt mehrere Seiten zusammen; `--wcag` prüft Kontrast an tatsächlichen DOM-Paaren. Die getrennten Ausgaben machen das Werkzeug zu einer Ressource für [Design Skills for Coding Agents](../concepts/Design%20Skills%20for%20Coding%20Agents.md). [tweet-2097134648270766520](../sources/tweet-2097134648270766520.md)

## Driftprüfung und MCP (Stand 2026-09)

`--compare baseline.json --json-only` vergleicht einen Snapshot mit einer gespeicherten Baseline und beendet sich bei Drift mit Exitcode 1. Der MCP-Aufruf `claude mcp add --transport stdio dembrandt -- npx -y --package dembrandt dembrandt-mcp` bindet Extraktions- und Analysewerkzeuge ein; Extraktion liefert eine job_id, die mit get_job_status abgefragt und an reine Analysewerkzeuge weitergereicht wird. [tweet-2097134648270766520](../sources/tweet-2097134648270766520.md)

## Grenzen und verwandtes Werkzeug (Stand 2026-09)

Canvas/WebGL ohne DOM ist nicht analysierbar; dynamische Inhalte können fehlen, Dark Mode braucht ein Flag und Hover-/Focus-Angaben stammen aus CSS statt vollständiger Interaktion. Extraktionsqualität und CI-Ergebnisse wurden hier nicht gemessen. [SkillUI](SkillUI.md) ist ein verwandtes Werkzeug, dessen Schwerpunkt auf der Verpackung von Designkontext als Skill liegt; Dembrandt dokumentiert insbesondere Token-Ausgaben und Baseline-Vergleiche. [tweet-2097134648270766520](../sources/tweet-2097134648270766520.md)
