---
tags: [tools, marketing, research]
sources: [tweet-2097920782823305690.md]
created: 2026-10-09
updated: 2026-10-09
---

# Google Maps Scrapper

## Projekt und Daten (Stand 2026-09)

[zohaibbashir/Google-Maps-Scrapper](https://github.com/zohaibbashir/Google-Maps-Scrapper) ist laut README ein MIT-lizenziertes Python-Skript mit Playwright. Es extrahiert Firmennamen, Adressen, Websites, Telefonnummern, Anzahl und Durchschnitt von Bewertungen, Öffnungszeiten sowie verfügbare Geschäftsmerkmale und Einführungen aus Google Maps. Die Schreibweise Scrapper folgt dem Repositorynamen. [tweet-2097920782823305690](../sources/tweet-2097920782823305690.md)

## Nutzung (Stand 2026-09)

Die gespeicherte Anleitung nennt Klonen des Repos, `pip install -r requirements.txt` und installierte Playwright-Browser. `python main.py -s "Turkish Restaurants in Toronto Canada" -t 20 -o results.csv --append` sucht Unternehmen, begrenzt die Zahl und hängt Ergebnisse an eine CSV an. Ohne --append wird die Ausgabe neu geschrieben; der Browser läuft sichtbar. [tweet-2097920782823305690](../sources/tweet-2097920782823305690.md)

## Voraussetzungen und Grenzen (Stand 2026-09)

Die README empfiehlt Python 3.8/3.9 und warnt vor möglicher Inkompatibilität ab 3.10. Main, Latest Libraries und Linux sind unterschiedliche Branches; Main wird bevorzugt. Änderungen am Maps-DOM können die XPaths in main.py brechen, häufige Abrufe können blockiert werden. Funktionsfähigkeit und Datenabdeckung wurden hier nicht getestet. [tweet-2097920782823305690](../sources/tweet-2097920782823305690.md)

[Lead Generation](Lead%20Generation.md) ist ein anderes Repository mit verwandtem Google-Maps-/CSV-Zweck; dieses Werkzeug liefert eine eigene Playwright-Implementierung und dokumentierte Ausgabeoptionen. [tweet-2097920782823305690](../sources/tweet-2097920782823305690.md)
