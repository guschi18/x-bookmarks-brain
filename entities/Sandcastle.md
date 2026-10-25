---
tags: [agents, tools, product-building]
sources: [tweet-2049506712801935611.md, tweet-2067721938894500036.md]
created: 2026-10-16
updated: 2026-10-20
---

# Sandcastle

## Zweck und Primitive (Stand 2026-04)

Matt Pocock stellt Sandcastle als TypeScript-Bibliothek zur Orchestrierung von Coding-Agenten in isolierten Sandboxes vor. Die zentrale Operation `sandcastle.run` verbindet Agent, Sandbox und Prompt; die aufrufende Anwendung definiert die Reihenfolge und Parallelität. [Claude Code](Claude%20Code.md) und [Codex](Codex.md) sind im Tutorial austauschbare Agentenrollen. [tweet-2049506712801935611](../sources/tweet-2049506712801935611.md)

Die Sandbox soll unbeaufsichtigte Arbeit ermöglichen, ohne pauschal Berechtigungsabfragen auf dem Host zu umgehen. Dies ist das erklärte Designziel; Schutz vor Datenabfluss oder destruktiven Aktionen wurde hier nicht geprüft. [tweet-2049506712801935611](../sources/tweet-2049506712801935611.md)

## Einrichtung im Tutorial (Stand 2026-04)

Nach Paketinstallation startet der Autor `npx sandcastle init`, wählt Agent, Docker als Sandbox und GitHub-Issues als Backlog. Ein Template erzeugt den `.sandcastle`-Ordner mit Einstiegsskript, Dockerfile, Prompt-Dateien und einer Beispiel-Umgebung. Im Dockerfile werden Systemwerkzeuge, GitHub CLI und der gewählte Agent eingerichtet. [tweet-2049506712801935611](../sources/tweet-2049506712801935611.md)

Die gezeigte Umgebung benötigt einen Anthropic-API-Key und GitHub-Token. Für die Verwendung eines Claude-Abonnements verweist Pocock auf gesonderte aktuelle Hinweise; das Video liefert keine pauschale Erlaubnis oder dauerhafte Kompatibilitätszusage. Das GitHub-Label `sandcastle` begrenzt, welche Issues der Workflow bearbeitet. [tweet-2049506712801935611](../sources/tweet-2049506712801935611.md)

## Planner, Implementer, Reviewer und Merger (Stand 2026-04)

Der Planner liest gelabelte Issues, Kommentare und Blockaden und liefert eine maschinenlesbare Aufgabenliste. Für jede ausführbare Aufgabe startet ein Implementer in einer eigenen Sandbox und auf einem eigenen Branch. Prompts und Projektstandards sind editierbare Dateien des aufrufenden Projekts. [tweet-2049506712801935611](../sources/tweet-2049506712801935611.md)

Nach erzeugten Commits prüft ein separater Reviewer den Diff auf Korrektheit und Verbesserungen. Der Autor beschreibt auch einen Modellwechsel für adversariale Reviews oder mehrere konkurrierende Implementierungen; dies sind konfigurierbare Abläufe, keine verpflichtende interne Sandcastle-Pipeline. [tweet-2049506712801935611](../sources/tweet-2049506712801935611.md)

Ein Merger-Agent führt die Ergebnisse zusammen und bearbeitet mögliche Konflikte. Im gezeigten Einzelfall laufen Typechecks, Merge und Issue-Abschluss erfolgreich; alternativ könne man PR-Branches erzeugen. Daraus folgt keine allgemeine Zuverlässigkeits- oder Geschwindigkeitsmessung. [tweet-2049506712801935611](../sources/tweet-2049506712801935611.md)

## Beleggrenzen (Stand 2026-04)

Das vollständige 684,8-Sekunden-Transkript erläutert den Aufbau, enthält aber erkennbare Erkennungsfehler bei Paketnamen, Produktnamen und Dateiendungen. Es fehlt eine separat gespeicherte Repository-README; insbesondere die transkribierte npm-Installationszeile ist nicht als geprüfter Kopierbefehl übernommen. Agenten und Docker wurden hier nicht gestartet. [tweet-2049506712801935611](../sources/tweet-2049506712801935611.md)

[Agentic Engineering](../concepts/Agentic%20Engineering.md) ordnet den Ablauf als Trennung von Planung, Ausführung und Kontrolle ein. Das Originaltutorial ergänzt den bereits separat dokumentierten späteren Issue-/PR-Beleg um Einrichtung und Rollenablauf. [tweet-2049506712801935611](../sources/tweet-2049506712801935611.md)

## Späteres Issue-/PR-Beispiel (Stand 2026-06)

Matt Pocock nennt GitHub Actions, Sandcastle und [Claude Code](Claude%20Code.md) als seinen damaligen Stack: Ein Issue-Label soll eine Implementierung auslösen. Der gespeicherte Pull Request #1048 des Course Video Manager dokumentiert Änderungen an Slug-Eindeutigkeit, einem virtuellen Dateisystem, Agentenwerkzeugen und Tests. Dieser separate Beleg ergänzt das April-Tutorial um ein konkretes PR-Beispiel, belegt aber keine allgemeine Erfolgsquote oder Zuverlässigkeit des Stacks. [tweet-2067721938894500036](../sources/tweet-2067721938894500036.md)
