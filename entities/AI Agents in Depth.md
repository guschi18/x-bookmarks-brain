---
tags: [agents, research, tools]
sources: [tweet-2093559715150303691.md]
created: 2026-10-09
updated: 2026-10-09
---

# AI Agents in Depth

## Buch und Architektur (Stand 2026-08)

[bojieli/ai-agent-book](https://github.com/bojieli/ai-agent-book) trägt im gespeicherten englischen README den Titel AI Agents in Depth: Design Principles and Engineering Practice. Die zentrale Formel ist Agent = LLM + Context + Tools; zehn Kapitel führen von Grundlagen zu Gedächtnis, Werkzeugen, Coding, Interaktion, Evaluation, Post-Training, Weiterentwicklung und Multi-Agent-Zusammenarbeit. [tweet-2093559715150303691](../sources/tweet-2093559715150303691.md)

## Lehrmaterial und Anwendung

Der README nennt 93 begleitende Projekte, davon mehr als 70 eigenständige, sowie freie PDF-/EPUB-Ausgaben und Online-Lesefassungen. Er empfiehlt praktische Neuimplementierung mit einem Coding-Agenten und Reflexionsfragen statt bloßer Codelektüre; Projektarten und Ausführungsstatus sind getrennt dokumentiert. [tweet-2093559715150303691](../sources/tweet-2093559715150303691.md)

Für Kapitelumgebungen beschreibt er Python 3.11 bis 3.13, `uv sync --locked --extra ch1` beziehungsweise kapitelbezogene pip-Extras. Experimente haben eigene Anforderungen an Schlüssel, Browser, CUDA oder andere Systeme; einzelne Komponenten verlangen Python ab 3.12. Ein erfolgreicher Clone oder Installationslauf ist laut Quelle kein Nachweis abgeschlossener Experimente. [tweet-2093559715150303691](../sources/tweet-2093559715150303691.md)

## Versionen und Evidenzgrenzen

Der gespeicherte README beschreibt Version 2.0 gegenüber 1.4: asynchrone Interaktion und multimodale Agenten werden in Kapitel 6 zusammengeführt, Evaluation/Post-Training/Weiterentwicklung verschieben sich zu Kapitel 7/8/9. Der darunter enthaltene externe Clone-Anhang verwendet teilweise andere Kapitelzuordnungen; deshalb die jeweilige Projekt-README prüfen und diese gemischten Zuordnungen nicht als einheitliche Anleitung übernehmen. [tweet-2093559715150303691](../sources/tweet-2093559715150303691.md)

Pranav empfiehlt das Buch für bessere Harness-Entwicklung, insbesondere [Context Engineering](../concepts/Context%20Engineering.md) und Agentenwahrnehmung. Eine Verbesserung ist nicht gemessen; hier wurden der vollständige gespeicherte README und seine Links, nicht alle Kapitel oder Experimente geprüft. Die Lehrquelle ergänzt [Agentic Engineering](../concepts/Agentic%20Engineering.md) und ist kein allgemeiner Nachweis der Fähigkeiten von [Codex](Codex.md). [tweet-2093559715150303691](../sources/tweet-2093559715150303691.md)
