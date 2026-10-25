---
tags: [tools, product-building]
sources: [tweet-2055333192366735670.md]
created: 2026-10-01
updated: 2026-10-01
---

# CheckMyGit

## Produkt (Stand 2026-05)

[whoisyurii/checkmygit](https://github.com/whoisyurii/checkmygit) beschreibt ein Werkzeug, das einen GitHub-Nutzernamen in ein teilbares Portfolio umwandelt. Die gespeicherte README verlinkt die [Demo](https://checkmygit.com/) und nennt keine Anmeldung für die Nutzung. [tweet-2055333192366735670](../sources/tweet-2055333192366735670.md)

## Dokumentierter Funktionsumfang

Die README nennt drei Vorlagen: GitHub-Sidebar, Bento-Grid und Minimal-CV. Sie führt Jahres-Beitragsgraph, Sprachenstatistik, hervorgehobene Projekte, PNG-Export und teilbare URLs wie checkmygit.com/username?template=bento auf. Das sind Projektangaben, keine im Ingest ausgeführten Funktionstests. [tweet-2055333192366735670](../sources/tweet-2055333192366735670.md)

## Technik und Eigenbetrieb

Als Stack nennt das Projekt SvelteKit 2, Svelte 5 Runes, Tailwind CSS 4, GitHub GraphQL mit REST-Fallback, Cloudflare Pages und html-to-image. Für Eigenbetrieb empfiehlt es optional einen GitHub-Token mit read:user gegen Rate Limits; „keine Anmeldung“ für Nutzer bedeutet deshalb nicht, dass jede Bereitstellung ohne API-Zugang auskommt. [tweet-2055333192366735670](../sources/tweet-2055333192366735670.md)

## Roadmap und Grenze

PDF-Export, zusätzliche Vorlagen, dynamische OG-Bilder, Theme-Schalter und eigene Akzentfarben stehen unter Roadmap und werden hier nicht als bereits verfügbar dargestellt. Die README nennt MIT; Geschwindigkeit und Portfolioqualität sind nicht unabhängig gemessen. [tweet-2055333192366735670](../sources/tweet-2055333192366735670.md)
