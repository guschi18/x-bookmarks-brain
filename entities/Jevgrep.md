---
tags: [agents, tools]
sources: [tweet-2103920741481848861.md, tweet-2104168233309974779.md]
created: 2026-10-03
updated: 2026-10-03
---

# Jevgrep

## Rolle

[Jevgrep](Jevgrep.md) (https://github.com/dzhng/jevgrep, CLI `jg`) sucht Code nach Funktion statt Wortlaut: Auf eine Repository-Frage liefert es relevante Dateien, Lesehinweise und wörtliche Auszüge in einer Antwort; [Jev](Jev.md) bewertet die Relevanz über Ordner, Dateien und Deklarationen. [tweet-2103920741481848861](../sources/tweet-2103920741481848861.md)

Avi Chawla führt Jev-gestützte Codesuche als einen von zwölf Agenten-Einsatzfällen. [tweet-2104168233309974779](../sources/tweet-2104168233309974779.md)

## Einrichtung

Installation über `npm install -g @dzhng/jevgrep`, dann `jg auth` und `jg skill`; der Skill ist nötig, damit der Coding-Agent die CLI zur Kontextsammlung nutzt. Voraussetzungen sind Node.js 22+, macOS oder Linux und ein Key für Vercel AI Gateway, TypeSafe, OpenRouter oder OpenCode Zen. [tweet-2103920741481848861](../sources/tweet-2103920741481848861.md)

## Widersprüchliche Kostenangaben

Der Post nennt 40 Prozent geringere Kosten (auf SWE-bench verifiziert), die README ~30 Prozent bei denselben 8 von 10 gelösten Aufgaben. Es handelt sich um einen Zehn-Aufgaben-Vergleich des Autors. [tweet-2103920741481848861](../sources/tweet-2103920741481848861.md) Siehe auch [AI Coding Cost Claims](../concepts/AI%20Coding%20Cost%20Claims.md).
