---
tags: [research, tools]
sources: [tweet-2100426999546184123.md]
created: 2026-10-07
updated: 2026-10-07
---

# 1k Papers

## Forschungsatlas und Bezug (Stand 2026-09)

[1k Papers](https://www.1kpapers.com/) erschließt laut gespeicherter Website 1.018 KI-Forschungspaper nach Labor, Monat und redaktionellem Thema. Der Korpus besteht aus 1.000 Papern vom 4. August 2025 bis 4. August 2026 plus 18 Together-AI-Papern; die Auswahl ist popularitätsgewichtet und keine vollständige Forschungsgeschichte. [tweet-2100426999546184123](../sources/tweet-2100426999546184123.md)

## Zweistufiger Ablauf (Stand 2026-09)

1. PDFs extrahieren und mit DeepSeek V4 Flash zusammenfassen. Der Benchmark hielt Text, Prompt und Output-Vertrag konstant; zu große Dokumente nutzten einen deterministischen Map-Reduce-Ablauf mit 50.000-Zeichen-Blöcken. [tweet-2100426999546184123](../sources/tweet-2100426999546184123.md)
2. Titel, Zusammenfassung und 24 mögliche Themen an [Jev](Jev.md) geben und das Paper klassifizieren lassen. Der Autor nennt 0,08 USD für die Klassifikationen und 256 ms Medianlatenz pro Paper. [tweet-2100426999546184123](../sources/tweet-2100426999546184123.md)
3. Die Ergebnisse im Atlas visualisieren. Hassan prüft die neuen Jev-Labels noch mit Evals, bevor sie die bestehenden Zuordnungen ersetzen; die veröffentlichte Website belegt deshalb nicht automatisch die Qualität dieser neuen Labels. [tweet-2100426999546184123](../sources/tweet-2100426999546184123.md)

## Messgrenzen (Stand 2026-09)

Die Zusammenfassungen kosteten laut Quelle 3,99 USD, getrennt von der Jev-Klassifikation. Die Website nennt für denselben 1.000-Paper-Input außerdem 6,00 USD bei GPT-5.6 Luna und 35,76 USD bei Claude Haiku 4.5, mit eingefrorenen Preisen vom 5. August 2026 und ausgeschaltetem Reasoning. Das ist ein Inferenzkostenvergleich, keine Rangfolge faktischer Qualität; Download, Extraktion, Speicherung, Netzwerk und Entwicklung sind ausgeschlossen. [tweet-2100426999546184123](../sources/tweet-2100426999546184123.md)
