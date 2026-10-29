---
tags: [agents, tools, security]
sources: [tweet-2115010135588589932.md]
created: 2026-10-28
updated: 2026-10-28
---

# Open Code Review

## Rolle (Stand 2026-10)

Open Code Review ist ein quelloffenes CLI-Tool für KI-gestützte Code-Reviews. Laut README war es zwei Jahre Alibabas interner Review-Assistent für zehntausende Entwickler und fand Millionen Defekte, bevor es veröffentlicht wurde. [tweet-2115010135588589932](../sources/tweet-2115010135588589932.md) Es liest Git-Diffs, schickt geänderte Dateien über einen Agenten mit Tool-Zugriff an ein konfigurierbares LLM und erzeugt Kommentare auf Zeilenebene. [tweet-2115010135588589932](../sources/tweet-2115010135588589932.md) Der Agent kann ganze Dateien lesen und die Codebasis durchsuchen; `ocr scan` prüft ganze Dateien ohne Diff. [tweet-2115010135588589932](../sources/tweet-2115010135588589932.md)

## Funktionen laut Post

Der Post nennt eingebaute Regeln für Null-Pointer, Thread-Sicherheit, XSS und SQL-Injection sowie Anbindung an Claude Code und Codex. [tweet-2115010135588589932](../sources/tweet-2115010135588589932.md)

## Benchmark und Evidenzgrenzen

Die README behauptet bei gleichem Modell höhere Precision und F1 als Claude Code bei etwa einem Neuntel der Tokens und schnellerer Laufzeit. [tweet-2115010135588589932](../sources/tweet-2115010135588589932.md) Grundlage ist der AACR-Bench aus 200 Pull Requests in 50 Repositories und 10 Sprachen mit 1.505 annotierten Fehlern. [tweet-2115010135588589932](../sources/tweet-2115010135588589932.md) Der Recall liegt laut README niedriger als bei allgemeinen Agenten, bewusst zugunsten der Precision. [tweet-2115010135588589932](../sources/tweet-2115010135588589932.md) Das sind Herstellerangaben; der Tweet nennt den niedrigeren Recall nicht. [tweet-2115010135588589932](../sources/tweet-2115010135588589932.md) Vergleiche zum Prüfen durch einen getrennten Reviewer: [Agent Harness Verification](../concepts/Agent%20Harness%20Verification.md). [tweet-2115010135588589932](../sources/tweet-2115010135588589932.md)
