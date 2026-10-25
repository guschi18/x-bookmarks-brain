---
tags: [tools]
sources: [tweet-2100090476976095331.md]
created: 2026-10-08
updated: 2026-10-10
---

# Omarchy iPhone Controller

## Rolle und Bedienung (Stand 2026-09)

Daniel Lemky zeigt ein Omarchy-Plugin, um das iPhone vom Schreibtisch aus mit Maus und Tastatur des Computers zu bedienen. Super+Shift+I schaltet die Kontrolle um. [tweet-2100090476976095331](../sources/tweet-2100090476976095331.md)

Das beim Ingest betrachtete Originalbild bezeichnet das Werkzeug als iPhone Controller für Bluetooth Mouse and Keyboard. Es zeigt Status für Maus und Tastatur sowie Return control to computer, Restart controller und Stop controller. [tweet-2100090476976095331](../sources/tweet-2100090476976095331.md)

## Rückkehr und Voraussetzung (Stand 2026-09)

Das Originalbild nennt Super+Shift+Escape als Notausstieg. Eingebaute Tastatur und Trackpad bleiben laut Bild lokal; AssistiveTouch muss eingeschaltet bleiben. Diese Details stammen aus dem Bild, nicht aus dem leeren Videotranskript. [tweet-2100090476976095331](../sources/tweet-2100090476976095331.md)

## Verwandtes Repository: omarchy-iphone-mirror (Stand 2026-10)

Daniel Lemky veröffentlicht [omarchy-iphone-mirror](https://github.com/DanielLemky/omarchy-iphone-mirror). Das ist ein eigenes Projekt neben dem Bluetooth-Controller: Es spiegelt das iPhone auf Omarchy und leitet Eingaben weiter. Die Zuordnung zum Controller-Post stammt aus der Repo-Seite, nicht aus dem gespeicherten Tweet. (Quelle: GitHub-README, abgerufen 2026-10-10, kein Tweet-Anker)

- **Status:** Early Alpha. Getestet nur auf ARM64-Omarchy mit iPhone 13 unter iOS 27; Intel ungeprüft. Anbieterangabe.
- **Technik:** MPV dekodiert den HEVC-Videostrom des iPhones. Taps, Drags, Scrollen und Tastatur laufen über CoreDevice-Dienste mit pymobiledevice3, per USB oder WLAN. Weder Bluetooth-HID noch AssistiveTouch sind nötig.
- **Voraussetzungen:** Hyprland, systemd-User-Session, Python 3.14, MPV, usbmuxd, iproute2, wl-clipboard; vertrauenswürdiges iPhone mit Developer Mode und Developer Image.
- **Installation:** als normaler Nutzer (ohne `sudo`) per `install-online.sh --release v0.1.4` oder `./install.sh`; danach `./setup-phone.sh`. Optionales Omarchy-Bar-Plugin.
- **Bedienung:** `iphone-mirror start | stop | restart | status | reload-ui`; Ctrl+V sendet Klartext aus der Zwischenablage; Super+W schließt den Spiegel; Home und Spotlight als Toolbar-Buttons. Läuft der Bluetooth-Controller, soll er im Computer-Modus bleiben.
- **Lizenz:** eigener Code MIT; die Abhängigkeit pymobiledevice3 steht unter GPL-3.0-or-later, die README erhebt keinen Anspruch auf MIT-only für das Gesamtpaket.
- **Aktivität (Seitenstand):** 113 Sterne, 7 Forks, 5 offene Issues, 2 offene Pull Requests.

## Evidenzgrenze

Der gespeicherte Post enthält keine Repository-URL oder Installationsanleitung. Das Repository oben wurde nachträglich vom Nutzer genannt und nur anhand der README zusammengefasst; Bedienung und Kompatibilität wurden nicht getestet. Aus dem gezeigten Plugin folgt keine Windows-Unterstützung. [tweet-2100090476976095331](../sources/tweet-2100090476976095331.md)
