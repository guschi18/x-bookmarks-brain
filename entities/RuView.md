---
tags: [tools, research]
sources: [tweet-2030701562117468580.md]
created: 2026-10-22
updated: 2026-10-22
---

# RuView

## Projekt und Quellenstand

[RuView](https://github.com/ruvnet/RuView) beschreibt WiFi-Sensing über Channel State Information (CSI) für Präsenz, Bewegung und experimentelle Vitalzeichen-/Pose-Anwendungen. Der Post vom 08.03.2026 ist eine Grok-Antwort, keine unabhängige Bestätigung. Die später gespeicherte umfangreiche README enthält Modelle, Korrekturen und Integrationen, die nicht pauschal dem Märzstand zugeschrieben werden. Beide HTTP-/HTTPS-Artikelkopien stammen vom selben Repository. [tweet-2030701562117468580](../sources/tweet-2030701562117468580.md)

## Hardware und Einstieg laut README

Reale CSI-Erfassung verlangt ESP32-S3/C6 oder geeignete Forschungs-Netzwerkkarten. Gewöhnliche Laptops liefern laut README nur RSSI für grobe Präsenz-/Bewegungserkennung. Der Docker-Einstieg mit ruvnet/wifi-densepose:latest verwendet simulierte Daten und beweist keine Live-Erkennung. [tweet-2030701562117468580](../sources/tweet-2030701562117468580.md)

Die Dokumentation trennt Firmware-Flashen, WLAN-Provisionierung, Sensordaten-Erfassung, Kalibrierung und Modelltraining. Geeignete Einstiege sind die im vollständigen Source-Beleg verlinkten User-, Build- und Calibration-Guides; Zugangsdaten und gerätespezifische Flash-Adressen müssen zur eigenen Hardware passen. Es wurde kein Gerät betrieben. [tweet-2030701562117468580](../sources/tweet-2030701562117468580.md)

## Modelle: Benchmark ist keine Live-Pose-Garantie

Die gespeicherte README meldet für einen CSI-Encoder 82,3 Prozent held-out temporal-triplet accuracy und zieht eine frühere 100-Prozent-Präsenzzahl aus einem Einklassen-Datensatz zurück. Das ist eine andere Metrik als Präsenzerkennung im eigenen Raum. [tweet-2030701562117468580](../sources/tweet-2030701562117468580.md)

Für das getrennte MM-Fi-Posemodell nennt sie 82,69 Prozent torso-PCK@20 auf random_split; die Live-ESP32-Kompatibilität sei damit nicht belegt. Das lokale pose_v1-Modell erreiche dagegen nur 3,0 Prozent PCK@20, und der beschriebene Laufzeitpfad liefere noch ein zentriertes Stub-Skelett mit confidence=0. Die Aussage, ein einzelner ESP32 liefere bereits zuverlässig 17 Körperpunkte, wird dadurch nicht getragen. [tweet-2030701562117468580](../sources/tweet-2030701562117468580.md)

Die Dual-Modal-Demo verwendet eine Webcam für Ground-Truth-Pose. Andere Aussagen betreffen Forschungsentwürfe oder synthetische Ergebnisse; die komplette README und ihre Links bewahren diese unterschiedlichen Reifegrade. [tweet-2030701562117468580](../sources/tweet-2030701562117468580.md)

## Integrationen und Grenzen

Die gespeicherte README dokumentiert Home-Assistant-/MQTT- und Matter-Brücken sowie eigene [Claude Code](Claude%20Code.md)-/[Codex](Codex.md)-Hilfen für Setup, Training und Verifikation. Das sind Projektangaben, keine hier geprüften Ende-zu-Ende-Integrationen. [tweet-2030701562117468580](../sources/tweet-2030701562117468580.md)

Das Projekt warnt selbst, dass medizinische, Notfall- und Sicherheitsanwendungen unabhängige Validierung für Hardware, Raum, Personen und Fehlerfälle benötigen. Werbeaussagen zu Reichweite, Vitalzeichen und Datenschutz werden nicht als geprüfte Garantien übernommen; kamerafreie Erfassung allein belegt keine regulatorische Ausnahme. [tweet-2030701562117468580](../sources/tweet-2030701562117468580.md)
