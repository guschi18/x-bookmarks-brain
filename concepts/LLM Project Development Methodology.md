---
tags: [agents, product-building]
sources: [tweet-2004129820335124948.md]
created: 2026-10-24
updated: 2026-10-24
---

# LLM Project Development Methodology

## Definition (Stand 2025-12)

Muratcan Koylan leitet aus Andrej Karpathys HN-Time-Capsule-Projekt eine Methodik für LLM-gestützte Batch-Projekte ab und fasst sie als Skill im Repository Agent-Skills-for-Context-Engineering (skills/project-development). [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md) Der Skill arbeitet laut Autor eine Ebene über den Laufzeit-Skills zu [Context Engineering](Context%20Engineering.md): Er klärt, was gebaut wird und wie das Projekt strukturiert wird. [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md)

## Vorlage: Karpathys Vorgehen

Karpathy beschreibt in seinem Blogartikel: Er sah, dass sich Rückblick-Analyse alter Diskussionen für ein LLM eignet, kopierte eine Artikel-und-Kommentar-Seite manuell in ChatGPT 5.1 Thinking und verglich das Ergebnis mit seiner eigenen Bewertung. Danach baute er die Pipeline mit Opus 4.5 in etwa drei Stunden per Vibe-Coding. Der Lauf über 930 Frontpage-Einträge vom Dezember 2015 dauerte laut Quote rund eine Stunde und kostete 60 $. [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md)

## Prinzipien

- Manueller Prototyp zuerst: Erst prüfen, dass das LLM die Aufgabe leisten kann, dann automatisieren. [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md)
- Task-Model-Fit: Vorab fragen, ob Synthese, subjektives Urteil und Fehlertoleranz der Aufgabe zu den Stärken des Modells passen. [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md)
- Gestufte Pipeline: Deterministische Stufen (beschaffen, vorbereiten, parsen, rendern) von der teuren nichtdeterministischen LLM-Stufe trennen, Zwischenergebnisse cachen, Stufen idempotent halten. Ablauf im Beispiel: fetch, prompt, analyze, parse, render. [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md)
- Dateisystem als Zustand: Jeder Artikel erhält ein Verzeichnis; welche Dateien existieren, bestimmt die offene Arbeit. [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md)
- Strukturierter Output: Format mit Beispielen vorgeben und begründen ("genau so, weil ich es programmatisch parse"). [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md)
- Architectural Reduction: Minimal beginnen, Komplexität nur bei erwiesenem Bedarf ergänzen; Gerüst kann das Modell mehr einengen als stützen. [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md)

## Einsatz und Grenzen

Laut Autor nützlich für Einsteiger in LLM-Projekte, für Leute, die Aufgaben automatisieren, die LLM-Agenten schlecht lösen, und für Batch-Pipelines (Analyse, Inhaltserzeugung, Datentransformation). [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md) Der Autor testete nur eine News-Scraping-Idee, bei der der Skill Zusammenfassen (LLM) von Scraping (kein LLM) trennte, und nennt den Skill selbst nicht revolutionär. Eine unabhängige Prüfung liegt nicht vor. [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md)

## Verwandt

[Context Engineering](Context%20Engineering.md)
