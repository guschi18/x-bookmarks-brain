---
tags: [llm-training, research]
sources: [tweet-2052674473808265246.md]
created: 2026-10-13
updated: 2026-10-13
---

# LLM Training Pipeline

## Drei Lernstufen (Stand 2026-05; historischer Vortrag)

Karpathy trennt Pretraining als Wissensaufnahme, Supervised Fine-Tuning (SFT) als Lernen aus vorgeführten Assistentenantworten und Reinforcement Learning (RL) als Übung mit bewerteten eigenen Lösungsversuchen. Das ist das Erklärmodell des gespeicherten Grundlagenvortrags, keine vollständige Spezifikation aller heutigen Trainingsverfahren. [tweet-2052674473808265246](../sources/tweet-2052674473808265246.md)

Pretraining filtert und tokenisiert große Textsammlungen und optimiert Next-Token-Vorhersagen. Das resultierende Basismodell kann Text fortsetzen; die Assistentenrolle folgt nicht allein aus diesem Trainingsziel. SFT verwendet anschließend Gesprächsbeispiele, die durch menschliche Vorgaben und teilweise synthetische Erzeugung geprägt sind. [tweet-2052674473808265246](../sources/tweet-2052674473808265246.md)

RL erzeugt mehrere Lösungsversuche, bewertet sie und verstärkt erfolgreiche Verhaltensweisen. Für überprüfbare Aufgaben wie Mathematik kann ein konkretes Ergebnis die Bewertung liefern; neue Lösungsstrategien werden damit erprobt, statt nur menschliche Antworten nachzuahmen. [tweet-2052674473808265246](../sources/tweet-2052674473808265246.md)

## RLHF und Bewertungsgrenzen (Stand 2026-05; historischer Vortrag)

Bei RLHF trainieren menschliche Präferenzurteile ein Reward-Modell, gegen das anschließend optimiert werden kann. Karpathy betont das Risiko, dass starke Optimierung Bewertungsfehler ausnutzt: Hoher Reward muss keine gute Antwort für Menschen bedeuten. Dies erklärt eine Grenze des Ersatzmaßstabs, keinen universellen Beweis für eine feste erlaubte Zahl von Trainingsschritten. [tweet-2052674473808265246](../sources/tweet-2052674473808265246.md)

## Bezug zur Nutzung und Evidenzgrenzen (Stand 2026-05; historischer Vortrag)

Der Vortrag unterscheidet Parameterwissen von unmittelbar bereitgestelltem Kontext und Werkzeugergebnissen. [Practical LLM Usage](Practical%20LLM%20Usage.md) behandelt daraus folgende Nutzungsentscheidungen; [Train LLM From Scratch](../entities/Train%20LLM%20From%20Scratch.md) ist ein eigener, verwandter Implementierungs-Lernpfad. [tweet-2052674473808265246](../sources/tweet-2052674473808265246.md)

Die Aufnahme beschreibt ihren Reasoning-Modellstand ausdrücklich als Anfang 2025. Produktmenüs, Preise, Rankings und Prognosen daraus sind historische Beispiele, keine aktuelle Modellberatung. Der Mai-Repost macht die Aufnahme nicht zu einem neuen Release. [tweet-2052674473808265246](../sources/tweet-2052674473808265246.md)
