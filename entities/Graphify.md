---
tags: [agents, tools, research, security]
sources: [tweet-2111838109029552334.md]
created: 2026-10-23
updated: 2026-10-23
---

# Graphify

## Rolle und dokumentierte Ausgaben (Stand 2026-10)

[Graphify](https://github.com/Graphify-Labs/graphify) macht laut gespeichertem Organisationsprofil einen Ordner aus Code, Dokumenten, PDFs, Bildern oder Video als Wissensgraph abfragbar. Genannt werden graph.html als interaktive Ansicht, GRAPH_REPORT.md als Zusammenfassung und graph.json als strukturierte Ausgabe. Es ist ein eigenständiger Werkzeugpfad von [Agentic Knowledge Graph Construction](../concepts/Agentic%20Knowledge%20Graph%20Construction.md). [tweet-2111838109029552334](../sources/tweet-2111838109029552334.md)

Code wird laut Anbieter lokal mit tree-sitter über rund 40 Sprachen analysiert; andere Medien erhalten einen semantischen Durchlauf über das Assistenzmodell oder einen konfigurierten Schlüssel. Aussagen über lokale, kostenfreie Code-Analyse gelten deshalb nicht pauschal für jede Dokument-/Medienverarbeitung. Kanten heißen EXTRACTED oder INFERRED; diese Kennzeichnung ist keine unabhängige Validierung. [tweet-2111838109029552334](../sources/tweet-2111838109029552334.md)

## Einstieg und persönliche Agenten-Einrichtung (Stand 2026-10)

Der Post nennt uv tool install graphifyy, dann graphify install und /graphify . im Arbeitsordner. Das gespeicherte Profil bestätigt diese Namen und verweist auf [PyPI](https://pypi.org/project/graphifyy/). Nichts wurde hier installiert. [tweet-2111838109029552334](../sources/tweet-2111838109029552334.md)

Die weitergehende Anleitung der Autorin kombiniert einen AGENT-Ordner mit CLAUDE.md und memory/, npm install -g @googleworkspace/cli mit gws auth setup, claude mcp add playwright npx @playwright/mcp@latest, Graphify sowie npm i -g jev-guard und jev-guard install claude. Eine abschließende Morgenroutine soll Eingänge, Entwürfe und offene Freigaben melden. Dies sind gespeicherte Community-Befehle, keine hier getestete plattformübergreifende Einrichtung; Jev-Guard-Schlüsselwerte werden nicht übernommen. [tweet-2111838109029552334](../sources/tweet-2111838109029552334.md)

## Open Source, Enterprise und Evidenzgrenzen (Stand 2026-10)

Das Anbieterprofil trennt den offenen lokalen Graphen von Enterprise mit behaupteter formaler Verifikation, MCP-Fact-Checking, Team-PR-Gates, SSO und Audit. Die Verifikations- und Datenschutzversprechen sind Herstellerangaben, kein im Bookmark reproduzierter Beweis für sichere Änderungen. [tweet-2111838109029552334](../sources/tweet-2111838109029552334.md)

Die Autorin nennt 126k GitHub-Sterne, YC-Aufnahme, 15 Minuten Einrichtung und einen Jev-Guard-Preis von etwa vier Cent pro tausend Checks. Diese Zahlen und die behauptete Blockierung gefährlicher Aktionen wurden nicht unabhängig geprüft. Das Demo-Video hat ein leeres Transkript; substantieller Beleg sind der vollständige Post, das Anbieterprofil und dessen direkte Links. Verwandte Rollen: [Claude Code](Claude%20Code.md) als Agent und [Jev](Jev.md) als beworbene Entscheidungsschicht. [tweet-2111838109029552334](../sources/tweet-2111838109029552334.md)
