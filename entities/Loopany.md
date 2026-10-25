---
tags: [agents, tools]
sources: [tweet-2076626834561925183.md]
created: 2026-10-01
updated: 2026-10-01
---

# Loopany

## Rolle und Architektur (Stand 2026-07)

[Loopany](https://github.com/superdesigndev/loopany-platform) verwaltet laut gespeicherter README wiederkehrende Agentenarbeit: Ein Server plant Läufe, speichert gewählte Artefakte, authentifiziert und benachrichtigt; @crewlet/loopany auf der eigenen Maschine führt den lokalen Coding-Agenten aus. Der Server soll weder LLMs noch Nutzercode ausführen. [tweet-2076626834561925183](../sources/tweet-2076626834561925183.md)

## Wiederkehrender Betrieb (Stand 2026-07)

Das Projekt unterscheidet offene Monitore von geschlossenen Zielen und nennt Cron/Einmalläufe, deterministische Vorstufen, gemeinsames Dashboard, Teamkanäle und periodische Evolve-Läufe. Evolve prüft vergangene Ergebnisse und Kosten und verändert Vertrag, Zustand, Trigger oder mechanische Skriptschritte; das ist die dokumentierte Umsetzung von [Loop Engineering](../concepts/Loop%20Engineering.md). [tweet-2076626834561925183](../sources/tweet-2076626834561925183.md)

Der daemon pollt den Server, beansprucht einen wartenden Lauf, startet den eigenen Agenten und meldet Ergebnisse zurück. Die CLI nennt up, status, down, log, new und edit; Templates sollen den ersten Loop samt Vertrag und Verlauf anlegen. [tweet-2076626834561925183](../sources/tweet-2076626834561925183.md)

## Voraussetzungen und Grenzen (Stand 2026-07)

Die README nennt Node.js ≥22, pnpm 8.15 und MIT für Server und Daemon. Lokal verwendet pnpm dev eingebettetes PGlite; für Produktion werden Authentifizierung, persistente Datenbank und Objektspeicher benötigt. Ohne Auth-Variablen ist der Server offen, ohne Objektspeicher liegen Artefakte nur im Arbeitsspeicher. [tweet-2076626834561925183](../sources/tweet-2076626834561925183.md)

Nur ein Serverprozess soll den In-Process-Scheduler betreiben, um doppelte Auslösungen zu vermeiden; PGlite-Dateien sollen nur bei gestopptem Server kopiert werden. Die README bezeichnet das Projekt als früh und den Daemon als hoch privilegiert. Der Eigenbericht über Superdesign ersetzt weder Sicherheitsprüfung noch unabhängige Leistungsmessung; [Verifier Setup](Verifier%20Setup.md) liefert die ergänzende Prüfinfrastruktur. [tweet-2076626834561925183](../sources/tweet-2076626834561925183.md)
