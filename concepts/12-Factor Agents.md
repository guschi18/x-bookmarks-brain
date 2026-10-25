---
tags: [agents, product-building]
sources: [tweet-2100496400547041778.md]
created: 2026-10-08
updated: 2026-10-08
---

# 12-Factor Agents

## Grundidee und Quelle (Stand 2026-09)

[HumanLayers 12-Factor Agents](https://github.com/humanlayer/12-factor-agents) empfiehlt, kleine Agentenbausteine gezielt in bestehende Software einzubauen. Dex beschreibt zuverlässige Produkte als überwiegend deterministische Abläufe mit Modellschritten an ausgewählten Stellen; seine Aussagen über Framework-Grenzen sind Praxiserfahrungen, keine kontrollierte Marktstudie. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)

Dex zerlegt Tool Calling in Klassifikation und Aktion: [Jev](../entities/Jev.md) kann begrenzte Entscheidungen liefern, Anwendungscode führt Aktionen aus, und kleine Chatloops ergänzen den Ablauf. Das passt zur Trennung von Urteilen und Host-Policy in [Typed Decision Layer](Typed%20Decision%20Layer.md). [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)

## Zwölf Prinzipien (Stand 2026-09)

1. Natürliche Sprache in konkrete Tool-Aufrufe übersetzen. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
2. Prompts selbst besitzen und kontrollieren. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
3. Das Kontextfenster selbst verwalten; dazu gehört [Context Engineering](Context%20Engineering.md). [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
4. Tools als strukturierte Ausgaben behandeln. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
5. Ausführungszustand und fachlichen Zustand zusammenführen. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
6. Start, Pause und Fortsetzung durch einfache APIs zugänglich machen. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
7. Menschen über Tool-Aufrufe kontaktieren. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
8. Den Kontrollfluss selbst bestimmen. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
9. Fehler kompakt in den Kontext zurückführen. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
10. Kleine Agenten mit klar begrenzter Aufgabe einsetzen. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
11. Aus verschiedenen Ereignisquellen starten und Nutzer in ihrem Arbeitskontext erreichen. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
12. Den Agenten als zustandslosen Reducer gestalten. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)

## Loop und Grenzen (Stand 2026-09)

Das README-Beispiel lässt das Modell den nächsten Schritt als strukturierte Ausgabe wählen, hängt diese Wahl an den Kontext, beendet bei done oder führt den Tool-Aufruf deterministisch aus und ergänzt dessen Ergebnis. Der Autor beschreibt, warum ein solcher freier Loop allein seine Qualitätsanforderungen nicht zuverlässig erfüllt. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)

Die gespeicherte Quelle enthält den Überblick und Links zu den Einzelkapiteln; deren vollständige Inhalte sind hier nicht separat ausgewertet. Als zusätzlicher dreizehnter Hinweis wird das Vorabladen möglicherweise benötigten Kontexts genannt. Prinzipien und Erfahrungsberichte liefern keine allgemeine Zuverlässigkeitsgarantie. [tweet-2100496400547041778](../sources/tweet-2100496400547041778.md)
