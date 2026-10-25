---
tags: [agents, tools, product-building]
sources: [tweet-2098047780086329364.md]
created: 2026-10-09
updated: 2026-10-09
---

# Agent Orchestrator

## Workspace und Einrichtung (Stand 2026-09)

[Untrivial-ai/agent-orchestrator](https://github.com/Untrivial-ai/agent-orchestrator) beschreibt AO als lokalen Desktop-Workspace für mehrere Coding-Agenten. Die gespeicherte README nennt Downloads für macOS, Windows und Linux; nach Auswahl eines Repositories startet die Desktop-App den lokalen Daemon. Lizenz ist Apache 2.0. [tweet-2098047780086329364](../sources/tweet-2098047780086329364.md)

## Worker und Projektplanung (Stand 2026-09)

Ein Worker hält eine Aufgabe, einen Coding-Agenten und einen isolierten Workspace zusammen. Für Git-Arbeit erhält er eigenen Branch und Worktree; Aufgabe, Chat, Terminal, Diff, Browser, Pull Request, CI und Review bleiben der Sitzung zugeordnet. Standalone-Agenten können branchlose AO-Verzeichnisse nutzen. Unterstützte Agenten sind laut README unter anderem [Claude Code](Claude%20Code.md) und [Codex](Codex.md); die angegebenen 27 Integrationen wurden hier nicht getestet. [tweet-2098047780086329364](../sources/tweet-2098047780086329364.md)

Der persistente Projekt-Orchestrator hält Ziele, Entscheidungen, Randbedingungen und Planungshistorie. Er kann Aufgaben zerlegen, Worker starten oder umlenken und Kontext weitergeben; Worker führen Implementierung, Tests, Commits und PRs aus. Der Daemon beobachtet Agentenaktivität und Source-Control-Zustand, damit Planung auf laufender Arbeit beruht. [tweet-2098047780086329364](../sources/tweet-2098047780086329364.md)

## Kanban und Rückkopplung (Stand 2026-09)

Das Board leitet Working, Needs you, In review und Ready to merge aus Sitzung, PR, CI und Review ab. Fehlende Eingaben, fehlgeschlagene Checks oder Änderungswünsche sollen beim verantwortlichen Worker sichtbar werden und an ihn zurückgehen. Pro Worker isolierte Browserprofile und native Terminalinterfaces ergänzen die strukturierte Chatansicht. [tweet-2098047780086329364](../sources/tweet-2098047780086329364.md)

## Grenzen und Telemetrie (Stand 2026-09)

Ablauf, Isolation und Merge-Zustand sind Herstellerbeschreibung, keine hier durchgeführte Parallelitäts- oder Zuverlässigkeitsprüfung. Die README beschreibt Nutzungs-/Fehlermetriken ohne Projektinhalt, erfasst aber den GitHub-Ownernamen einer eingebundenen Organisation oder eines Kontos; bei persönlichen Repos ist dies ein Nutzername und daher laut README nicht anonym. [tweet-2098047780086329364](../sources/tweet-2098047780086329364.md)

[Codex Astra Luna Orchestrator](Codex%20Astra%20Luna%20Orchestrator.md) ist ein anderer Wiki-Eintrag zu einem anderen Repository. AO dokumentiert einen Desktop-/Daemon-Workspace mit Worktrees und Kanban, weshalb die Namensähnlichkeit keinen identischen Werkzeugbeleg bedeutet. [tweet-2098047780086329364](../sources/tweet-2098047780086329364.md)
