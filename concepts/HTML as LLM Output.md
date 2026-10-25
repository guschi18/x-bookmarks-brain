---
tags: [agents, product-building]
sources: [tweet-2053920266493808646.md, tweet-2106039761320518126.md, tweet-2105842218418544773.md, tweet-2107192972983075241.md, tweet-2090884854590382515.md, tweet-2087569590268391897.md]
created: 2026-10-02
updated: 2026-10-12
---

# HTML as LLM Output

## Kernidee (Stand 2026-05)

Andrej Karpathy empfiehlt im zitierten Beitrag, am Ende einer Anfrage „structure your response as HTML“ zu verlangen und die erzeugte Datei im Browser zu öffnen; auch Slideshows hätten funktioniert. Seine Begründung: Audio sei die bevorzugte menschliche Eingabe an KI, visuelle Ausgabe die bevorzugte Ausgabe, weil etwa ein Drittel des Gehirns auf Sehen spezialisiert sei. [tweet-2053920266493808646](../sources/tweet-2053920266493808646.md)

## Stufenmodell (Stand 2026-05)

Karpathy skizziert die Folge Rohtext, Markdown (Stand 2026-05 der Standard), HTML (früh, aber neuer guter Standard) bis zu interaktiven neuronalen Videos oder Simulationen, die direkt von einem Diffusionsmodell erzeugt werden. [tweet-2053920266493808646](../sources/tweet-2053920266493808646.md)

## Beispiele und Kosten (Stand 2026-05)

Der Post nennt als Beispiele farbige Code-Review-Diffs mit Randanmerkungen, ein Kanban aus 30 Tickets, Slider mit Live-Vorschau für Regex, Farben oder Cron sowie sechs Spec-Optionen mit Mockups nebeneinander. HTML koste laut Post etwa doppelt so viele Token wie Markdown, was bei großen Kontextfenstern weniger ins Gewicht falle; erzeugtes HTML könne auch ein prüfender Agent lesen. [tweet-2053920266493808646](../sources/tweet-2053920266493808646.md)

## Grenzen (Stand 2026-05)

Die Verweise auf Thariq Shihipars Artikel „The Unreasonable Effectiveness of HTML“, dessen Reichweite und Simon Willisons Wechsel sind Angaben des Posts; der Artikel selbst ist nicht gespeichert, das angehängte Video hat kein Transkript. Eine praktische Anwendung mit HTML für Menschen und JSON für Agenten beschreibt [Codebase Maps](Codebase%20Maps.md). [tweet-2053920266493808646](../sources/tweet-2053920266493808646.md)

## Additions (Stand 2026-10)

[Answer Me With HTML](../entities/Answer%20Me%20With%20HTML.md) makes the model write Markdown and computes layout/diagrams with a bundled renderer. Its author benchmark reports fewer output tokens and faster answers but similar/slightly higher cost due to extra context-reading turns; no reproduced savings are recorded here. [tweet-2106039761320518126](../sources/tweet-2106039761320518126.md)

[Explain Skill](../entities/Explain%20Skill.md) supplies a format ladder and complete writing/diagram/HTML templates; it keeps videos request-only and grounds code explanations in the actual repo. [tweet-2105842218418544773](../sources/tweet-2105842218418544773.md)

## Direkt beantwortbare Planseiten (Stand 2026-10)

Thariq liefert die Installation von [HTML Plan](../entities/HTML%20Plan.md). Das am 12.10.2026 separat geprüfte offizielle README konkretisiert einen aufklappbaren Entscheidungsbaum mit UI-/Schema-/Code-Ebenen und gebündelter Rückgabe von Nutzerantworten; damit dient die Seite nicht nur dem Lesen, sondern der Planabstimmung. [tweet-2107192972983075241](../sources/tweet-2107192972983075241.md)

## Erklärung ohne Vorwissen (Stand 2026-08)

Thariq nennt /eli5 <what you want explained> und diesen vollständigen Kurzprompt für einfache visuelle Erklärungen: [tweet-2090884854590382515](../sources/tweet-2090884854590382515.md)

> explain like I'm someone who knows nothing about this topic, using a HTML artifact with big pictures and few words [tweet-2090884854590382515](../sources/tweet-2090884854590382515.md)

Der Post berichtet häufige interne Nutzung bei Anthropic, keine Wirkungsmessung. [Explain Skill](../entities/Explain%20Skill.md) ist eine spätere, ausführlichere Implementierung mit Formatleiter, ELI13-Analogie und Repo-Belegen; der August-Kurzprompt bleibt eine eigenständige, datierte Anweisung. [tweet-2090884854590382515](../sources/tweet-2090884854590382515.md)

## Kompakte Formen vor HTML (Stand 2026-08)

[Show Me](../entities/Show%20Me.md) beschreibt Komponentenbäume, Call-Stacks, flache Dateibäume mit Zuständigkeiten, Pseudocode und Signaturen als kompakte Formen für Codeklärung; Diffs zeigen die Veränderung an diesen Formen. HTML-Mockups und Diagramme bleiben eine reichere Option. Das ergänzt [Answer Me With HTML](../entities/Answer%20Me%20With%20HTML.md) um einen anderen Darstellungsansatz; behauptete Verständlichkeits- und Geschwindigkeitsvorteile sind nicht gemessen. [tweet-2087569590268391897](../sources/tweet-2087569590268391897.md)
