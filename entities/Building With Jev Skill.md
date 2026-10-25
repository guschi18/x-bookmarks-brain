---
tags: [agents, tools]
sources: [tweet-2100693810397540386.md]
created: 2026-10-07
updated: 2026-10-07
---

# Building With Jev Skill

## Artefakt und Inhalt (Stand 2026-09)

Drew Breunigs [Building-with-Jev-Skill](https://github.com/dbreunig/building-with-jev-skill) ist ein eigener Agent-Skill zum Schreiben und Verbessern von Programmen mit [Jev](Jev.md). Das README nennt Fragenentwurf für Choice, Score und Noul, State-Struktur, Kombination der Antworten im Code, Konfidenzschwellen sowie Diagnose falscher oder unsicherer Antworten; Zielversion ist Jev 1.13. [tweet-2100693810397540386](../sources/tweet-2100693810397540386.md)

Die eigentliche Anleitung liegt in [skills/jev/SKILL.md](https://github.com/dbreunig/building-with-jev-skill/blob/main/skills/jev/SKILL.md). Das gespeicherte README verweist dafür auf TypeSafes Dokumentation; der vollständige Skill-Text und überprüfte Anwendungsergebnisse sind hier nicht gespeichert. [tweet-2100693810397540386](../sources/tweet-2100693810397540386.md)

## Installation und Aufruf (Stand 2026-09)

Für [Claude Code](Claude%20Code.md) nennt das README die beiden Befehle /plugin marketplace add dbreunig/building-with-jev-skill und /plugin install jev@building-with-jev. Als gemeinsamer Skills-CLI-Weg für Claude Code, [Codex](Codex.md), Cursor und weitere Agenten ist npx skills add dbreunig/building-with-jev-skill angegeben. Die Installation wurde hier nicht ausgeführt. [tweet-2100693810397540386](../sources/tweet-2100693810397540386.md)

Der Skill soll bei Jev-/TypeSafe-Aufgaben automatisch geladen werden oder in Claude Code mit /jev aufrufbar sein. Er ist ein separates Community-Artefakt gegenüber dem offiziellen TypeSafe-Skill; das thematische Muster erläutert [Typed Decision Layer](../concepts/Typed%20Decision%20Layer.md). [tweet-2100693810397540386](../sources/tweet-2100693810397540386.md)
