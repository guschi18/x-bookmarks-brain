---
tags: [agents, research]
sources: [tweet-2115076613461418010.md]
created: 2026-10-28
updated: 2026-10-28
---

# Agent Harness Verification

## Definition (Stand 2026-10)

Verifikation in einem Agent-Harness bedeutet, dass der Harness die Arbeit eines Coding-Agenten prüfen und überarbeiten lässt. Das Preprint 'Rethinking Verification in Agent Harnesses' (arXiv 2610.34577, 2026-10-25) ordnet Designs in vier Schichten: Anfangsanweisungen (L0), Erinnerungen während der Arbeit (L1), Completion Gates (L2) und unabhängiger Review (L3). [tweet-2115076613461418010](../sources/tweet-2115076613461418010.md)

## Befunde laut Paper

Verglichen wurden 17 Designs über sieben Coding-Modelle auf Terminal-Bench und SWE-bench Verified; dazu kommt VisualBench mit 18 visuellen Aufgaben. [tweet-2115076613461418010](../sources/tweet-2115076613461418010.md) Anweisungen und Erinnerungen bringen kleine, modellabhängige Gewinne. Completion Gates können mehr bringen, erhöhen aber die Kosten deutlich (laut Thread das 1,60- bis 1,76-fache). [tweet-2115076613461418010](../sources/tweet-2115076613461418010.md) Ein unabhängiger Critic steigert die Genauigkeit um 5,9 bis 9,5 Prozentpunkte auf Terminal-Bench (1,13- bis 1,25-facher Preis) und um 3,9 bis 6,6 auf SWE-bench (1,00- bis 1,04-facher Preis). [tweet-2115076613461418010](../sources/tweet-2115076613461418010.md) Weitere Review-Runden oder Critics bringen bis zu 3,5 Punkte zusätzlich. [tweet-2115076613461418010](../sources/tweet-2115076613461418010.md)

## Praktische Hinweise aus dem Thread

Nur 6,2 bis 13,6 Prozent der Edit-Züge folgen auf einen Prüfbefehl; die Anweisung 'prüfe deine Arbeit' allein reicht nicht. [tweet-2115076613461418010](../sources/tweet-2115076613461418010.md) Ein Reviewer, der nur den Diff erhält, schnitt bei visuellen Aufgaben besser ab als einer mit vollem Verlauf (+21,2 gegenüber +13,2 Punkte Nettopräferenz). [tweet-2115076613461418010](../sources/tweet-2115076613461418010.md)

## Evidenzgrenzen

Quelle ist ein Preprint, wiedergegeben über einen Thread und den gespeicherten Abstract; das Paper wurde nicht vollständig geprüft. Der Critic war für alle Modelle Qwen3.7-Plus. [tweet-2115076613461418010](../sources/tweet-2115076613461418010.md) Verwandt: [Verifier Setup](../entities/Verifier%20Setup.md) und [Open Code Review](../entities/Open%20Code%20Review.md). [tweet-2115076613461418010](../sources/tweet-2115076613461418010.md)
