---
tags: [agents, tools, product-building]
sources: [tweet-2093711487114043425.md]
created: 2026-10-09
updated: 2026-10-09
---

# SwarmForge

## Rolle (Stand 2026-08)

[unclebob/swarm-forge](https://github.com/unclebob/swarm-forge) koordiniert laut gespeicherter README Coding-Agenten in isolierten Git-Worktrees und tmux-Sitzungen. Ein lokales Dashboard dient zum Starten, Beobachten und Stoppen von Arbeit sowie zur Bearbeitung von Freigaben und Rückfragen. Agenten übergeben committierte Arbeit durch persistente Handoffs. [tweet-2093711487114043425](../sources/tweet-2093711487114043425.md)

## Installation und Rollen (Stand 2026-08)

Voraussetzungen: zsh, git, tmux, Babashka und mindestens ein konfiguriertes Backend aus grok, codex, claude oder copilot. Der Helfer `get-swarm-forge` komponiert Laufzeit/Regeln aus main und Konfiguration/Rollen aus einem Produktbranch; main allein ist laut README kein ausführbares Produkt. [tweet-2093711487114043425](../sources/tweet-2093711487114043425.md)

Pakete werden in ein bestehendes Projekt installiert: `get-swarm-forge two-pack` für coder → cleaner; four-pack für specifier → coder → refactorer → architect; six-pack trennt zusätzlich Hardening und QA. Anschließend startet `./swarm` die Projektrollen. Die forge-Produkte project-manager und lieutenant werden dagegen in einem leeren Hostverzeichnis installiert und verwalten Projekte darunter. [tweet-2093711487114043425](../sources/tweet-2093711487114043425.md)

## Übergaben und Zustandsgrenzen (Stand 2026-08)

`swarmforge/swarmforge.conf` legt Rollen, Backends, Worktrees, Empfangsmodus und Rückpropagation fest. Genau eine Rolle nutzt den Sentinel master, der den aktuellen Hauptcheckout meint und keinen Branch mit diesem Namen verlangt. Weitere Worktrees entstehen unter .worktrees/; Transport-/Prozesszustand liegt unter .swarmforge/. [tweet-2093711487114043425](../sources/tweet-2093711487114043425.md)

Die Helfer swarm_handoff.sh, ready_for_next.sh und done_with_current.sh senden, akzeptieren/mergen und schließen Arbeitsobjekte. Der [Handoff-Vertrag](https://github.com/unclebob/swarm-forge/blob/main/swarmforge/handoff-protocol.md) beschreibt Zustellung, Audit, Retry und Lifecycle. Agenten sollen generierten Zustand nicht anstelle dieser Helfer editieren. [tweet-2093711487114043425](../sources/tweet-2093711487114043425.md)

## Einordnung und Grenze (Stand 2026-08)

Unterstützte Backends umfassen [Claude Code](Claude%20Code.md) und [Codex](Codex.md). [Agent Orchestrator](Agent%20Orchestrator.md) dokumentiert einen anderen Desktop-/Daemon-Workspace; SwarmForge ist ein separates Repository mit komponierten Rollenpaketen und Shell-/tmux-Laufzeit. Die Installation und Übergabesicherheit wurden hier nicht praktisch getestet. [tweet-2093711487114043425](../sources/tweet-2093711487114043425.md)
