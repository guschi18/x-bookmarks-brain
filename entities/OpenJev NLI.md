---
tags: [llm-training, research, tools]
sources: [tweet-2100341039986798930.md]
created: 2026-10-08
updated: 2026-10-08
---

# OpenJev NLI

## Modell und Bezug (Stand 2026-09)

OpenJev NLI bezeichnet hier [AlexWortega/openjev](https://huggingface.co/AlexWortega/openjev), das von Alex Nikolic verlinkte Qwen3.5-4B-NLI-Modell. Es ist eine eigenständige offene Implementierung, kein Nachweis von TypeSafes privatem [Jev](Jev.md)-Training und nicht TheoLeeCJs früher ebenfalls OpenJev genanntes SemIf aus dem [Jev Project Directory](../synthesis/Jev%20Project%20Directory.md). [tweet-2100341039986798930](../sources/tweet-2100341039986798930.md)

Die Modellkarte beschreibt einen Cross-Encoder, der Premise und Hypothesis gemeinsam liest und contradiction, entailment oder neutral bewertet. Der Checkpoint qwen3.5-4b-nli nutzt Qwen3_5ForSequenceClassification, drei Labels, Last-Token-Pooling und Cross-Entropy über diese Klassen. [tweet-2100341039986798930](../sources/tweet-2100341039986798930.md)

## Verwendung (Stand 2026-09)

modeling_openjev.py stellt OpenJevCrossEncoder mit predict, rerank, grade und latents bereit. predict liefert die drei Klassenwahrscheinlichkeiten; rerank wählt den Kandidaten mit höchstem Entailment. Die Modellkarte schlägt damit Antwort-Ranking, Referenzbewertung und Content-Guards vor. [tweet-2100341039986798930](../sources/tweet-2100341039986798930.md)

Das Beispiel lädt OpenJevCrossEncoder mit Modell-ID AlexWortega/openjev und subfolder qwen3.5-4b-nli. Alternativ nennt die Karte AutoModelForSequenceClassification und AutoTokenizer sowie model.config.nli_template.format für Premise und Hypothesis. [tweet-2100341039986798930](../sources/tweet-2100341039986798930.md)

Die Karte verweist auf Trainer, Multiple-Choice-Harness, Flappy Bird, Doom, Radar sowie Videos und Raw-JSON-Resultate. Doom soll ohne Training pro Aufgabe sowohl aus Textzustand als auch über Qwens Vision-Tower aus Pixeln gespielt werden; das sind Modellkartenangaben, keine hier replizierten Spieltests. [tweet-2100341039986798930](../sources/tweet-2100341039986798930.md)

## Grenzen und Referenz (Stand 2026-09)

Der Hauptpost sagt, ein MLP auf Qwen 4B funktioniere wie Jev; die konkrete gespeicherte Modellkarte beschreibt dagegen einen dreiklassigen NLI-Cross-Encoder. Ohne gespeicherten kontrollierten Vergleich folgt daraus weder gleiche Architektur noch gleiche Qualität, Latenz oder Kalibrierung. [tweet-2100341039986798930](../sources/tweet-2100341039986798930.md)

Die Modellkarte nennt MIT und verlinkt [dleemillers NLI-Cross-Encoder-Anwendungen](https://huggingface.co/blog/dleemiller/nli-xenc-ways-to-use) als Bezug. Das Modell ergänzt [Typed Decision Layer](../concepts/Typed%20Decision%20Layer.md) um eine trainierte NLI-Variante; zulässige Handlungen und Ergebnisprüfung bleiben Aufgaben des Anwendungscodes. [tweet-2100341039986798930](../sources/tweet-2100341039986798930.md)
