---
tags: [tools, product-building, agents]
sources: [tweet-2021661315329405174.md]
created: 2026-10-24
updated: 2026-10-24
---

# Greenlight

## Überblick (Stand 2026-02)

Greenlight (https://github.com/RevylAI/greenlight, MIT-Lizenz, gebaut von Revyl) ist eine Vorab-Prüfung auf Konformität mit dem Apple App Store und Google Play. Es liest Quellcode, Privacy-Manifeste, Android-Manifeste und Gradle-Builds, IPA-Binaries und App-Store-Connect-Metadaten und prüft sie gegen Apples Review Guidelines und Googles Developer Program Policies; jeder Fund nennt seine Regel. [tweet-2021661315329405174](../sources/tweet-2021661315329405174.md)

Der Post beschreibt es als CLI für iOS-Apps mit Prüfung von Zahlungs- und IAP-Konformität, Privacy-Manifesten, Pflicht-Anmeldung und Konto-Verwaltung, Vollständigkeit und Metadaten sowie Binär- und Entitlement-Validierung; als Claude-Code-Skill behebe es die Funde selbst. [tweet-2021661315329405174](../sources/tweet-2021661315329405174.md)

## Befehle und Scanner

- `greenlight preflight [Pfad]` startet alle passenden Scanner parallel (metadata, codescan mit 24 Regeln für Swift, Objective-C, React Native und Expo, privacy, playscan, ipa); iOS und Android im selben Repo werden gemeinsam geprüft. Optionen: `--ipa`, `--format json|sarif`, `--exit-code`. [tweet-2021661315329405174](../sources/tweet-2021661315329405174.md)
- Vier Schweregrade: CRITICAL, HIGH, WARN, INFO. `--exit-code` schlägt bei CRITICAL, HIGH und bei einem abgestürzten Scanner fehl, ein unvollständiger Scan meldet also nie "bestanden". [tweet-2021661315329405174](../sources/tweet-2021661315329405174.md)
- playscan prüft Google-Play-Fristen und Berechtigungen, z. B. Ziel-API 36 ab 2026-08-31, Play Billing v7 und älter ab 2026-08-31 ohne Support, 16-KB-Seitengröße, 64-Bit-Pflicht; `--apk` und `--aab` lesen das zusammengeführte Manifest. [tweet-2021661315329405174](../sources/tweet-2021661315329405174.md)
- `greenlight scan --app-id` prüft per App-Store-Connect-API Metadaten, Screenshots, Build-Status, Altersfreigabe und Verschlüsselung; `greenlight guidelines` durchsucht Apples Richtlinien lokal. [tweet-2021661315329405174](../sources/tweet-2021661315329405174.md)
- Ausgabe als Terminal, JSON, SARIF (für GitHub Code Scanning) und JUnit; Regeln lassen sich in `.greenlight.yml` abschwächen oder per `// greenlight:ignore <regel>` einzeln unterdrücken. [tweet-2021661315329405174](../sources/tweet-2021661315329405174.md)

## Laufzeitprüfung (verify)

Die README räumt ein, dass ein statischer Scan nur Text liest: Ein "Delete Account"-Button ohne Funktion besteht die Prüfung, weil der String im Code steht. `greenlight verify` führt deshalb die Abläufe account-deletion (§5.1.1), restore-purchases (§3.1.1) und sign-in-apple (§4.8) auf einem Cloud-Gerät von Revyl aus und macht den Build bei einem Fehlschlag fehlgeschlagen. Diese Stufe ist nicht offline, braucht die Revyl-CLI und ein kostenloses Konto; iOS verlangt ein Simulator-`.app`, ein Geräte-`.ipa` wird abgelehnt. `--dry-run` zeigt die erzeugten Tests ohne Gerät und Konto. [tweet-2021661315329405174](../sources/tweet-2021661315329405174.md)

## Installation und Agenten-Nutzung

Installation per Homebrew (`brew install revylai/tap/greenlight`), `go install github.com/RevylAI/greenlight/cmd/greenlight@latest` oder aus dem Quellcode. Als Claude-Code-Plugin: `/plugin marketplace add RevylAI/greenlight`, dann `/plugin install greenlight`; alternativ die Datei `skills/greenlight/SKILL.md` nach `.claude/skills/` kopieren. Der Auftrag lautet sinngemäß: preflight ausführen und alles beheben, bis GREENLIT erscheint; der Agent arbeitet CRITICAL zuerst ab. Ein Codex-Skill-Paket liegt unter `codex-skill/`. [tweet-2021661315329405174](../sources/tweet-2021661315329405174.md)

## Grenzen

Laufzeitangabe "einstellige Millisekunden" und alle Wirksamkeitsaussagen stammen von der README und sind nicht unabhängig geprüft. Revyl ist Hersteller der Laufzeitstufe und bewirbt sich in der README selbst. Das Demo-Video des Posts hat kein Transkript. Verwandt: [App Store Connect CLI](App%20Store%20Connect%20CLI.md) (Release-Automatisierung statt Konformitätsprüfung). [tweet-2021661315329405174](../sources/tweet-2021661315329405174.md)
