---
tags: [agents, tools]
sources: [tweet-2106377863163507162.md, tweet-2106039761320518126.md, tweet-2105842218418544773.md, tweet-2105819303471976479.md, tweet-2084753070437609606.md]
created: 2026-10-04
updated: 2026-10-12
---

# Simplified Technical English

## Skill and mechanism (Stand 2026-10)

The [0xpili repository](https://github.com/0xpili/simplified-technical-english) provides an agent skill based on ASD-STE100 Issue 7 (2017; the current issue is Issue 9 of 2025-01-15, so rules and word lists may differ), with 53 rules, 869 approved words, substitutions and before/after examples. [tweet-2106377863163507162](../sources/tweet-2106377863163507162.md)

Clone into the Claude skills folder and request STE writing or review; other LLMs can receive SKILL.md and reference material in their system prompt. [tweet-2106377863163507162](../sources/tweet-2106377863163507162.md)

## Check and limits (Stand 2026-10)

Run python3 scripts/ste_check.py --mode procedural draft.txt or --mode descriptive chapter.md; the Python-only tool flags long sentences/paragraphs, unapproved verbs, passive voice and vocabulary issues. [tweet-2106377863163507162](../sources/tweet-2106377863163507162.md)

It cannot verify approved word meanings or certify full compliance. The unofficial skill still requires a knowledgeable reviewer for important documents. [tweet-2106377863163507162](../sources/tweet-2106377863163507162.md)

The quoted Karpathy post proposes relaxed STE, diagrams, HTML and requested explainer videos as formats for understanding model output. [tweet-2106377863163507162](../sources/tweet-2106377863163507162.md)

## Additions (Stand 2026-10)

[Answer Me With HTML](Answer%20Me%20With%20HTML.md) adds adapted writing checks to a Markdown renderer, rather than certifying the official specification. [tweet-2106039761320518126](../sources/tweet-2106039761320518126.md)

[Explain Skill](Explain%20Skill.md) uses relaxed STE rules with format selection and examples; it is distinct from this repository's word-list checker. [tweet-2105842218418544773](../sources/tweet-2105842218418544773.md)

## Originalpost und Bildreferenz (Stand 2026-10)

Karpathy empfiehlt Erklärungen in ASD-STE100 oder einer gelockerten Form (80 Prozent), danach Diagramme, HTML und individuell erzeugte Erklärvideos. Der identische Text steht bereits in den früheren Quellen; dieses Original ergänzt eine Grafik mit Satzbeispielen und Wörterbuchersetzungen. [tweet-2105819303471976479](../sources/tweet-2105819303471976479.md)

Die Grafik nennt höchstens 20 Wörter pro prozeduralem Satz, 25 pro beschreibendem Satz, sechs Sätze pro beschreibendem Absatz und drei Wörter pro noun cluster; sie empfiehlt einen Schritt pro Satz, aktive Form in Verfahren und ein Thema pro Absatz. Diese Werte sind Angaben der gespeicherten Grafik, keine unabhängig geprüfte Normfassung. [tweet-2105819303471976479](../sources/tweet-2105819303471976479.md)

Beispiele im Bild: ensure ? make sure, replenish ? fill, utilize ? use, prior to ? before; zugelassene Wörter dürfen nur in der freigegebenen Wortart und Bedeutung verwendet werden. Diagramme und [HTML as LLM Output](../concepts/HTML%20as%20LLM%20Output.md) sind Karpathys weitere Darstellungsoptionen, nicht Ergebnisse eines Verständlichkeitstests. [tweet-2105819303471976479](../sources/tweet-2105819303471976479.md)

## Kurze globale Anweisung (Stand 2026-08)

Matt Pocock experimentiert mit dieser vollständigen CLAUDE.md-Anweisung; sie verbindet die Sprachwahl mit dem Lesen lokaler Domänenbegriffe. [tweet-2084753070437609606](../sources/tweet-2084753070437609606.md)

```text
Always talk in ASD-STE100 Simplified Technical English. Always read CONTEXT.md files, and use their ubiquitous language.
```

Der August-Post ist ein Praxisvorschlag ohne Wirkungsmessung oder Normprüfung und ersetzt nicht die später dokumentierten Skill-Regeln. Die CONTEXT.md-Ergänzung gehört zu [Context Engineering](../concepts/Context%20Engineering.md). [tweet-2084753070437609606](../sources/tweet-2084753070437609606.md)
