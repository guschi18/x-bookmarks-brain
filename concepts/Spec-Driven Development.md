---
tags: [agents, research]
sources: [tweet-2114486060730237224.md]
created: 2026-10-27
updated: 2026-10-27
---

# Spec-Driven Development

## Definition (Stand 2026-10)

Spec-Driven Development (SDD) lässt Entwickler und Agenten Spezifikationen schreiben, die die Umsetzung leiten, damit die Absicht nicht nur im Chat steht. Werkzeuge sind u. a. OpenSpec, Kiro und [Spec Kit](../entities/Spec%20Kit.md). [tweet-2114486060730237224](../sources/tweet-2114486060730237224.md)

## Empirische Befunde (Stand 2026-10)

Das Paper "Spec-Driven Development as Prescribed and as Practiced" (CMU und Google, arXiv 2608.25202, Fassung v4 vom 15.10.2026) wertet Reddit-Diskussionen, Interviews mit 21 Praktikern (davon acht Werkzeugbauer) und 266 aktive Repositories aus dem Korpus SpecMine (470.795 Spec-Dateien aus 73.030 Repositories) aus. [tweet-2114486060730237224](../sources/tweet-2114486060730237224.md)

- 77,6 % der Specs enthalten Implementierungsdetails (Angabe aus dem Tweet; die gespeicherte Abstract-Seite nennt die Zahl nicht). Details können Agenten helfen, lassen Specs aber veralten. [tweet-2114486060730237224](../sources/tweet-2114486060730237224.md)
- SDD wird selektiv und vor allem für neue Features genutzt; Praktiker berichten zuverlässigeres Agentenverhalten bei mehr Planungs- und Review-Aufwand. [tweet-2114486060730237224](../sources/tweet-2114486060730237224.md)
- Spec-Code-Prüfungen finden meist beim Abschluss einer Änderung statt, nicht fortlaufend. [tweet-2114486060730237224](../sources/tweet-2114486060730237224.md)
- Individueller Nutzen kommt wohl vom Klären der Absicht vor der Delegation; Teamnutzen hängt davon ab, dass SDD ein gemeinsamer Prozess wird. [tweet-2114486060730237224](../sources/tweet-2114486060730237224.md)

## Grenzen

Laut Tweet ließ sich der SDD-Nutzen nicht von Modellverbesserungen trennen. Die Studie ist qualitativ; ein Kausalbeweis für bessere Codequalität liegt nicht vor. Verwandt: [Agentic Engineering](Agentic%20Engineering.md). [tweet-2114486060730237224](../sources/tweet-2114486060730237224.md)
