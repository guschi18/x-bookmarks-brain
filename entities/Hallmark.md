---
tags: [agents, tools, product-building]
sources: [tweet-2113506956933476634.md]
created: 2026-10-24
updated: 2026-10-24
---

# Hallmark

## Überblick (Stand 2026-10)

Hallmark ist ein Design-Skill von Together AI für Claude Code, Codex, Cursor und OpenCode (https://github.com/Nutlope/hallmark, https://www.usehallmark.com/). Er soll Seiten bauen, die nicht wie KI-Ausgaben aussehen. Der Post nennt 30,8K Sterne und MIT-Lizenz. [tweet-2113506956933476634](../sources/tweet-2113506956933476634.md)

## Mechanismus (Stand 2026-10)

Laut README wählt Hallmark aus 48 Themes (Material mit Typografie, Farbe, Oberflächen, Komponenten), baut die Seite aus dem Zweck der Besucher (Buchungsseite bucht, Shop verkauft) und prüft das Ergebnis mit `sloplint --render` bei acht Breiten. Danach entscheidet ein Subagent mit frischem Kontext. [tweet-2113506956933476634](../sources/tweet-2113506956933476634.md)

Die Gates haben drei Stufen: Floor (Kontrast, Fokus, Reduced Motion, erfundene Fakten, kaputtes Mobil-Layout) blockiert immer; Reflex-Gates dürfen mit Begründung übergangen werden; Finish-Checks blockieren nie. [tweet-2113506956933476634](../sources/tweet-2113506956933476634.md)

## Bedienung (Stand 2026-10)

Installation: `npx skills add nutlope/hallmark -g`, Node 18+; Browserchecks brauchen puppeteer-core und Chrome. Aufruf `/hallmark <Prompt>`, `/hallmark redesign <Pfad>` behält Inhalt und Verdrahtung, `/hallmark audit <Pfad>` meldet nur. [tweet-2113506956933476634](../sources/tweet-2113506956933476634.md)

## Grenzen

Alle Qualitäts- und Neuheitsaussagen sind Herstellerangaben; es liegt kein unabhängiger Test vor. Einordnung unter [Design Skills for Coding Agents](../concepts/Design%20Skills%20for%20Coding%20Agents.md). [tweet-2113506956933476634](../sources/tweet-2113506956933476634.md)
