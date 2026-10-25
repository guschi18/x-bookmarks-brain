---
tags: [tools, agents]
sources: [tweet-2112528257924964751.md]
created: 2026-10-23
updated: 2026-10-23
---

# Harp

## Überblick (Stand 2026-10)

Harp (dominikmartn/harp) ist ein inoffizieller Fork des Open-Source-Terminals [Warp](Warp.md). Er ersetzt die Tab-Leiste durch eine Sidebar für lang laufende Coding-Agents und lässt den Rest von Warp unverändert. Dom kündigt ihn als Open-Source-Version seines Redesigns an; der Vorgänger-Post nannte die Neugestaltung seines Terminals nach der Warp-Öffnung. [tweet-2112528257924964751](../sources/tweet-2112528257924964751.md)

## Funktionen laut README

- Agent-Status je Zeile: arbeitet, wartet oder fertig für [Claude Code](Claude%20Code.md)- und Codex-Sessions, mit Ungelesen-Markierung. [tweet-2112528257924964751](../sources/tweet-2112528257924964751.md)
- Benannte Tab-Gruppen; mit tmux-Integration liegen Gruppe und Reihenfolge in den tmux-Sessions und überleben einen Neustart. [tweet-2112528257924964751](../sources/tweet-2112528257924964751.md)
- Limit-Ringe für das 5-Stunden-Fenster und das Wochenlimit je Anbieter; Codex-Werte kommen aus den Session-Logs, Claude-Werte aus der Statuszeile von Claude Code. Harp ruft nichts ab und liest keine Zugangsdaten. [tweet-2112528257924964751](../sources/tweet-2112528257924964751.md)
- tmux-Sessions vom Handy per SSH lassen sich mit tmux set-option @warp_adopt 1 als Tab übernehmen. [tweet-2112528257924964751](../sources/tweet-2112528257924964751.md)

## Installation und Lizenz

DMG aus den GitHub-Releases (macOS, eigene Bundle-ID und Settings-Ordner ~/.harp), Update-Prüfung alle 10 Minuten mit Signaturprüfung. Einstellungen in ~/.harp/settings.toml; tmux-Sync ist standardmäßig aus. Lizenz: GNU AGPL v3, die Crates warpui und warpui_core unter MIT. [tweet-2112528257924964751](../sources/tweet-2112528257924964751.md)

## Evidenzgrenze

Alle Angaben stammen aus der README. Die übrigen Warp-Funktionen (KI, Cloud, Login) laufen weiter über Warps Server; Login über Harp ist laut README ungetestet. Harp ist nicht von Warp unterstützt. [tweet-2112528257924964751](../sources/tweet-2112528257924964751.md)
