---
tags: [agents, tools]
sources: [tweet-2113741692176355455.md]
created: 2026-10-25
updated: 2026-10-25
---

# System One Computer Use

## Überblick (Stand 2026-10)

System One Computer Use ist ein Open-Source-Prototyp von brainstormity (GitHub brainstormity/System-One-Computer-Use), der einen Rechner per Screenshots steuert. Die Schleife lautet: Screenshot aufnehmen, das Modell JEV (Typesafe) nach der nächsten Aktion fragen (klicken, tippen, Enter, scrollen, Website öffnen oder stoppen), die Aktion per pyautogui ausführen. [tweet-2113741692176355455](../sources/tweet-2113741692176355455.md)

## Eigenschaften laut README (Stand 2026-10)

- Der Agent ist eine einzelne Datei (`jev_agent.py`); ein kleines Dashboard zeigt je Schritt Screenshot mit markierter Klickstelle, gewählte Aktion, Sicherheit und Kosten. [tweet-2113741692176355455](../sources/tweet-2113741692176355455.md)
- JEV wählt nur aus vorgegebenen Optionen und schreibt keinen freien Text; getippt wird nur Text aus der Aufgabe. Laut README kann Text auf einer Webseite den Agenten deshalb nicht zum Tippen fremder Inhalte bringen. [tweet-2113741692176355455](../sources/tweet-2113741692176355455.md)
- Unter 50 % Sicherheit bei Klick, Eingabe, Enter oder Einfügen stoppt der Agent; harmlose Aktionen brauchen 25 %. Notstopp per Maus in eine Bildschirmecke oder Strg+C. [tweet-2113741692176355455](../sources/tweet-2113741692176355455.md)
- Kosten: Der Autor nennt etwa 0,002 $ je Aufgabe; im früheren Demo-Post 0,0019 $ und rund 50.000 Tokens. Das README nennt 0,042 $ je Million Eingabe-Tokens. Das sind Angaben des Autors und Anbieters ohne unabhängige Messung. [tweet-2113741692176355455](../sources/tweet-2113741692176355455.md)

## Grenzen (Stand 2026-10)

Das README warnt vor Produktionseinsatz: Der Agent steuert echte Maus und Tastatur ohne weitere Sicherheitsprüfung, kann auf Konten posten und bleibt laut Autor wenig getestet. Getestet ist nur macOS mit Brave und Python 3.14; Einfügen, Link-Kopieren und Tab-Schließen funktionieren nur auf macOS. Screenshots gehen an Typesafe. [tweet-2113741692176355455](../sources/tweet-2113741692176355455.md)

## Verwandte Seiten

[Browser Use](Browser%20Use.md) verfolgt ein anderes Muster der Browser-Steuerung durch Agenten. [tweet-2113741692176355455](../sources/tweet-2113741692176355455.md)
