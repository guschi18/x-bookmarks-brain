---
tags: [tools, product-building, research]
sources: [tweet-2071025590145003686.md]
created: 2026-10-08
updated: 2026-10-08
---

# Exercises Dataset

## Datensatz und zeitlicher Geltungsbereich (Poststand 2026-06)

[hasaneyldrm/exercises-dataset](https://github.com/hasaneyldrm/exercises-dataset) wird von Tom Dörr als Fitness-Datensatz mit Animations-GIFs und zweisprachigen Anleitungen verlinkt. Die gespeicherte README nennt 1.324 Übungen und zehn Anleitungssprachen, ihr gespeicherter Titel sechs. Der Body kann einen späteren Projektstand enthalten; die zehn Sprachen werden nicht rückwirkend dem Post vom 28.06.2026 zugeschrieben. [tweet-2071025590145003686](../sources/tweet-2071025590145003686.md)

## Datenmodell der gespeicherten README (Bezug: Poststand 2026-06)

`data/exercises.json` enthält laut README ID, Name, Körperregion, Gerät, Ziel-/Muskelgruppen, Sekundärmuskeln, Anleitungen und geordnete Anleitungsschritte pro Sprache. Hinzu kommen 180×180-Thumbnails, GIF-Pfade, media_id und Attribution; `data/exercises.schema.json` definiert das Schema nach JSON Schema 2020-12. [tweet-2071025590145003686](../sources/tweet-2071025590145003686.md)

Die Sprachliste im Body lautet Englisch, Spanisch, Italienisch, Türkisch, Russisch, Chinesisch, Hindi, Polnisch, Koreanisch und Französisch. Die README nennt 325 Übungen mit Körpergewicht, also ungefähr ein Viertel des Bestands. Das sind Projektangaben des gespeicherten Dokuments, keine eigene Datenprüfung. [tweet-2071025590145003686](../sources/tweet-2071025590145003686.md)

## Erkunden und integrieren (Bezug: Poststand 2026-06)

`index.html` bietet laut README eine rein clientseitige Suche und Filter nach Körperregion, Gerät und Zielmuskel mit Detailansichten und Animationen. `setup.html` erzeugt Datenbanktabellen und SQL-Importe für SQL Server, PostgreSQL, MySQL und SQLite. [tweet-2071025590145003686](../sources/tweet-2071025590145003686.md)

Die Setup-Seite enthält Clientbeispiele für mehrere Sprachen und einen Prompt für eine REST-API mit gewähltem Framework und Datenbank; Beispiele umfassen Express, FastAPI, ASP.NET Core, Spring Boot, Laravel und Gin. Die Bezeichnung production-ready ist eine Projektbehauptung, kein hier ausgeführter API- oder Sicherheitstest. [tweet-2071025590145003686](../sources/tweet-2071025590145003686.md)

Die README bezeichnet den Datensatz als Datenebene des [LogPress-Trackers](https://github.com/hasaneyldrm/logpress-public) und zeigt direkte JSON-/Pandas-/JavaScript-Filter als Integrationsbeispiele. Er dient damit als konkretes Entwicklungsartefakt; medizinische Wirksamkeit oder Qualität der Übersetzungen wurde hier nicht geprüft. [tweet-2071025590145003686](../sources/tweet-2071025590145003686.md)

## Nutzungsbedingungen der gespeicherten README (Bezug: Poststand 2026-06)

Die [Lizenz](https://github.com/hasaneyldrm/exercises-dataset/blob/main/LICENSE) unterscheidet MIT-Code, Datenstruktur und Anleitungstext von Bildern und GIFs von Gym visual. Die README behauptet erlaubte Weitergabe in 180×180-Auflösung, verlangt erhaltene Attribution und verweist für eigene Mediennutzung auf eine eigene Gym-visual-Lizenz. Die Medien dürfen daher nicht pauschal als MIT übernommen werden; maßgebliche Dokumente sind LICENSE und [NOTICE.md](https://github.com/hasaneyldrm/exercises-dataset/blob/main/NOTICE.md). Das ist die Wiedergabe gespeicherter Projektbedingungen, keine rechtliche Prüfung. [tweet-2071025590145003686](../sources/tweet-2071025590145003686.md)
