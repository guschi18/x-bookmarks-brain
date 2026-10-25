---
tags: [agents, tools]
sources: [tweet-2099928503487517062.md]
created: 2026-10-08
updated: 2026-10-08
---

# My Brain Is Full Crew

## Projekt und Arbeitsweise (Stand 2026-09)

https://github.com/gnekt/My-Brain-Is-Full-Crew beschreibt eine über Chat bediente Obsidian-Crew mit acht Kernagenten und 14 Skills. Ein Dispatcher wählt reaktive Agenten oder mehrstufige Skills und kann nach einer Ausgabe mit Suggested next agent passende Folgearbeit anstoßen. Es ist ein eigenes Projekt neben [Obsidian Second Brain](Obsidian%20Second%20Brain.md) und [Claude Obsidian](Claude%20Obsidian.md), mit verwandtem Wissensablage-Ziel wie [LLM Wiki Pattern](../concepts/LLM%20Wiki%20Pattern.md). [tweet-2099928503487517062](../sources/tweet-2099928503487517062.md)

## Agenten und Skills (Stand 2026-09)

Die Rollen sind Architect für Einrichtung und Struktur, Scribe für Notizerfassung, Sorter für Inbox, Seeker für Suche mit Zitaten, Connector für Querverbindungen, Librarian für Wartung, Transcriber für Audio/Meetings und Postman für Mail/Kalender. Die Wirksamkeit dieser Rollen wird durch die README beschrieben, nicht durch unabhängige Ergebnisse belegt. [tweet-2099928503487517062](../sources/tweet-2099928503487517062.md)

Die 14 Skills heißen /onboarding, /create-agent, /manage-agent, /defrag, /email-triage, /meeting-prep, /weekly-agenda, /deadline-radar, /transcribe, /vault-audit, /deep-clean, /tag-garden, /inbox-triage und /contact-sync. Sie laufen laut README im Hauptgespräch und behalten den Kontext mehrstufiger Vorgänge. [tweet-2099928503487517062](../sources/tweet-2099928503487517062.md)

## Einrichtung und Pflege (Stand 2026-09)

Repository innerhalb des Vaults klonen, in My-Brain-Is-Full-Crew wechseln und bash scripts/launchme.sh ausführen. Als Plattformen sind [Claude Code](Claude%20Code.md), Gemini CLI, OpenCode und [Codex](Codex.md) vorgesehen; --platform claude-code, gemini-cli, opencode oder codex-cli wählt den Adapter explizit. Anschließend Initialize my vault anfordern. [tweet-2099928503487517062](../sources/tweet-2099928503487517062.md)

Das Onboarding legt ein hybrides PARA-/Zettelkasten-System an und bildet bestehende Ordner über Meta/vault-map.md ab, statt ihre Umbenennung zu verlangen. Die README nennt Inbox, Projects, Areas, Resources, Archive, People, Meetings, Daily, MOC und Templates als Standardrollen. [tweet-2099928503487517062](../sources/tweet-2099928503487517062.md)

Nach git pull aktualisiert bash scripts/updateme.sh die installierten Agenten und Skills; Plattformwahl geht ebenfalls über --platform. Laut README bleiben Vault-Notizen dabei unangetastet. Orchestra-Helfer sind im TODO noch als manueller Kopierschritt genannt. [tweet-2099928503487517062](../sources/tweet-2099928503487517062.md)

## Integrationen und Grenzen (Stand 2026-09)

Postman verwendet Google Workspace CLI für Gmail und Google Calendar oder Hey CLI für Hey.com; Calendar bleibt dabei bei gws. MCP ist als eingeschränkter Fallback mit Lesen und Entwürfen vorgesehen. Apple-Contacts-Sync ist optional und macOS-bezogen; andere Rollen arbeiten laut README nur am lokalen Vault. [tweet-2099928503487517062](../sources/tweet-2099928503487517062.md)

Für [Codex](Codex.md) beschreibt die Quelle getrennte .codex/agents und .agents/skills sowie AGENTS.md als Dispatcher. Ihre Windows-Empfehlung für WSL ist ein historischer README-Hinweis, keine hier geprüfte aktuelle Plattformgrenze. Die Quelle empfiehlt Vault-Backups und konservatives Archivieren statt Löschen; sämtliche Integrationen und Agenten wurden hier nicht installiert oder getestet. [tweet-2099928503487517062](../sources/tweet-2099928503487517062.md)
