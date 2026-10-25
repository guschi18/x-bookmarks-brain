---
tags: [llm-training, research]
sources: [tweet-2044402750809940302.md]
created: 2026-10-21
updated: 2026-10-21
---

# Memory Caching

## Mechanismus (Stand 2026-04)

Memory Caching erweitert rekurrente Modelle, deren einzelner Zustand ältere Information überschreiben kann: Die Sequenz wird segmentiert, Zustände werden an Segmentgrenzen gespeichert, und spätere Tokens greifen auf diese Checkpoints zu. Der Post nennt O(NL) bei N Segmenten gegenüber O(L) für ein festes RNN-Gedächtnis und quadratischer Attention; die Segmentwahl bestimmt den Aufwand. Die separat geprüfte [Paper-Zusammenfassung](https://arxiv.org/abs/2602.24281) bestätigt den flexiblen Übergang zwischen fester und wachsender Speicherkapazität. [tweet-2044402750809940302](../sources/tweet-2044402750809940302.md)

## Vier Varianten

- Residual Memory summiert gespeicherte Zustände. [tweet-2044402750809940302](../sources/tweet-2044402750809940302.md)
- Gated Residual Memory gewichtet Segmente abhängig vom aktuellen Input. [tweet-2044402750809940302](../sources/tweet-2044402750809940302.md)
- Memory Soup interpoliert Parameter gespeicherter Gedächtnisse zu einem tokenabhängigen Netzwerk. [tweet-2044402750809940302](../sources/tweet-2044402750809940302.md)
- Sparse Selective Caching wählt über Routing nur relevante Segmente aus. [tweet-2044402750809940302](../sources/tweet-2044402750809940302.md)

## Ergebnisse und Grenzen

Der Post beschreibt Gated Residual Memory als stärkste Variante über die untersuchten Aufgaben und Verbesserungen auch für Titans. Transformer bleiben laut Post und Paper bei anspruchsvollem Recall vorn. Die Versuche bis 1,3 Milliarden Parameter belegen keine Übertragbarkeit auf Frontier-Modelle; Benchmarks wurden hier nicht repliziert. [tweet-2044402750809940302](../sources/tweet-2044402750809940302.md)

Dieses Modellgedächtnis ist eine Architekturtechnik; [Prompt Caching](Prompt%20Caching.md) behandelt dagegen die Wiederverwendung von Eingabekontext und ist kein Synonym. [tweet-2044402750809940302](../sources/tweet-2044402750809940302.md)
