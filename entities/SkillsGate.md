---
tags: [tools, agents]
sources: [tweet-2097998818134376494.md]
created: 2026-10-09
updated: 2026-10-09
---

# SkillsGate

## Aufgabe (Stand 2026-09)

[skillsgate/skillsgate](https://github.com/skillsgate/skillsgate) beschreibt eine MIT-lizenzierte Desktop-App zum Finden, Installieren und Verwalten von Agent Skills. Der Katalog kommt aus skills.sh; Installation ist pro Agent oder für mehrere gleichzeitig möglich. Die Liste umfasst unter anderem [Claude Code](Claude%20Code.md), [Codex](Codex.md), Cursor, OpenCode und OpenClaw; die README nennt insgesamt 20+ Agenten. [tweet-2097998818134376494](../sources/tweet-2097998818134376494.md)

## Bedienung und Speicherung (Stand 2026-09)

Die gespeicherte Anleitung empfiehlt Desktop-Downloads für macOS, Windows und Linux. Ein Editor zeigt gerenderten Skill-Text oder bearbeitet die Quelldatei direkt; Einstellungen, Favoriten und Remote-Server-Konfiguration liegen lokal in SQLite. SSH-Zugriff soll Skills anderer Maschinen durchsuchen und synchronisieren, private Skills können lokal bleiben oder im Team geteilt werden. Ein Konto ist laut README nicht erforderlich. [tweet-2097998818134376494](../sources/tweet-2097998818134376494.md)

## Versionswechsel (Stand 2026-09)

Die README erklärt skillsgate und @skillsgate/tui auf npm für deprecated und nicht weiter gepflegt. `npx skillsgate` startet nur die letzte veröffentlichte TUI; für öffentliche CLI-Installationen wird `npx skills add` genannt. Die TUI-Erwähnung im Screenshot bildet daher einen anderen Stand ab als die gespeicherte Bedienanleitung. [tweet-2097998818134376494](../sources/tweet-2097998818134376494.md)

Für macOS 0.7.0 und älter beschreibt die README einen manuellen Wechsel auf 0.7.2: passenden arm64-/Intel-DMG herunterladen und in Applications ziehen. Erst spätere Updates sollen wieder normal funktionieren; Einstellungen und installierte Skills bleiben laut Anbieter erhalten. Dieser Versionshinweis ist ein gespeicherter Stand, keine aktuelle Upgradeempfehlung. [tweet-2097998818134376494](../sources/tweet-2097998818134376494.md)

## Grenzen (Stand 2026-09)

Agentenkompatibilität, SSH-Synchronisierung und Erhalt vorhandener Skills wurden hier nicht praktisch geprüft. Das Werkzeug verwaltet lokale Skill-Dateien; der README-Umfang ist kein Wirksamkeitsnachweis der installierten Skills. [tweet-2097998818134376494](../sources/tweet-2097998818134376494.md)
