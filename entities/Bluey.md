---
tags: [agents, tools]
sources: [tweet-2106168904208785614.md]
created: 2026-10-12
updated: 2026-10-12
---

# Bluey

## Rolle und Bedienung (Stand 2026-10)

[rbrown101010/bluey-by-riley](https://github.com/rbrown101010/bluey-by-riley) beschreibt Bluey, auch Googly Eyes genannt, als Blaubeerfigur auf einem iPhone unter dem Mac-Bildschirm. Die Figur zeigt mit einem eigenen Cursor auf Inhalte; ein Doppeltipp oder ⌥Space startet eine Sitzung, Gedrückthalten auf dem Telefon stellt eine Frage, Loslassen fordert die Antwort an. Antworten erscheinen als Sprechblase mit einem kurzen Ton. [tweet-2106168904208785614](../sources/tweet-2106168904208785614.md)

## Verbindung und Meeting-Notizen (Stand 2026-10)

Laut README nutzt das Telefon eine OpenAI-Realtime-WebSocket-Sitzung mit Textausgabe; der Mac erzeugt ein zehn Minuten gültiges Client-Secret. Bildschirmabfragen verwenden ScreenCaptureKit und Vision und liefern Screenshot, Text-IDs und Mausposition. point_at und point_at_spot steuern den Zeiger. Die Geräte finden sich im selben WLAN über Bonjour. [tweet-2106168904208785614](../sources/tweet-2106168904208785614.md)

Während einer Sitzung zeichnet das Telefon fünfminütige AAC-Blöcke auf; der Mac transkribiert mit Sprecherkennzeichnung und speichert notes.md, session.json und audio unter ~/Documents/Bluey Notes. Ein kopierbarer Agenten-Prompt verweist auf diese Dateien. Der README nennt automatisches Wiederverbinden, ohne hier geprüfte Dauerlaufstabilität. [tweet-2106168904208785614](../sources/tweet-2106168904208785614.md)

## Computeraktionen und Einrichtung (Stand 2026-10)

Optional darf Bluey klicken, tippen, Tastenkürzel senden, scrollen, ziehen sowie Apps und URLs öffnen. Dafür verlangt der Mac Accessibility-Rechte; Let Him Use the Computer schaltet die Aktionen ab, ⌃⌥S stoppt sie. Der README beschreibt Handeln nur auf Anfrage, Ablehnen von Passwortfeldern und Behandlung sichtbaren Texts als Daten statt Anweisungen; diese Schutzmaßnahmen wurden nicht getestet. [tweet-2106168904208785614](../sources/tweet-2106168904208785614.md)

Die Mac-App wird mit ./scripts/build-mac.sh gebaut; die iPhone-App erfordert Xcode und Signing. Der API-Schlüssel liegt laut README lokal in ~/Library/Application Support/Googly/keys.json; Lizenz ist Unlicense. Der Text bezeichnet den aktuellen Modus als ohne Sprachausgabe, nennt bei irreversiblen Aktionen zugleich eine Bestätigung „out loud“; dieser Widerspruch bleibt offen. [tweet-2106168904208785614](../sources/tweet-2106168904208785614.md)
