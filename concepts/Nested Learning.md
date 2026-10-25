---
tags: [llm-training, research]
sources: [tweet-2054738364667228487.md, tweet-2054611399792644386.md]
created: 2026-10-01
updated: 2026-10-01
---

# Nested Learning

## Forschungsansatz (Stand 2026-05)

Der gespeicherte Google-Research-Blog zu „Nested Learning: The Illusion of Deep Learning Architectures“ beschreibt ein Modell als mehrere verbundene, geschachtelte oder parallele Optimierungsprobleme. Jede Ebene hat einen eigenen Kontextfluss und eine Update-Frequenz; Architektur und Lernregel werden in dieser Perspektive gemeinsam modelliert. Der Blog ordnet das Paper NeurIPS 2025 zu. [tweet-2054738364667228487](../sources/tweet-2054738364667228487.md)

## Mechanismus und Deep Optimizers

Die Forscher betrachten Backpropagation als assoziatives Gedächtnis für die Zuordnung eines Datenpunkts zu lokalem Fehler; auch Attention und Momentum-Optimierung werden als Gedächtnis-/Optimierungsmodule betrachtet. Unterschiedliche Update-Raten ordnen diese Module in Ebenen. [tweet-2054738364667228487](../sources/tweet-2054738364667228487.md)

Für Deep Optimizers beschreibt der Blog eine Änderung der zugrunde liegenden Zielfunktion in Richtung L2-Regression, aus der neue Momentum-Formulierungen abgeleitet werden sollen. Der gespeicherte Blog liefert die Idee, keine vollständige Implementierung oder eigene Replikation. [tweet-2054738364667228487](../sources/tweet-2054738364667228487.md)

## Continuum Memory und Hope

Ein Continuum Memory System (CMS) besteht laut Blog aus einem Spektrum von Modulen mit verschiedenen Update-Frequenzen statt nur kurzzeitigem Sequenzkontext und langfristigem Pretraining-Wissen. Hope wird als selbstmodifizierende rekurrente Variante von Titans mit CMS und mehreren Ebenen von In-Context Learning beschrieben. [tweet-2054738364667228487](../sources/tweet-2054738364667228487.md)

Der Blog berichtet niedrigere Perplexität, höhere Genauigkeit in ausgewählten Sprach-/Common-Sense-Aufgaben und bessere Long-Context-Ergebnisse bei Needle-in-a-Haystack. Das sind Forschungsergebnisse nach Darstellung der Autoren; detaillierte Messwerte, Vergleichskonfigurationen und Paper-Volltext sind hier nicht gespeichert. Der [Paper-Link](http://abehrouz.github.io/files/NL.pdf) und [Titans-Verweis](https://arxiv.org/abs/2501.00663) bleiben zugänglich. [tweet-2054738364667228487](../sources/tweet-2054738364667228487.md)

## Continual Learning und Evidenzgrenze

Der Forschungsbericht behandelt Catastrophic Forgetting beim weiteren Parameterlernen und beschreibt NL als Ansatz zur Verbesserung von Continual Learning. Er belegt weder die vollständige Lösung aller Vergessensprobleme noch unbegrenztes Lernen in einem eingesetzten Produkt. [tweet-2054738364667228487](../sources/tweet-2054738364667228487.md)

Der zweite Post nennt NL „Attention Is All You Need V2“, behauptet das Ende der Transformer-Ära und „100 % Stabilität“ sowie eine allgemeine Erklärung von Halluzinationen durch Catastrophic Forgetting. Diese Aussagen gehen über den gespeicherten Forschungsblog hinaus; der Screenshot bestätigt lediglich Titel und Forschungsgegenstand, keine solchen Resultate. [tweet-2054611399792644386](../sources/tweet-2054611399792644386.md) [tweet-2054738364667228487](../sources/tweet-2054738364667228487.md)

Die zeitliche Einordnung bleibt getrennt: ein 2025 zugeordnetes Paper wird im Mai 2026 weiterverbreitet; der Post ist kein Nachweis einer neuen Paper-Veröffentlichung im Jahr 2026. [tweet-2054738364667228487](../sources/tweet-2054738364667228487.md) [tweet-2054611399792644386](../sources/tweet-2054611399792644386.md)
