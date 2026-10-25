---
tags: [tools, product-building]
sources: [tweet-2106627744427639118.md]
created: 2026-10-12
updated: 2026-10-12
---

# OpenGym

## Anwendung und Daten (Stand 2026-10)

[OpenGym](https://github.com/DuarteSantos8/openGym) ist laut README ein selbst gehosteter Trainings- und Körpergewichtstracker: Routinen planen, geführte Einheiten protokollieren, Gewichte verfolgen und Daten zwischen Geräten synchronisieren. Docker/PWA, Passkeys und Offline-Arbeit sind dokumentiert; das Originalbild zeigt Startseite, Trainingsansicht und Statistiken. [tweet-2106627744427639118](../sources/tweet-2106627744427639118.md)

Daten liegen als JSON unter ./data auf dem eigenen Host. Import ist aus FitNotes, Strong, Hevy und Apple-Health-Gewichtsexporten vorgesehen; ein JSON-Export und Plan-Sharing/PDF erlauben die Mitnahme. Zwei Geräte verwenden Revisionen und feldweise Änderungsstempel statt vollständigem Überschreiben. [tweet-2106627744427639118](../sources/tweet-2106627744427639118.md)

## Training laut gespeicherter README (Stand 2026-10)

Dokumentiert sind Wochenpläne oder A/B/C-Rotation, Supersets, Warm-ups, Cardio und eigene Übungen. Geführte Einheiten übernehmen letzte Gewichte, Resttimer und PR-Erkennung. Fortschrittsregeln umfassen lineare und doppelte/dreifache Progression; fehlende Wiederholungen erhöhen die Last nicht, Stagnation kann einen Deload auslösen. Das sind Softwarefunktionen, keine belegte individuelle Trainingswirkung. [tweet-2106627744427639118](../sources/tweet-2106627744427639118.md)

## Start und Betrieb (Stand 2026-10)

Die README nennt diesen Start; auf dem Telefon erfordern Passkeys HTTPS und eine passende RP_ID/ORIGIN-Konfiguration. [tweet-2106627744427639118](../sources/tweet-2106627744427639118.md)

```text
git clone https://github.com/DuarteSantos8/openGym
cd openGym
cp .env.example .env
docker compose pull
docker compose up -d
```

Die PWA läuft über den eigenen Server; die README bietet zusätzlich eine Android-APK sowie Xcode-Builds für eigene iPhones. Backup des ./data-Verzeichnisses sichert laut Dokumentation die Instanzdaten. [tweet-2106627744427639118](../sources/tweet-2106627744427639118.md)

## Optionale Agentenfunktionen (Stand 2026-10)

Ein ausgeschalteter AI-Coach kann mit eigenem Provider-Schlüssel Routinen entwerfen und Änderungen vorschlagen, die der Nutzer freigibt. Ein separater, lokaler, lesender [Model Context Protocol](../concepts/Model%20Context%20Protocol.md)-Server macht Trainingshistorie für Assistenten zugänglich und gehört nicht zum Docker-Build. Eine normale Installation benötigt laut README keinen LLM-Dienst. [tweet-2106627744427639118](../sources/tweet-2106627744427639118.md)

## Snapshot und Grenzen (Stand 2026-10)

Das Originalbild zeigt v1.3.8, die gespeicherte README bezeichnet v1.3.10 als veröffentlicht; spätere README-Funktionen werden damit nicht rückwirkend dem Screenshot zugeschrieben. Die App wurde hier nicht betrieben. [tweet-2106627744427639118](../sources/tweet-2106627744427639118.md)

Die README nennt AGPL für eigenen Code und getrennte, eingeschränkte Nutzungsbedingungen für Gym-Visual-Übungsmedien. Die Medien stehen nicht unter derselben offenen Code-Lizenz; Details verweist sie auf LICENSE und NOTICE.md. [tweet-2106627744427639118](../sources/tweet-2106627744427639118.md)
