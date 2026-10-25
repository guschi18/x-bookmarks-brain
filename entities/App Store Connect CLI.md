---
tags: [tools, product-building]
sources: [tweet-2096595527085555965.md, tweet-2021661315329405174.md]
created: 2026-10-02
updated: 2026-10-24
---

# App Store Connect CLI

## Überblick (Stand 2026-09)

App Store Connect CLI (`asc`, Repository https://github.com/rorkai/App-Store-Connect-CLI) ist laut README ein schnelles, skriptbares CLI für die App Store Connect API. Es automatisiert Release-Abläufe für iOS, macOS, tvOS und visionOS aus Terminal, IDE oder CI/CD, darunter TestFlight, Builds, Einreichungen, Signierung, Analytics, Screenshots und Abonnements. Rudrank Riyam kündigt Version 5.0.0 als eines seiner größten Releases an. [tweet-2096595527085555965](../sources/tweet-2096595527085555965.md)

## Einrichtung

Installation per Homebrew (`brew install asc`), Install-Skript für macOS/Linux oder WinGet; Release-Binaries sind eigenständig und brauchen kein Go. Die Anmeldung nutzt einen App-Store-Connect-API-Key (`asc auth login` mit Key-ID, Issuer-ID und .p8-Datei); ohne Keychain gibt es eine dateibasierte Konfiguration, `asc auth doctor` prüft die Anmeldung. [tweet-2096595527085555965](../sources/tweet-2096595527085555965.md)

## Agenten- und Skriptnutzung

- Ausgabe ist TTY-abhängig: Tabelle im Terminal, JSON in Pipes, Dateien und CI; `--output` hat Vorrang vor `ASC_DEFAULT_OUTPUT`. [tweet-2096595527085555965](../sources/tweet-2096595527085555965.md)
- `asc install-skills` kopiert 25 Agent-Skills aus rorkai/app-store-connect-cli-skills von einem fest geprüften Commit in das globale Skills-Verzeichnis, pinnt die Lock-Einträge, verifiziert alle Dateien und rollt bei Fehlern zurück; benötigt wird nur git. [tweet-2096595527085555965](../sources/tweet-2096595527085555965.md)
- Die Release-Prüfung warnt vor Platzhaltern wie „Lorem ipsum“, TODO, TBD oder FIXME in lokalisierten Store-Texten; ein `--deep`-Modus nutzt zusätzlich private Apple-Web-Endpunkte, deren Ausfall als ungeprüft statt als Blocker gilt. [tweet-2096595527085555965](../sources/tweet-2096595527085555965.md)
- `asc system-status` prüft Apples Entwicklerdienste ohne Anmeldung. [tweet-2096595527085555965](../sources/tweet-2096595527085555965.md)

## Telemetrie und Grenzen

Die README beschreibt Telemetrie mit zufälliger Installations-ID, Befehlspfad, Dauer und Ergebnisklasse ohne Argumente, Zugangsdaten oder App-IDs; abschaltbar per `ASC_TELEMETRY_DISABLED=1` oder `DO_NOT_TRACK=1`. Die gespeicherte README ist ein Momentstand ohne 5.0.0-Release-Notes; welche Funktionen neu in 5.0.0 sind, ist nicht belegt. Verwandt: [Claude Code](Claude%20Code.md). [tweet-2096595527085555965](../sources/tweet-2096595527085555965.md)

## Verwandt: Konformitätsprüfung (Stand 2026-02)

Vor der Einreichung prüft [Greenlight](Greenlight.md) eine App offline gegen die App-Store- und Play-Richtlinien und lässt sich als Claude-Code-Skill einsetzen; es ergänzt Release-Automatisierung wie dieses CLI, ersetzt sie aber nicht. [tweet-2021661315329405174](../sources/tweet-2021661315329405174.md)
