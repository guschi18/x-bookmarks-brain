---
tags: [agents, tools]
sources: [tweet-2058093406874689770.md]
created: 2026-10-01
updated: 2026-10-08
---

# Cmux

## Produkt und Arbeitsweise (Stand 2026-05)

[cmux](https://github.com/manaflow-ai/cmux) ist laut README ein natives macOS-Terminal in Swift/AppKit mit libghostty als Renderbibliothek. Es bietet vertikale Tabs, Splits, Agentenbenachrichtigungen und einen eingebauten Browser; es ist kein Ghostty-Fork. [tweet-2058093406874689770](../sources/tweet-2058093406874689770.md)

Steinberger beschreibt [Codex](Codex.md) in der Mac-App für Wissen, Lernen und Lesen sowie cmux mit Codex CLI fürs Programmieren. Das ist seine Arbeitsaufteilung, kein Vergleichstest. [tweet-2058093406874689770](../sources/tweet-2058093406874689770.md)

## Kontrolle und Aufmerksamkeit (Stand 2026-05)

Die README nennt Workspace-Metadaten wie Git-Branch, PR, Verzeichnis und Ports sowie blaue Benachrichtigungsringe, OSC 9/99/777 und cmux notify. CLI und Unix-Socket steuern Workspaces, Eingaben und Browseraktionen; SSH-Workspaces und [Claude Code](Claude%20Code.md)-Teammate-Panes sind dokumentiert. [tweet-2058093406874689770](../sources/tweet-2058093406874689770.md)

## Wiederherstellung und Grenzen (Stand 2026-05)

Gespeichert werden Layout, Verzeichnisse, bestmöglicher Scrollback und Browserzustand. Unterstützte Agenten können mit gespeicherten Session-IDs fortgesetzt werden; beliebige laufende Prozesse werden nicht eingefroren. cmux local-tmux erlaubt lokales Detach/Reattach, überlebt jedoch keinen Logout, Rechnerneustart oder Stromverlust. [tweet-2058093406874689770](../sources/tweet-2058093406874689770.md)

Laut README ist die Desktop-App derzeit macOS-exklusiv; iOS-Zugang ist Beta (Stand 2026-10-08 bestätigt). Die Quelle nennt GPL-3.0-or-later und begrenzte kommerzielle Rechte nur für kontrollierte Bestandteile. Funktions- und Performanceangaben sind Projektbeschreibungen, keine hier getestete Integration. [tweet-2058093406874689770](../sources/tweet-2058093406874689770.md)
