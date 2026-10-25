---
tags: [product-building, agents]
sources: [tweet-2093396854822052158.md]
created: 2026-10-09
updated: 2026-10-09
---

# Bill Dash

## Konzept und Beleg (Stand 2026-08)

Bill Dash ist in dieser Quelle ein App-Konzept in einem vollständig lesbaren Bildprompt: Freunde fahren zu einem gemeinsamen Ziel, und der zuletzt Ankommende soll die Rechnung zahlen. Der Tweet behauptet einen One-Shot-Bau in fünf Minuten, zeigt jedoch keine überprüfte fertige Implementierung. Die detaillierten Bildanforderungen sind in [tweet-2093396854822052158](../sources/tweet-2093396854822052158.md) textlich aufgelöst. [tweet-2093396854822052158](../sources/tweet-2093396854822052158.md)

## Nutzerfluss und visuelle Spezifikation

Der Prompt verlangt Splash/Home, Start a Dash, eine Lobby mit Sitzungscode und die Wahl stilisierter Voxel-Fahrzeuge. Eine Midnight-Neon-V3-Karte kombiniert Kohle-/Navy-Grund, elektrisch blaue Straßen, ein pulsierendes cyanfarbenes Eigenroutenband und dünne gestrichelte Linien für andere Teilnehmer. Das dynamische Arby’s-Ziel trägt Logo und Geofence-Ring. [tweet-2093396854822052158](../sources/tweet-2093396854822052158.md)

Topbar und Avatarleiste sollen Geschwindigkeit, Fahrzeug-Icons, Status und farbige Ränder zeigen; unten liegen Ghost Mode, Kamera hinter dem Fahrzeug und OTS-44-Kartenansicht. Ghost Mode verbirgt die Position für 90 Sekunden mit fünf Minuten Cooldown. Diese Angaben sind Anforderungen des Prompts, keine nachgewiesenen Produktfunktionen. [tweet-2093396854822052158](../sources/tweet-2093396854822052158.md)

## Echtzeitmodell und Regeln

WebSockets über socket.io oder Pusher sollen Koordinaten und Geschwindigkeit alle 500 ms übertragen. Nutzer speichern ID, Name, Avatar, Fahrzeug, GPS, Geschwindigkeit, Richtung und Ankunftshistorie; Sessions speichern Host, Ziel, Teilnehmer, Start und verifizierbare Ankunftszeiten. Serverseitiges Geofencing nutzt einen Zielradius von 30 Metern; der letzte aktive Teilnehmer erhält lost. [tweet-2093396854822052158](../sources/tweet-2093396854822052158.md)

Mehr als zwei Minuten offline bedeutet automatisch Letzter, mit Ausnahme ebenfalls ausfallender anderer Teilnehmer. Der Prompt verlangt Strafen für Ghost-Mode-Missbrauch, Live-Ankunftsverfolgung, Leaderboard und finale Anzeige des Letzten. Die konkreten Konflikt- und Strafberechnungen sind dabei nicht ausformuliert. [tweet-2093396854822052158](../sources/tweet-2093396854822052158.md)

## Vorgeschlagener Stack und Grenzen

Als Optionen nennt die Vorlage React Native oder Flutter, Node.js/Redis, socket.io, Mapbox GL JS oder Google Maps sowie MongoDB Atlas Device Sync. Dazu verlangt sie CRUD für Nutzer/Sessions, Kartenlayer, Verbindungsverwaltung, Geofencing- und Leaderboard-API, Batterieoptimierung durch GPS-Polling und binäre Updates sowie mobile Voxel-Assets. Diese historische Technologieliste ist keine geprüfte aktuelle Architektur oder Empfehlung. [tweet-2093396854822052158](../sources/tweet-2093396854822052158.md)

Die erste Aufgabe ist ausdrücklich, einen detaillierten Prompt für [Claude Code](Claude%20Code.md) beziehungsweise Claude zur Gesamtarchitektur zu erzeugen, als einen langen direkt kopierbaren Absatz. Als Beispiel konkretisiert das Bild [Agentic Engineering](../concepts/Agentic%20Engineering.md) durch Datenfelder, Zustände und Randfälle; Viralität, Bauzeit und Laufzeitverhalten wurden nicht gemessen. [tweet-2093396854822052158](../sources/tweet-2093396854822052158.md)
