---
tags: [tools, llm-training]
sources: [tweet-2078400632294457379.md, tweet-2086850058021196072.md, tweet-2052674473808265246.md]
created: 2026-10-02
updated: 2026-10-13
---

# Practical LLM Usage

## Mentales Modell (Stand 2026-07)

Im gespeicherten Vortrag beschreibt Karpathy ein Chatmodell als selbstständige Datei: Pre-Training komprimiert das Internet verlustbehaftet in die Parameter und erzeugt einen Wissensstichtag, Post-Training gibt die Assistentenrolle. Ohne Werkzeuge gibt es keinen Rechner, keine Websuche und keinen Interpreter. Häufig im Netz vorkommendes, nicht aktuelles Wissen sei eher verlässlich, bleibe aber prüfbedürftig. [tweet-2078400632294457379](../sources/tweet-2078400632294457379.md)

## Kontext und Modellwahl (Stand 2026-07)

- Bei Themenwechsel einen neuen Chat beginnen: Tokens im Kontextfenster können ablenken, die Genauigkeit senken und die Berechnung leicht verteuern. [tweet-2078400632294457379](../sources/tweet-2078400632294457379.md)
- Immer prüfen, welches Modell aktiv ist; Preisstufen geben Zugriff auf unterschiedlich starke Modelle. Karpathy fragt mehrere Anbieter parallel und nennt das seinen „LLM Council“. [tweet-2078400632294457379](../sources/tweet-2078400632294457379.md)
- Thinking-Modelle sind zusätzlich mit Reinforcement Learning trainiert und helfen bei Mathematik, Code und Logik; für einfache Fragen wie Reisetipps lohnen sie sich laut Vortrag nicht, deshalb erst schnell ohne Reasoning versuchen und bei schwachem Ergebnis wechseln. [tweet-2078400632294457379](../sources/tweet-2078400632294457379.md)

## Werkzeuge (Stand 2026-07)

- Websuche für aktuelle oder sich ändernde Informationen, mit Zitaten zur Gegenprüfung. [tweet-2078400632294457379](../sources/tweet-2078400632294457379.md)
- Deep Research für längere, zitierte Recherchen, deren Ergebnis dennoch Fehler enthalten kann. [tweet-2078400632294457379](../sources/tweet-2078400632294457379.md)
- Datei-Uploads für gemeinsames Lesen: Kapitel in den Kontext laden, erst zusammenfassen lassen, dann beim Lesen Fragen stellen. [tweet-2078400632294457379](../sources/tweet-2078400632294457379.md)
- Python-Interpreter für Rechnungen und Diagramme, Artifacts für kleine Apps und Diagramme, Cursor/Composer für professionelle Codearbeit; „Vibe Coding“ bezeichnet dort das Steuern eines Agenten über Anweisungen. [tweet-2078400632294457379](../sources/tweet-2078400632294457379.md)

## Modalitäten und Komfortfunktionen (Stand 2026-07)

Audio und Bilder lassen sich als Token-Ströme modellieren; native multimodale Modelle unterscheiden sich von angeflanschten Zusatzmodellen. Der Vortrag zeigt Spracheingabe, NotebookLM-Podcasts, Bildanalyse und -erzeugung. Memory, Custom Instructions und Custom GPTs sparen wiederholtes Prompten; Karpathy empfiehlt dabei Beschreibung plus konkrete Beispiele (Few-Shot), etwa für eine Vokabelextraktion beim Koreanischlernen. [tweet-2078400632294457379](../sources/tweet-2078400632294457379.md)

## Grenzen (Stand 2026-07)

Konkrete Produktaussagen spiegeln den Stand der Aufnahme, etwa GPT-4o als Standardmodell, o1 Pro im 200-Dollar-Tarif und Claude ohne Suche oder Thinking-Modell; sie sind für die Gegenwart nicht gültig. Die Prinzipien sind Karpathys Praxiserfahrung, keine gemessenen Vergleiche. [Personalized LLM Workflows](Personalized%20LLM%20Workflows.md) ergänzt dauerhafte Instruktionen und Prompt-Vorlagen. [tweet-2078400632294457379](../sources/tweet-2078400632294457379.md)

## Council als konkrete Anwendung (Stand 2026-08)

[LLM Council](../entities/LLM%20Council.md) ergänzt das parallele Befragen mehrerer Anbieter um eine konkrete lokale OpenRouter-App: unabhängige Antworten, anonymisiertes gegenseitiges Ranking und Chairman-Synthese. Der Originalautor stellt das Projekt als unbetreuten Experimentier-Hack bereit; die Empfehlung im Post belegt keinen allgemeinen Qualitätsgewinn. [tweet-2086850058021196072](../sources/tweet-2086850058021196072.md)

## Trainingsgrundlagen als Ergänzung (Stand 2026-05; historischer Vortrag)

[LLM Training Pipeline](LLM%20Training%20Pipeline.md) ergänzt den späteren Praxisvortrag um die Unterscheidung von Pretraining, SFT und RL sowie die Grenzen eines Reward-Modells als Ersatz für menschliche Bewertung. Es handelt sich um eine andere Aufnahme; deren historisches Produktmenü ersetzt die später dokumentierten Aussagen nicht. [tweet-2052674473808265246](../sources/tweet-2052674473808265246.md)
