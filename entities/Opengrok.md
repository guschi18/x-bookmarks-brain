---
tags: [agents, tools]
sources: [tweet-2093077239873069058.md]
created: 2026-10-10
updated: 2026-10-10
---

# Opengrok

## Rolle und Einrichtung (Stand 2026-08; gespeicherte README)

[OnlyTerp/opengrok](https://github.com/OnlyTerp/opengrok) ist laut README ein Konfigurations-Sidecar für eine vorhandene Grok-Bot-Installation. Es bindet externe oder lokale Modelle pro Agent, bietet einen Modellwähler und Diagnosewerkzeuge und ersetzt nicht den Grok-Bot-Host. Voraussetzungen sind Grok Bot, Python ab 3.9, Node ab 18 und Zugangsdaten für die gewählten Provider. [tweet-2093077239873069058](../sources/tweet-2093077239873069058.md)

```bash
git clone https://github.com/OnlyTerp/opengrok
cd opengrok
python setup.py
python tools/doctor.py
python tools/qa.py
```

Diese Befehle stammen aus der gespeicherten README; Installation und Ergebnis wurden nicht ausgeführt. [tweet-2093077239873069058](../sources/tweet-2093077239873069058.md)

## Provider-Steuerung und Cloud

Die README unterscheidet direkte Provider-Mappings und Hop-Routen über eine OpenAI-kompatible Basis-URL. Reasoning, Effort und Fast-Modus werden je Modellfamilie anders übertragen; ein HTTP-200 allein gilt nicht als Beweis dafür, dass der Provider eine Einstellung beachtet. Wire-Captures und Verhaltenstests sollen diese Unterschiede belegen. Die genannten Testzahlen sind Projektaussagen. [tweet-2093077239873069058](../sources/tweet-2093077239873069058.md)

Cloud-Hosts lesen laut README lokale model-bindings.json nicht automatisch: Ein Binding-Consumer, Dateiübertragung, Host-Neustart und anschließende Verifikation bilden einen separaten Ablauf. Der Doctor erkennt Änderungen an Dateien, Diensten und Caches nach Grok-Updates. [tweet-2093077239873069058](../sources/tweet-2093077239873069058.md)

## Zusätzliche dokumentierte Bausteine und Grenzen

Die gespeicherte README enthält eine lokale Brücke von Chat Completions zu Responses für [Codex](Codex.md) Everywhere sowie eine lokale Voice-Pipeline aus STT, Realtime-Brain und ElevenLabs-TTS. Zugangsschlüssel sollen außerhalb der Bindings bleiben. Der Launch-Post verspricht Nutzung von Abos und eigene Cloud-PCs; daraus folgt keine geprüfte Unterstützung beliebiger Abos oder unabhängiger Rechner. [tweet-2093077239873069058](../sources/tweet-2093077239873069058.md)

Die README nennt MIT und unterschiedliche Reifegrade je Provider; OpenRouter, Groq und Mistral sind dort noch als Capture-pending markiert. Dokumentation, Kompatibilität und Sicherheitsbehauptungen wurden nicht praktisch verifiziert. [tweet-2093077239873069058](../sources/tweet-2093077239873069058.md)
