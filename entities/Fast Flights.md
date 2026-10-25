---
tags: [tools, research]
sources: [tweet-2098011339381707216.md]
created: 2026-10-09
updated: 2026-10-09
---

# Fast Flights

## Zweck und API (Stand 2026-09)

[AWeirdDev/flights](https://github.com/AWeirdDev/flights) beschreibt fast-flights als typisierten Python-Scraper für Google Flights. Installation: `pip install fast-flights`. FlightQuery hält Datum und dreibuchstabige Flughafencodes; create_query kombiniert Flugabschnitte, Reiseklasse, Reiseart, Passengers und Sprache, get_flights führt die Abfrage aus. [tweet-2098011339381707216](../sources/tweet-2098011339381707216.md)

## Filter (Stand 2026-09)

Pro Flugabschnitt sind Umstiege, Airlines, lokale Abflug-/Ankunftsstunden, maximale Dauer, Anschlussflughäfen und Umsteigezeiten beschrieben. Suchweit sind Währung, Preisobergrenze, Gepäck und Ausschluss von Basic Economy beziehungsweise separaten Selbsttransfers konfigurierbar. Stunden sind lokale Flughafenzeit von 0 bis 23, Dauern Minuten und Preise in der gewählten Währung; laut README wendet Google den Airlinefilter des ersten Abschnitts auf die ganze Suche an. [tweet-2098011339381707216](../sources/tweet-2098011339381707216.md)

## Mechanismus und Entwicklung (Stand 2026-09)

Der Autor erklärt das Reverse Engineering des tfs-URL-Parameters: Base64 dekodieren, Protobuf-Struktur untersuchen und Reiseparameter rekonstruieren. Die Versionsnotizen nennen Playwright-Fallbacks für v2 und JavaScript-Daten statt früherem HTML-Parsing für v3. Der historische Entstehungsbericht beschreibt damit nicht allein den aktuellen v3-Auslesepfad. [tweet-2098011339381707216](../sources/tweet-2098011339381707216.md)

## Integrationen und Grenzen (Stand 2026-09)

BrightData und das gesponserte SearchApi sind optionale externe Integrationen; SearchApiResult nennt zusätzlich günstigere Alternativen, Preisanalysen und Buchungsoptionen. Das Projekt ist ein Scraper, keine offizielle Google-API; Geschwindigkeit, Stabilität und Flugpreisabdeckung wurden hier nicht geprüft. Ein interner GetShoppingResults-API-Pfad steht in der Roadmap, nicht als bestätigte vorhandene Funktion. [tweet-2098011339381707216](../sources/tweet-2098011339381707216.md)
