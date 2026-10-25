---
tags: [agents, tools]
sources: [tweet-2021517290320130103.md]
created: 2026-10-24
updated: 2026-10-24
---

# Claude Skills Guide

## Definition (Stand 2026-02)

Anthropic veröffentlichte einen Leitfaden "The Complete Guide to Building Skills for Claude" (laut Post 32 Seiten, laut Bild-Beschreibung 33). Ein Skill ist ein Ordner mit Anweisungen, der Claude eine Aufgabe einmal beibringt. MCP gibt Claude Zugriff auf Werkzeuge wie Notion, Linear oder Figma; Skills lehren, sie so zu nutzen, wie das Team arbeitet. Das Wissen stammt aus einer Zusammenfassung des Autors Harshil Tomar, nicht aus dem PDF. [tweet-2021517290320130103](../sources/tweet-2021517290320130103.md)

## Anwendungsfälle

Dokumenterstellung (konsistente Ergebnisse nach den eigenen Standards, ohne Style Guides neu zu erklären), Workflow-Automatisierung (mehrstufige Abläufe, etwa Sprint-Planung mit Status, Velocity, Prioritäten und Aufgaben) und MCP-Erweiterung (Fachwissen über Werkzeugzugriff legen). [tweet-2021517290320130103](../sources/tweet-2021517290320130103.md)

## Aufbau

Pflicht ist eine SKILL.md mit YAML-Frontmatter; optional sind Skripte, Referenzdokumente und Vorlagen. Das Frontmatter entscheidet, wann Claude den Skill lädt, ohne unnötig Kontext zu verbrauchen; wichtig sind name (kebab-case, keine Leerzeichen) und description (was er tut und wann er auslöst). Eine falsche Beschreibung führt laut Autor dazu, dass der Skill nie lädt. [tweet-2021517290320130103](../sources/tweet-2021517290320130103.md)

Das offene Format beschreibt agentskills.io: Agenten laden Skills in drei Stufen, Discovery (nur Name und Beschreibung beim Start), Activation (volle SKILL.md bei passender Aufgabe) und Execution (Skripte oder Referenzdateien nach Bedarf), sodass viele Skills mit kleinem Kontextbedarf bereitstehen. Das Format wurde von Anthropic entwickelt und als offener Standard freigegeben. [tweet-2021517290320130103](../sources/tweet-2021517290320130103.md)

## Fünf Muster und vier Fehler

Muster: Sequential Workflow (feste Schrittfolge, z. B. Onboarding oder Deployment), Multi-MCP Coordination (mehrere Dienste, z. B. Figma, Linear, Slack), Iterative Refinement (Validierungsschleifen, z. B. Berichte mit Qualitätsprüfung), Context-Aware Selection (gleiches Ziel, andere Werkzeuge je nach Dateityp, Größe oder Kontext) und Domain Intelligence (Fachregeln über den Werkzeugzugriff hinaus, z. B. Compliance). [tweet-2021517290320130103](../sources/tweet-2021517290320130103.md)

Fehler: vage Beschreibungen, die nie auslösen; Anweisungen, die in langem Text untergehen; fehlende Fehlerbehandlung bei MCP-Aufrufen; ein Skill, der zu viel auf einmal will. [tweet-2021517290320130103](../sources/tweet-2021517290320130103.md)

## Grenzen

Sekundärquelle: Das PDF ist nicht gespeichert, die Zusammenfassung stammt vom Autor des Posts. Verwandt: [Agent Skill Mining](Agent%20Skill%20Mining.md), [Design Skills for Coding Agents](Design%20Skills%20for%20Coding%20Agents.md). [tweet-2021517290320130103](../sources/tweet-2021517290320130103.md)
