---
tags: [tools, product-building]
sources: [tweet-2053758121571422611.md]
created: 2026-10-13
updated: 2026-10-13
---

# Website Downloader

## Werkzeug (Stand 2026-05; gespeicherte README)

[AhmadIbrahiim/Website-downloader](https://github.com/AhmadIbrahiim/Website-downloader) stellt eine Node.js-Weboberfläche vor wget. Das Programm lädt Website-Dateien samt Assets, komprimiert sie mit archiver und sendet das Archiv über eine Socket-Verbindung zurück. [tweet-2053758121571422611](../sources/tweet-2053758121571422611.md)

Der gespeicherte Mirror-Befehl ist `wget --mirror --convert-links --adjust-extension --page-requisites --no-parent http://example.org`: rekursiver Download, relative Links für Offlineansicht, passende Dateiendungen, notwendige CSS/Bilder und kein Aufstieg ins übergeordnete URL-Verzeichnis. [tweet-2053758121571422611](../sources/tweet-2053758121571422611.md)

## Einrichtung und Grenzen

Die README verlangt Node.js 16 oder neuer sowie wget im PATH. Nach Klonen des Repositorys werden `npm install` und `npm start` ausgeführt; die Oberfläche liegt standardmäßig auf `http://localhost:3000/`. Für Windows nennt die README `winget install JernejSimoncic.Wget`. Diese Anleitung wurde nicht lokal ausgeführt. [tweet-2053758121571422611](../sources/tweet-2053758121571422611.md)

Als Einstellungen nennt der gespeicherte Text `PORT=3000`, `DOWNLOAD_QUOTA=100m` und `DOWNLOAD_TIMEOUT_MS=300000`. Quota und Zeitlimit sollen Downloads begrenzen; ihre tatsächliche Durchsetzung ist hier nicht getestet. [tweet-2053758121571422611](../sources/tweet-2053758121571422611.md)

Die Behauptung „complete source code“ bezieht sich im dokumentierten Ablauf auf ausgelieferte Webdateien und Assets. Backend-Code, Datenbanken oder eine vollständige Reproduktion dynamischer Anwendungen sind dadurch nicht belegt. Der Screenshot zeigt einen abgeschlossenen Download, keinen unabhängigen Funktionstest. [tweet-2053758121571422611](../sources/tweet-2053758121571422611.md)
