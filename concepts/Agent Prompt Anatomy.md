---
tags: [agents, product-building]
sources: [tweet-2104576851863822513.md]
created: 2026-10-06
updated: 2026-10-06
---

# Agent Prompt Anatomy

## Aufbau (Stand 2026-09)

Der betrachtete Screenshot gliedert eine vollständige Agentenanweisung in Goal, Return Format, Warnings und Context Dump. Der Post bezeichnet ihn als überarbeitete Vorlage; die Zuschreibung an Greg Brockman ist nicht unabhängig bestätigt. [tweet-2104576851863822513](../sources/tweet-2104576851863822513.md)

## Konkretes Einkaufsbeispiel (Stand 2026-09)

Ziel: 40 ergonomische Bürostühle für ein neues Büro in San Francisco, insgesamt unter 20.000 Dollar, gut bewertet für ganztägigen Komfort und Ankunft binnen zwei Wochen. [tweet-2104576851863822513](../sources/tweet-2104576851863822513.md)

Ausgabe je Option: Modell, Händler, dessen Baselayer-Verifikationsstatus, Stückpreis, Gesamtkosten, Lieferdatum und Begründung. Die besten drei Optionen zurückgeben und vor Checkout auf menschliche Freigabe warten. [tweet-2104576851863822513](../sources/tweet-2104576851863822513.md)

Grenzen: nur Baselayer-verifizierte Händler verwenden, am Checkout die Baselayer-Identität vorzeigen und die Karte nie auf einer Seite ohne Gegenparteiverifikation eingeben. Diese Prüfmechanik ist produktspezifischer Vorlageninhalt, keine hier belegte Sicherheitsgarantie. [tweet-2104576851863822513](../sources/tweet-2104576851863822513.md)

Kontext: ein 40-köpfiges Fintech-Team zieht um; eine frühere Agentenbestellung bei einem frisch registrierten Händler ging verloren, die Finanzabteilung ist vorsichtig und über acht Stunden sitzende Arbeit macht Komfort wichtiger als Optik. Ein anderer Händler blockierte Agenten als Bots; der Einkauf soll als Nachweis für weitere Beschaffungen dienen. [tweet-2104576851863822513](../sources/tweet-2104576851863822513.md)

## Wiederverwendung und Grenze (Stand 2026-09)

Aus diesem Beispiel lassen sich Ziel und messbare Grenzen, Vergleichsfelder, Freigabepunkt und Hintergrund getrennt vorgeben. Budget, Produkt, Händlerprüfung und Kontext müssen zur eigenen Aufgabe passen; das ist eine Vorlagenstruktur ohne belegte Ergebnisverbesserung. Verwandt: [Agent-First Product Design](Agent-First%20Product%20Design.md). [tweet-2104576851863822513](../sources/tweet-2104576851863822513.md)
