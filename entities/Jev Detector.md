---
tags: [tools, marketing]
sources: [tweet-2100627898436571555.md]
created: 2026-10-07
updated: 2026-10-07
---

# Jev Detector

## Zweck und Bezug (Stand 2026-09)

[Jev Detector](https://www.jevdetector.com/) prüft laut gespeicherter Website bis zu 10.000 Wörter ohne Anmeldung auf erkennbare KI-Schreibmuster. Jozefs Ankündigung nennt rund zwei Sekunden für diese Textmenge; die Laufzeit ist hier nicht gemessen. Das Werkzeug nutzt [Jev](Jev.md). [tweet-2100627898436571555](../sources/tweet-2100627898436571555.md)

## Review-Ablauf (Stand 2026-09)

Der Server hält die Position jedes Satzes fest, sendet begrenzte Batches und fragt nach einem Stilscore von 0 bis 4 sowie dem stärksten passenden Signal einer Wikipedia-basierten Rubrik. Markierte Stellen zeigen Satznummer, Signalkategorie, Score, Konfidenz und passende Formulierung; Pfeile führen durch die Treffer. [tweet-2100627898436571555](../sources/tweet-2100627898436571555.md)

Mit Apply & recheck lässt sich ein einzelner Satz überarbeiten und erneut prüfen. Die Änderung wird laut Website erst nach erfolgreicher Prüfung übernommen, andere Markierungen bleiben erhalten; Edit in place bearbeitet den ganzen Text. Sehr satzreiche Dokumente werden zu benachbarten Passagen zusammengefasst. [tweet-2100627898436571555](../sources/tweet-2100627898436571555.md)

## Grenzen und Verarbeitung (Stand 2026-09)

Eine Markierung ist kein Nachweis von KI-Urheberschaft: Menschen verwenden dieselben Sprachmuster. Die Website verlangt menschliches Urteil und verspricht durch Entfernen von Formulierungen keine Undetektierbarkeit; sie enthält außerdem einen StealthGPT-Werbelink. [tweet-2100627898436571555](../sources/tweet-2100627898436571555.md)

Laut Website speichert die Anwendung keine eingefügten Texte in ihrem Anwendungscode oder einer Dokumentdatenbank; Vercel und TypeSafe verarbeiten sie für den Scan. Die Quelle rät von vertraulichen Eingaben ab und verweist auf ihre Datenschutzseite. Das beschreibt Anbieterangaben, keine unabhängig geprüfte Aufbewahrungspraxis. [tweet-2100627898436571555](../sources/tweet-2100627898436571555.md)
