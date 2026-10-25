---
tags: [tools, product-building]
sources: [tweet-2053429856558325835.md]
created: 2026-10-13
updated: 2026-10-13
---

# Lazycut

## Werkzeug (Stand 2026-05; gespeicherte README)

[lazycut](https://github.com/ozemin/lazycut) bietet Videoschnitt mit Vorschau im Terminal. Die gespeicherte README nennt In-/Out-Marken, mehrere Segmente, getrennten oder zusammengeführten Export und Seitenverhältnisse 16:9, 9:16, 1:1 und 4:5. Der Tweet verwendet den früheren Repository-Pfad emin-ozata/lazycut. [tweet-2053429856558325835](../sources/tweet-2053429856558325835.md)

## Bedienung und Einrichtung

`lazycut video.mp4` startet die Oberfläche; `i` und `o` setzen Schnittmarken, Komma und Punkt bewegen sich um ein Einzelbild, Enter exportiert und `u` macht die letzte Aktion rückgängig. Zählpräfixe unterstützen beispielsweise zehn Einzelbildschritte. [tweet-2053429856558325835](../sources/tweet-2053429856558325835.md)

Die CLI dokumentiert `lazycut trim --in 00:01:00 --out 00:02:00 -o out.mp4 video.mp4` sowie `lazycut probe video.mp4`. Die Preview-Bildrate ist mit `--fps` einstellbar. [tweet-2053429856558325835](../sources/tweet-2053429856558325835.md)

Die README verlangt Go, FFmpeg und Chafa samt Entwicklungspaketen und nennt `go install github.com/ozemin/lazycut@latest`. Das Bild zeigt v0.3.9. Windows-Unterstützung, Schnittgenauigkeit der exportierten Datei und aktuelle Version wurden hier nicht überprüft; es wurde nichts installiert. [tweet-2053429856558325835](../sources/tweet-2053429856558325835.md)
