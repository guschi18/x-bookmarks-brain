---
tags: [research, agents]
sources: [tweet-2080003448624300428.md, tweet-2080003451270885851.md, tweet-2080003454165295403.md, tweet-2080003459248755141.md, tweet-2080003461517549887.md, tweet-2080003463660925129.md, tweet-2080003446602600756.md, tweet-2080003444035703028.md]
created: 2026-10-02
updated: 2026-10-02
---

# Agentic Proof Search

## Definition (Stand 2026-07)

Shouqiao Wang beschreibt einen Ablauf für mathematische Beweissuche mit einem Coding-Agenten: ein Prompt, der exakt festlegt, was als Lösung zählt, ein langer autonomer Lauf in [Codex](../entities/Codex.md) und wiederholte adversariale Prüfung jedes Beweisentwurfs. Kern sei die Definition dessen, was als Lösung des Problems gilt. [tweet-2080003448624300428](../sources/tweet-2080003448624300428.md) Der Ablauf diente nach seinen Angaben offenen Erdős-Problemen, deren Beweise und Prompts er veröffentlicht hat. [tweet-2080003463660925129](../sources/tweet-2080003463660925129.md)

## Problemauswahl (Stand 2026-07)

Als ersten Erfolgsfaktor nennt Wang die Auswahl: Probleme, die Mathematiker bereits beschäftigen und die etwa Terence Tao aktiv diskutiert, anschließend ein KI-Filter gegen extrem schwere oder eng an große offene Vermutungen gebundene Probleme. [tweet-2080003446602600756](../sources/tweet-2080003446602600756.md)

## Prompt-Aufbau (Stand 2026-07)

Jeder Prompt formuliert das Problem präzise neu, legt fest, was ein vollständiger Beweis oder eine Widerlegung leisten muss, listet schwächere Ergebnisse auf, die nicht zählen, benennt problemspezifische Fallen und Randfälle und verlangt unabhängige adversariale Agenten gegen jedes Kandidatenargument. [tweet-2080003451270885851](../sources/tweet-2080003451270885851.md)

Der Prompt steuert auch die Suche: viele unabhängige Ansätze beginnen, mehrere unvereinbare Routen offenhalten, aggressiv Gegenbeispiele zu vorgeschlagenen Lemmata suchen und eine Route als blockiert markieren, wenn sie das Problem nur auf eine gleich starke unbewiesene Aussage reduziert. [tweet-2080003454165295403](../sources/tweet-2080003454165295403.md)

Neue Prompts entstehen aus Vorlagen: GPT erhält das Problem und einige erfolgreiche Prompts, schreibt einen problemspezifischen Prompt im selben Stil, und anschließend wird geprüft, dass die ursprüngliche Problemaussage exakt erhalten ist. Die Prompts je Problem liegen im Repository des Autors. [tweet-2080003454165295403](../sources/tweet-2080003454165295403.md)

## Referenzprompt zur Cycle Double Cover Conjecture (Stand 2026-07)

Vorbild ist der von OpenAI veröffentlichte Prompt an GPT 5.6 Sol Ultra zur Cycle Double Cover Conjecture. Er enthält: [tweet-2080003448624300428](../sources/tweet-2080003448624300428.md)

- exakte Definitionen von Multigraph, Brücke, Zyklus und Zyklen-Doppelüberdeckung sowie die genau zu beweisende Aussage ohne Zusatzannahmen. [tweet-2080003448624300428](../sources/tweet-2080003448624300428.md)
- eine Ausschlussliste: Spezialklassen, Varianten mit anders überdeckten Kanten, Reduktionen auf andere unbewiesene Vermutungen, Rechnerprüfung bis zu einer festen Größe und Gegenbeispielkandidaten ohne Zertifikat zählen nicht. [tweet-2080003448624300428](../sources/tweet-2080003448624300428.md)
- bis zu 64 parallele Agenten ohne feste Zuteilung, ein Register der Ansatzfamilien nach mathematischer Idee, Unabhängigkeit in frühen Runden und Umlenkung, wenn zu viele Agenten in einer Familie landen. [tweet-2080003448624300428](../sources/tweet-2080003448624300428.md)
- adversariale Prüfung auf benannte Fehlerklassen, Zurückweisung von Statusberichten und vager Zuversicht sowie eine Wurzelinstanz, die wiederholt synthetisiert, angreift und neue Runden startet. [tweet-2080003448624300428](../sources/tweet-2080003448624300428.md)
- Rückgabe nur bei einem vollständigen, auditfesten Beweis, mindestens 8 Stunden Arbeit und Websuche nur für Standardhintergrund, nicht für die Lösung selbst. [tweet-2080003448624300428](../sources/tweet-2080003448624300428.md)

