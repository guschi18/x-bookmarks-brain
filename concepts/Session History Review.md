---
tags: [agents, product-building]
sources: [tweet-2102481940742115352.md, tweet-2106143340794454346.md, tweet-2105390978777690480.md, tweet-2110475744056877503.md]
created: 2026-10-03
updated: 2026-10-23
---

# Session History Review

## Definition

Ein Agent liest alle lokalen Sitzungen eines Projekts aus [Claude Code](../entities/Claude%20Code.md), [Codex](../entities/Codex.md) und anderen Tools zusammen mit Dateien, Instruktionen und Plänen, weil Korrekturen, Fehlversuche und Entscheidungen oft nie in die Projektinstruktionen gelangen. [tweet-2102481940742115352](../sources/tweet-2102481940742115352.md)

## Ablauf

1. Sitzungen lesen, bei großer Historie in Batches mit gesicherten Befunden. [tweet-2102481940742115352](../sources/tweet-2102481940742115352.md)
2. Nach wiederholten Instruktionen, manuellen Aufgaben, fehlender Information, gescheiterten Ansätzen und Unfertigem suchen, mit Verweis auf Sitzung und Datei. [tweet-2102481940742115352](../sources/tweet-2102481940742115352.md)
3. Jeden Befund am aktuellen Stand prüfen, Verbesserungen nach Wirkung und Aufwand ranken und vor Änderungen auf Freigabe warten. [tweet-2102481940742115352](../sources/tweet-2102481940742115352.md)
4. Umsetzen und testen, etwa per Playwright oder Probelauf, dann Erkenntnisse in Instruktionen, Skills und Skripte übernehmen. [tweet-2102481940742115352](../sources/tweet-2102481940742115352.md)

## Grenzen

Alte Sitzungen können bereits behobene Probleme beschreiben; daher die Prüfung gegen den aktuellen Code. Vorgestellt mit [Claude Opus 5.5](../entities/Claude%20Opus%205.5.md). Eine persönliche statt projektbezogene Lesart desselben Verlaufs beschreibt [Agent History Reflection](Agent%20History%20Reflection.md). [tweet-2102481940742115352](../sources/tweet-2102481940742115352.md)

## Additions (Stand 2026-10)

The [Claude Code Mods](../entities/Claude%20Code%20Mods.md) example asks an agent to identify repeated instructions, recurring tasks and friction in session logs, then propose five useful UI mods. The author reviews the suggestions before building; the complete reusable prompt is on the mods page. [tweet-2106143340794454346](../sources/tweet-2106143340794454346.md)

## /insights als Einstieg (Stand 2026-09)

RoundtableSpace empfiehlt /insights in [Claude Code](../entities/Claude%20Code.md), um Aufgaben, wiederkehrende Schwierigkeiten und bisher ungenutzte Funktionen aus dem Sitzungsverlauf zu identifizieren. Der Post nennt Opus 5.5 und die letzten 200 Sitzungen; diese Details sind unbestätigte Angaben des Autors. [tweet-2105390978777690480](../sources/tweet-2105390978777690480.md)

Das gespeicherte Video hat ein leeres Transkript. Es belegt hier keine weiteren Funktionen, und eine automatisierte Analyse ersetzt nicht die Prüfung der Befunde gegen den heutigen Projektstand. [tweet-2105390978777690480](../sources/tweet-2105390978777690480.md)

## Liegengebliebene Arbeit finden (Stand 2026-10)

Vox nennt einen Prompt für Opus 5.5, der die letzten 20 Sessions durchsucht (die .jsonl-Logs unter ~/.claude/projects/ ohne die laufende Session; wegen der Größe per Stichwort suchen statt ganz lesen). Er sucht drei Arten: Dinge, die man später erledigen wollte, Probleme außerhalb der damaligen Aufgabe (toter Code, veraltete Doku, fehlende Tests, Sicherheitsrisiken) und halb abgebrochene Aufgaben. Jeder Fund braucht ein wörtliches Zitat mit Session und Datei, wird gegen den aktuellen Code abgehakt und nach Wirkung gerankt; zuerst erscheint nur die Liste, dann je Auswahl eine Karte für eine neue Session. [tweet-2110475744056877503](../sources/tweet-2110475744056877503.md)

Die Prüfung gegen den heutigen Code entspricht der Grenze oben: Alte Sessions können bereits Erledigtes beschreiben. Der Kartenablauf hängt an der Desktop-App (siehe [Claude Code](../entities/Claude%20Code.md)). [tweet-2110475744056877503](../sources/tweet-2110475744056877503.md)
