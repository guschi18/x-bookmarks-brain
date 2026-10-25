---
tags: [agents, tools]
sources: [tweet-2104679128020754457.md]
created: 2026-10-06
updated: 2026-10-06
---

# Claude Projects

## Arbeitsmodell im Leitfaden (Stand 2026-09)

Der gespeicherte Leitfaden beschreibt ein Project als fortlaufende Coordinator-Konversation, die Arbeit in eigenständige parallele Threads zerlegt, ihnen Briefings schreibt und Ergebnisse verfolgt. Der Nutzer gibt idealerweise eine vollständige Aufgabe pro Thread; das ist die beschriebene Oberfläche, kein hier ausgeführter Produkttest. [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)

## Kontext und Instructions (Stand 2026-09)

Beim Anlegen Name und Goal setzen sowie kuratierte Repositories, Dateien, Ordner oder Drive-Kontext hinzufügen. Der Autor empfiehlt ein bis zwei häufig genutzte Repositories statt großer ungefilterter Sammlungen; andere Repositories sollen die Instructions auffindbar machen. Bei Verbindungsfehlern nennt er erneute GitHub-Verknüpfung und passende App-Berechtigungen. [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)

Project Instructions sollen Kontext, Quellen, Source of Truth, Beziehungen, Invarianten und den Einstieg in die richtige Quelle erklären, bestehende Repo-CLAUDE.md aber nicht wiederholen. Auto Memory mit MEMORY.md und ergänzenden Dateien regelmäßig auf veraltete Projektstände prüfen. [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)

## Modell und Effort (Stand 2026-09)

Post und Screenshot empfehlen [Claude Opus 5.5](Claude%20Opus%205.5.md) als Coordinator und Sonnet 5.5 als Threadmodell; im Screenshot ist Coordinator-Effort Medium sichtbar. Der Artikel beschreibt zugleich eigene Nutzung von Opus 5.5 für beide Rollen mit medium sowie Opus 5.5 und Sonnet 5 für einfachere Projekte. Diese gespeicherten Empfehlungen unterscheiden sich und sind kein universelles Optimum. [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)

Usage nach Thread, Modell, Coordinatoranteil und Cache prüfen und Modell/Effort an die eigene Aufgabenkomplexität anpassen. Der Autor empfiehlt Auto-continue when usage limits reset; Verfügbarkeit und Auswirkungen wurden hier nicht unabhängig geprüft. Siehe [Model Selection Evals](../concepts/Model%20Selection%20Evals.md). [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)

## Cloud-Environment und Zugänge (Stand 2026-09)

Laut Artikel klont jeder Cloudthread die hinzugefügten Repositories frisch vom Defaultbranch und beginnt eigene Branches. Environment umfasst Netzwerkfreigaben, Konfiguration, Credentials und Startskript; der Autor empfiehlt Trusted beziehungsweise gezielte Custom-Domains. [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)

Environment Variables sind im Leitfaden lesbare Konfigurationswerte, API Credentials dagegen nach Zielhosts begrenzte Secrets, die ein Proxy erst nach Verlassen der Session an Requests hängt. Das ist eine Beschreibung des Artikels, keine hier geprüfte Isolation oder aktuelle Planverfügbarkeit. [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)

Der Artikel beschreibt gecachte Setup-Dateien bei einem Startskript unter fünf Minuten, aber keine fortlaufenden Prozesse im Cache; Datenbanken müssten pro Session starten. Connectors sollen vorab verbunden sein und stehen laut Quelle Threads, nicht der Coordinator-Konversation selbst, zur Verfügung. [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)

## Plugins, Threads und Ergebnisablage (Stand 2026-09)

Benötigte Cloud-Plugins über Project Plugins hinzufügen; repositorylokale .claude/settings.json-Plugins sollen laut Artikel dort nicht laden. Threads und zugehörige PRs erscheinen im Overview mit Working, Waiting on you, Ready for review, Landing, Idle und Resolved. Der Autor empfiehlt einen Thread pro PR. [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)

Library enthält Kontext sowie produzierte Dateien; Routines starten geplante Arbeit als Threads. Limits, Interface-Details, Cachezeitraum und Connectorverhalten sind der gespeicherte Artikelstand, keine unabhängig verifizierten Produktgarantien. Verwandt: [Claude Code](Claude%20Code.md). [tweet-2104679128020754457](../sources/tweet-2104679128020754457.md)