## Ausführung (Stand 2026-07)

Der Prompt wurde in Codex als Ziel gesetzt und ohne weitere Interaktion laufen gelassen; begründet wird das mit langer Laufzeit, gehaltenem Forschungskontext und Zugriff auf lokale Dateien. Läufe dauerten etwa 6 bis 32 Stunden. [tweet-2080003459248755141](../sources/tweet-2080003459248755141.md)

Die Arbeit verlief als Schleife: Versuch, Fehlschlag, Diagnose, neuer Ansatz, Beweisentwurf, adversariales Audit, Reparatur. Sie endete, wenn das Modell keine substanziellen Lücken mehr fand. [tweet-2080003461517549887](../sources/tweet-2080003461517549887.md)

## Material (Stand 2026-07)

Das Repository ShouqiaoW/erdos (MIT) enthält Ordner für die Probleme 390, 486, 536, 788, 1002 und 1038 mit Beweis-PDFs, LaTeX-Quellen, Prompts und teils Python-Experimenten. [tweet-2080003463660925129](../sources/tweet-2080003463660925129.md)

## Forum-Claims und Erfolgsquote (Stand 2026-07)

Wang nennt rund 13 Versuche für die sechs Probleme 390, 486, 536, 788, 1002 und 1038, also etwa 46 Prozent Erfolg. [tweet-2080003444035703028](../sources/tweet-2080003444035703028.md)

| Problem | Claim auf erdosproblems.com | Kern laut Zusammenfassung |
| --- | --- | --- |
| 390 | full proof | Asymptotik von f(n) mit neuer oberer Schranke über glatte Zahlen; Lean-Formalisierung angekündigt |
| 486 | full proof | Antwort nein: logarithmische Dichte existiert nicht immer |
| 536 | partial proof | f(N)=o(N) über Cap-Set-Schranke in einer F3-Würfelstruktur |
| 788 | full proof | f(n)=n^(1/2+o(1)) mit Kernen linearer Abbildungen |
| 1002 | full proof | Cauchy-Grenzverteilung über Kettenbruchziffern |
| 1038 | full proof | Infimum etwa 1,834430, Supremum 2√2 nach Taos Argument |

Alle Zeilen: [tweet-2080003444035703028](../sources/tweet-2080003444035703028.md)

- Das Forum betont, dass ein Eintrag keine Korrektheitsprüfung durch die Seite bedeutet; Wangs Notizen nennen eigene Lektüre und mehrere KI-Prüfrunden, bei 390 einen langen, nur im Überblick verstandenen Beweis. [tweet-2080003444035703028](../sources/tweet-2080003444035703028.md)
- Die Problemseiten führen 486, 536, 788, 1002 und 1038 beim Abruf weiterhin als OPEN; 536 ist nur als Teilbeweis eingereicht, obwohl der Thread von sechs gelösten Problemen spricht. [tweet-2080003444035703028](../sources/tweet-2080003444035703028.md)
- Bei 1002 und 1038 stehen unabhängige KI-gestützte Konkurrenzclaims: Sangyoon Kwon mit GPT-5.6-sol Pro und Codex für 1002, Darvas, Peng und Tao mit GPT-5.5 Pro und einem Prover-Verifier-Ansatz für 1038. Dessen Autor fragt im Forum ausdrücklich nach Normen für das Ankündigen KI-gestützter Beweise. [tweet-2080003444035703028](../sources/tweet-2080003444035703028.md)

## Grenzen (Stand 2026-07)

- Das Abbruchkriterium „keine substanziellen Lücken mehr gefunden“ ist ein Urteil des Modells über sich selbst, kein unabhängiger Beweis. [tweet-2080003461517549887](../sources/tweet-2080003461517549887.md)
- Laut README sind die Beweise mit Hilfe von KI geprüft; laut Post sind zwei Probleme in Lean formalisiert, die übrigen noch nicht. Eine fachliche Begutachtung ist in den gespeicherten Quellen nicht belegt. Gespeichert ist nur die Repository-Übersicht, nicht Prompts, PDFs oder Lean-Dateien. [tweet-2080003463660925129](../sources/tweet-2080003463660925129.md)

Verwandte Muster: [Loop Engineering](Loop%20Engineering.md) für Schleifen mit Prüfung und Stoppregel, [Agent Workflow Graphs](Agent%20Workflow%20Graphs.md) für adversariale Verifier und Fan-out. [tweet-2080003461517549887](../sources/tweet-2080003461517549887.md)
