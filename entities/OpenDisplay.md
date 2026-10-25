---
tags: [tools]
sources: [tweet-2098809741279445342.md]
created: 2026-10-08
updated: 2026-10-08
---

# OpenDisplay

## Display und Transport (Stand 2026-09)

[Repository](https://github.com/peetzweg/opendisplay): Mac-Sender und iPhone-/iPad-Empfänger erzeugen einen echten erweiterten Bildschirm statt alleiniger Spiegelung; ein zweiter Mac kann ebenfalls Empfänger sein. [tweet-2098809741279445342](../sources/tweet-2098809741279445342.md)

CGVirtualDisplay erzeugt den virtuellen Monitor, ScreenCaptureKit erfasst ihn, VideoToolbox kodiert H.264 und eine direkte TCP-Verbindung über USB/usbmuxd oder WLAN transportiert die Frames. Touch und Scroll werden als Eingabe zurückgesendet. [tweet-2098809741279445342](../sources/tweet-2098809741279445342.md)

## Installation und Berechtigungen (Stand 2026-09)

Die README nennt signierte Mac-Downloads, iOS-TestFlight beziehungsweise Xcode-Build. Screen Recording wird für Erfassung, Accessibility für Eingabe und Local Network auf beiden Geräten für WLAN benötigt; ein Datenkabel genügt für USB. [tweet-2098809741279445342](../sources/tweet-2098809741279445342.md)

Der gespeicherte Stand nennt macOS 14 für den Sender und macOS 12 für einen Mac-Empfänger. iOS-Mindestangaben widersprechen sich zwischen 16.4+ und 16+ einschließlich 16.7.x; die konkrete Release-Kompatibilität ist vor Nutzung zu prüfen. [tweet-2098809741279445342](../sources/tweet-2098809741279445342.md)

## Grenzen (Stand 2026-09)

CGVirtualDisplay ist eine private API und kann nach macOS-Updates brechen. WLAN-Verschlüsselung mit Pairing und Audio sind im gespeicherten Text Roadmap; die README enthält zugleich Aussagen über automatische Updates und noch inaktive Signierschlüssel. Diese widersprüchlichen Statusangaben sind keine Betriebszusage. [tweet-2098809741279445342](../sources/tweet-2098809741279445342.md)

Der Lizenzabschnitt nennt GPL-3.0 und zuvor MIT-lizenzierte Releases bis v0.4.x. Die Funktion wurde hier nicht auf realer Apple-Hardware geprüft. [tweet-2098809741279445342](../sources/tweet-2098809741279445342.md)
