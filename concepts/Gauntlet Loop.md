---
tags: [agents, product-building]
sources: [tweet-2081857631254372509.md]
created: 2026-10-02
updated: 2026-10-08
---

# Gauntlet Loop

## Definition (Stand 2026-07)

Matt Shumer nennt so seine Prompting-Methode für lange Agentenläufe: Ein Lead-Agent erhält ein Ziel und ein reales Beispiel dafür, wie „großartig“ aussieht, zerlegt das Ziel in kleinste separat verbesserbare Teile und gibt jedem Teil einen Builder und einen separaten Critic mit frischem Kontext. Verliert das Ergebnis gegen die Referenz, benennt der Critic die größte verbleibende Lücke und schickt die Arbeit zurück. [tweet-2081857631254372509](../sources/tweet-2081857631254372509.md)

## Regeln (Stand 2026-07)

1. **Ziel statt Implementierung:** Architektur, Arbeitsstränge und Schritte nicht vorgeben; das Modell wählt den Weg. [tweet-2081857631254372509](../sources/tweet-2081857631254372509.md)
2. **Echter Maßstab:** „Make it amazing“ ist kein Maßstab. Nötig ist etwas Prüfbares, etwa echte Call-of-Duty-Screenshots, die besten Websites einer Kategorie, Referenzabsätze, eine Testsuite, ein Latenzziel oder eine Referenzimplementierung. Der Maßstab muss nicht erreichbar sein; er gibt Richtung und verhindert frühes Aufhören. Fehlt er, wird das Finden eines Maßstabs Teil der Aufgabe. [tweet-2081857631254372509](../sources/tweet-2081857631254372509.md)
3. **Agent zerlegt selbst:** Der Lead-Agent entscheidet, welche Teile getrennt, zusammen oder parallel laufen. [tweet-2081857631254372509](../sources/tweet-2081857631254372509.md)
4. **Builder bewertet sich nie selbst:** Der Critic bekommt Ziel, Maßstab, Regeln und das echte Artefakt, aber keine Builder-Historie; er vergleicht möglichst blind wie ein A/B-Tester und prüft echte Pixel, laufendes Produkt oder Testergebnisse statt einer Zusammenfassung. [tweet-2081857631254372509](../sources/tweet-2081857631254372509.md)
5. **Keine feste Rundenzahl:** weiterlaufen, bis das Ergebnis gefällt, Verbesserungen zu klein werden oder das Compute-Budget erreicht ist. [tweet-2081857631254372509](../sources/tweet-2081857631254372509.md)

## Beobachten und Glätten (Stand 2026-07)

Für lange Läufe soll der Agent eine einfache Live-HTML-Seite oder workbench.md mit dem Fortschritt pflegen, damit man ohne Unterbrechung zuschauen kann. Optional prüft nach jeder größeren Welle ein frischer Agent das Gesamtergebnis und glättet Inkonsistenzen zwischen separat verbesserten Teilen. [tweet-2081857631254372509](../sources/tweet-2081857631254372509.md)

## Voraussetzungen (Stand 2026-07)

Die Methode braucht ein agentisches Harness wie [Claude Code](../entities/Claude%20Code.md) oder [Codex](../entities/Codex.md), kein normales Chatfenster. Shumer bevorzugte (Stand 2026-07) Claude Code mit Opus 5 für visuelle und kreative Arbeit, weil Subagenten jeweils eigenen sauberen Kontext haben, und sieht Codex stärker bei Backend-Arbeit; zusätzlich empfiehlt er die teurere Effort-Stufe ultracode. Der Artikel enthält ein Meta-Prompt-Template, das aus Ziel und optionalen Referenzen einen kurzen Gauntlet-Prompt schreibt. [tweet-2081857631254372509](../sources/tweet-2081857631254372509.md)

## Beispiel und Grenzen (Stand 2026-07)

Das Beispiel ist „Claude of Duty“: ein Shooter in Three.js aus einem Prompt, laut Artikel rund 55.000 Codezeilen nach vielen Stunden, Prompt und Code auf GitHub (mshumer/Claude-of-Duty). Andere Nutzer hätten den Prompt erfolgreich nachgebaut. Gemessen werden weder Kosten noch Qualität gegenüber anderen Methoden; Laufzeit und Zeilenzahl sind Angaben des Autors. Verwandt: [Loop Engineering](Loop%20Engineering.md), [Agent Workflow Graphs](Agent%20Workflow%20Graphs.md). [tweet-2081857631254372509](../sources/tweet-2081857631254372509.md)
