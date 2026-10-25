---
tags: [agents, tools, product-building]
sources: [tweet-2093335809097109630.md]
created: 2026-10-10
updated: 2026-10-10
---

# SnagTime

## Historischer Build-Bericht (Stand 2026-08)

Der Autor berichtet, mit [Codex](Codex.md) eine Calendly-ähnliche Anwendung namens SnagTime gebaut zu haben: Verfügbarkeit, Buchungslinks, Rollen, Branding, Google Calendar und Stripe-Sandbox-Zahlungen. Ein großer /goal-Auftrag gliedert Recherche, Planung, Bau und wiederholte Tests; später folgen Rebranding, Performance- und UX-Korrekturen. [tweet-2093335809097109630](../sources/tweet-2093335809097109630.md)

Er nennt fünf Tage und fünf Stunden aktive Laufzeit, 334 aggregierte Agentenstunden, 76 einzigartige Subagenten, 32.103.178.736 Input- und 47.364.103 Output-Tokens. Die 14.982,96 Dollar sind sein geschätzter Inferenzgegenwert, keine gezahlte API-Rechnung; er nennt ein ausgeschöpftes 200-Dollar-Abo und rund 150 Dollar Zusatzcredits. Diese Einzelfallzahlen sind nicht unabhängig geprüft und keine allgemeinen Abo-Werte. [tweet-2093335809097109630](../sources/tweet-2093335809097109630.md)

## Menschliche Prüfung und Folgekosten

Testagenten fanden technische Fehler, aber übersahen eine Buchungs-Fortschrittsleiste, deren frühere Schritte trotz passendem Aussehen nicht anklickbar waren. Der Autor korrigierte das nach eigener Nutzung. Selbsthosting ersetzt die Softwaregebühr durch Integrations-, Wartungs-, Support- und Hostingverantwortung; die Fallstudie ergänzt [Agentic Engineering](../concepts/Agentic%20Engineering.md) um ein konkretes UX- und Kostenbeispiel. [tweet-2093335809097109630](../sources/tweet-2093335809097109630.md)

## Repository-Nachtrag des Nutzers (Stand 2026-10-10)

Der Nutzer ergänzte am 10.10.2026 [nateherkai/snagtime](https://github.com/nateherkai/snagtime). Die dazu gelesene aktuelle README ist als eigener Nachtrag unter output/snagtime-readme-2026-10-10.md gespeichert und gehört nicht zum unveränderten Raw-Post. Sie nennt MIT, Node ab 20.9 (24 getestet), `npm run setup` und `npm run demo:free` für eine lokale SQLite-Demo mit lokalem Kalender, Test-Inbox und Stub-Zahlungen ohne Google-/Stripe-Zugangsdaten. [tweet-2093335809097109630](../sources/tweet-2093335809097109630.md)

Die [aktuelle README](https://github.com/nateherkai/snagtime#put-it-on-the-internet) präzisiert gegenüber dem historischen Video: Öffentlicher Betrieb benötigt einen dauerhaften Node-Webdienst, Background-Worker und PostgreSQL; Vercel wird nicht direkt unterstützt. [Stripe-Live-Schlüssel werden bewusst abgewiesen](https://github.com/nateherkai/snagtime#what-is-actually-free), deshalb ist der Videohinweis auf bloßen Wechsel zu Produktionsschlüsseln keine aktuelle Betriebsanleitung. [tweet-2093335809097109630](../sources/tweet-2093335809097109630.md)

Die Software wurde weder installiert noch auf Zahlungs-, Kalender- oder Produktionssicherheit geprüft. Kostenfreiheit betrifft den Quellcode und mögliche lokale Nutzung, nicht garantiert öffentliche Infrastruktur oder Drittanbieter. [tweet-2093335809097109630](../sources/tweet-2093335809097109630.md)
