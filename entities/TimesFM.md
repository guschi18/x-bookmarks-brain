---
tags: [tools, research]
sources: [tweet-2088947629413556239.md]
created: 2026-10-12
updated: 2026-10-12
---

# TimesFM

## Rolle und gespeicherter Stand (Stand 2026-08)

[TimesFM](https://github.com/google-research/timesfm) ist ein vortrainiertes Zeitreihenmodell von Google Research. Die gespeicherte README nennt TimesFM 2.5, lokale Nutzung mit Torch oder Flax, XReg für Kovariaten und LoRA-Fine-Tuning über Transformers/PEFT. Der Tweet beschreibt es als frei und neu; die README dokumentiert bereits frühere Releases und ist die konkretere Quelle. [tweet-2088947629413556239](../sources/tweet-2088947629413556239.md)

Das 2.5-Modell hat laut gespeicherter README 200 Millionen Parameter, unterstützt bis zu 16k Kontext und einen optionalen Quantilkopf für bis zu 1k Vorhersagehorizont. Der Artikel verweist auf die [ICML-2024-Publikation](https://arxiv.org/abs/2310.10688) und eine [Checkpoint-Sammlung](https://huggingface.co/collections/google/timesfm-release-66e4be5fdb56e960c1e482a6). Dies sind versionierte Anbieterangaben. [tweet-2088947629413556239](../sources/tweet-2088947629413556239.md)

## Lokaler Einstieg für 2.5 (Stand des gespeicherten Captures)

Die README nennt pip install timesfm[torch], alternativ timesfm[flax] und optional timesfm[xreg]. CPU-, GPU-, TPU- oder Apple-Silicon-Backend muss zur Umgebung passen. Das Beispiel lädt google/timesfm-2.5-200m-pytorch und berechnet Punkt- und Quantilprognosen für zwei künstliche Reihen. [tweet-2088947629413556239](../sources/tweet-2088947629413556239.md)

## Aktuelle Version und Lizenz (ergänzend geprüft 2026-10-12)

Die aktuelle [Repository-README](https://github.com/google-research/timesfm#timesfm) führt inzwischen TimesFM 3.0 als neueste Version mit nativer multivariater Prognose und flexiblen Kovariaten. Der alte 2.5-Code liegt weiterhin unter src/timesfm; die historische Anleitung ist daher kein aktueller 3.0-Einstieg. [tweet-2088947629413556239](../sources/tweet-2088947629413556239.md)

Die Lizenz unterscheidet Code und Gewichte: Repository-Code und Gewichte bis 2.5 bleiben Apache-2.0. Heruntergeladene 3.0-Gewichte unter timesfm-non-commercial-license-v1.0 sind auf nichtkommerzielle, nichtproduktive Nutzung beschränkt; kommerzielle/produktive 3.0-Nutzung wird über autorisierte Google-Cloud-Dienste angeboten. Die pauschale Aussage frei/open source im alten Tweet ist damit keine allgemeine Lizenzbeschreibung der aktuellen Gewichte. [tweet-2088947629413556239](../sources/tweet-2088947629413556239.md)

## Evidenzgrenze

Die frei verfügbare Repository-Fassung wird ausdrücklich nicht als offiziell unterstütztes Google-Produkt bezeichnet. Gespeichert sind Dokumentation und Beispielcode, keine eigenen Prognosemessungen oder Nachweise finanzieller Erträge. [tweet-2088947629413556239](../sources/tweet-2088947629413556239.md)
