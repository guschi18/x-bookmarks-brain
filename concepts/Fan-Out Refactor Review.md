---
tags: [agents, tools]
sources: [tweet-2103378606986863103.md]
created: 2026-10-03
updated: 2026-10-03
---

# Fan-Out Refactor Review

## Mechanismus

Ein Orchestrator kartiert Architektur und Konventionen des Repos, teilt es in Slices und schickt je Subsystem einen frischen read-only Agenten; danach validiert, dedupliziert und rankt er die Befunde. [tweet-2103378606986863103](../sources/tweet-2103378606986863103.md)

## Prüfkatalog

Die Checkliste nennt Smells (Bloaters, Object-orientation abusers, Change preventers, Dispensables, Couplers) und Architekturkriterien (SOLID, Boundaries and layering, Extension points, Consistency, Behaviour). [tweet-2103378606986863103](../sources/tweet-2103378606986863103.md)

## Grenzen

Der Autor erwartet echte Smells, toten Code, Duplikation und Architekturprobleme statt KI-Nitpicks; Ergebnisse der Agenten müssen verifiziert werden, eine Messung liegt nicht vor. Eingesetzt mit [Claude Opus 5.5](../entities/Claude%20Opus%205.5.md); verwandt mit [Prefactoring](Prefactoring.md). [tweet-2103378606986863103](../sources/tweet-2103378606986863103.md)
