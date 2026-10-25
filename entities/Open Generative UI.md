---
tags: [agents, tools, product-building]
sources: [tweet-2052299884817240444.md]
created: 2026-10-14
updated: 2026-10-14
---

# Open Generative UI

## Mechanismus (Stand 2026-05)

Der Post stellt Open Generative UI von CopilotKit als frei erzeugte HTML-/SVG-Oberflächen vor: Der Agent streamt Markup in ein iframe im Chat. Anders als bei einer festen Komponentenwahl entstehen Visualisierungen aus Modelltext; Design-Skills sollen Format, Diagrammbeschriftung und Verhalten steuern. AG-UI dient als Anbindung an Agentenframeworks. [tweet-2052299884817240444](../sources/tweet-2052299884817240444.md)

## Anwendung und Abgrenzung (Stand 2026-05)

Als Beispiele nennt der Autor Chart.js-Dashboards und drehbare 3D-Modelle. Der beschriebene Skill gibt dem Agenten Gestaltungsregeln und konkrete Formate; die Qualität wird im Post der Skill-Schicht zugeschrieben, ohne reproduzierten Vergleich. [tweet-2052299884817240444](../sources/tweet-2052299884817240444.md)

Das bestehende [OpenUI](OpenUI.md) von thesysdev erzeugt eine eigene strukturierte UI-Sprache mit registrierter Komponentenbibliothek. CopilotKits Open Generative UI ist ein anderes Projekt; ein Vergleichseintrag in dessen README ist keine bereits vollständig gespeicherte Anleitung zu diesem Ansatz. [tweet-2052299884817240444](../sources/tweet-2052299884817240444.md)

## Zusätzliche Primärquelle (geprüft 2026-10-14)

Die [heutige CopilotKit-Dokumentation](https://docs.copilotkit.ai/generative-ui/open-generative-ui) dokumentiert `openGenerativeUI` im Runtime-Setup und `openGenerativeUI.designSkill` für den visuellen Prompt; der eingebaute Renderer zeigt gestreamtes HTML/CSS im sandboxed iframe. Der damalige [Repository-Einstieg](https://github.com/CopilotKit/OpenGenerativeUI) führt inzwischen zu OpenIntelligentUI. Das ist ein späterer Dokumentationsstand und kein auf Mai eingefrorener Release. [tweet-2052299884817240444](../sources/tweet-2052299884817240444.md)

## Evidenzgrenzen

Das gespeicherte Demo-Video hat keinen gesprochenen Transkriptinhalt; die im Post angekündigten Repository-/Playground-Links in Replies wurden nicht mitgespeichert. Die absoluten Aussagen über Isolation, Datenabfluss und breite SDK-Kompatibilität sind Autorangaben, keine durchgeführte Sicherheitsprüfung oder getestete Integration. [tweet-2052299884817240444](../sources/tweet-2052299884817240444.md)
