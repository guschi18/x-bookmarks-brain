---
tags: [tools, product-building]
sources: [tweet-2091457953757012349.md]
created: 2026-10-12
updated: 2026-10-12
---

# Marker

## Aufgabe und Ausgaben (Stand 2026-08)

Repository: https://github.com/datalab-to/marker. Die gespeicherte README beschreibt die Umwandlung von PDF, Bildern und weiteren Dokumentformaten in Markdown, JSON, HTML oder flache Chunks; Tabellen, Formeln, Bilder und Layoutstruktur werden dabei gesondert verarbeitet. [tweet-2091457953757012349](../sources/tweet-2091457953757012349.md)

JSON bewahrt eine Baumstruktur aus Seiten und Blöcken mit Typen und Koordinaten; Chunks flacht die Struktur ab und stellt vollständiges Block-HTML für flexible RAG-Aufteilung bereit. [tweet-2091457953757012349](../sources/tweet-2091457953757012349.md)

## Betriebsarten und wiederverwendbare Einstellungen (Stand 2026-08)

Die gespeicherte Dokumentation trennt balanced mit umfassenderer VLM-/OCR-Verarbeitung von fast mit leichter Layoutanalyse und selektiver Reparatur. --disable_ocr deaktiviert VLM-Aufrufe und lässt Scan-/Formelinhalte aus; --force_ocr erzwingt OCR und --use_llm ergänzt optionale LLM-Nachbearbeitung. [tweet-2091457953757012349](../sources/tweet-2091457953757012349.md)

marker_single verarbeitet einzelne Dateien, marker einen Ordner. --skip_existing setzt vorhandene Ausgaben fort; --workers steuert parallele Konverter, die sich einen Inferenzserver teilen; --num_chunks und --chunk_idx verteilen Dateien auf mehrere Maschinen. [tweet-2091457953757012349](../sources/tweet-2091457953757012349.md)

Die README nennt Surya-VLM-Inferenz mit vLLM auf NVIDIA oder llama.cpp auf CPU/Apple Silicon sowie optionale externe LLM-Dienste. Für rein digitale Dokumente ohne OCR kann die Text-/Layoutverarbeitung ohne VLM-Server laufen. [tweet-2091457953757012349](../sources/tweet-2091457953757012349.md)

## Grenzen und Lizenz (Stand 2026-08)

Komplexe verschachtelte Tabellen und Formulare bleiben dokumentierte Grenzen. Der kleine API-Server wird als nicht robust für große Last beschrieben und stellt weniger Optionen als CLI/Python bereit; Benchmark- und Qualitätszahlen sind hier nicht reproduzierte Anbieterangaben. [tweet-2091457953757012349](../sources/tweet-2091457953757012349.md)

Die README nennt Apache 2.0 für Code und zusätzliche Nutzungsbedingungen für Modellgewichte. Nicht alle Installationssnippets sind in der gespeicherten Textextraktion vorhanden; Versions-/Backendangaben sind ein Dokumentationssnapshot und keine aktuelle Installationsprüfung. [tweet-2091457953757012349](../sources/tweet-2091457953757012349.md)
