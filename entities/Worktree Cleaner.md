---
tags: [tools, agents]
sources: [tweet-2113726955937730604.md]
created: 2026-10-25
updated: 2026-10-25
---

# Worktree Cleaner

## Überblick (Stand 2026-10)

Worktree Cleaner ist ein Skill aus der Sammlung claude-code-templates von Daniel San. Er soll Speicher freigeben, den alte Git-Worktrees (etwa einer je Claude-Code-Aufgabe) mit duplizierten node_modules belegen. Installation laut Post: `npx claude-code-templates@latest --skill git/worktree-cleaner`. [tweet-2113726955937730604](../sources/tweet-2113726955937730604.md)

## Ablauf und Regeln laut SKILL.md (Stand 2026-10)

- Ein Inventar-Skript (nur lesend, optional mit `git fetch --prune`) klassifiziert jeden Worktree mit Belegen: gemergt, PR-Status, uncommittete oder ungepushte Arbeit, gesperrt, veraltet, von laufender Sitzung genutzt. [tweet-2113726955937730604](../sources/tweet-2113726955937730604.md)
- Vor jedem zerstörerischen Befehl (`git worktree remove`, `prune`, `unlock`, `git branch -d/-D`) fragt der Skill nach; die Freigabe gilt nur für diesen Worktree oder diese Gruppe. [tweet-2113726955937730604](../sources/tweet-2113726955937730604.md)
- Nie `--force` bei Arbeit, die verloren ginge; nie den Haupt-Worktree, den eigenen Worktree oder einen mit laufenden Prozessen anfassen; nie Remote-Branches löschen. [tweet-2113726955937730604](../sources/tweet-2113726955937730604.md)
- Vor der Aktion wird der einzelne Worktree erneut geprüft, nach der Aktion das Ergebnis verifiziert; bei Fehlern stoppt der Skill, statt mit stärkeren Flags zu wiederholen. [tweet-2113726955937730604](../sources/tweet-2113726955937730604.md)

## Grenzen (Stand 2026-10)

Die Quelle belegt Beschreibung und Regeln, nicht eine Wirkung in Zahlen; der freigegebene Speicherplatz hängt vom Repository ab. Eine Ausführung wurde hier nicht getestet. [tweet-2113726955937730604](../sources/tweet-2113726955937730604.md)

## Verwandte Seiten

[Claude Code](Claude%20Code.md) erzeugt solche Worktrees bei parallelen Aufgaben. [tweet-2113726955937730604](../sources/tweet-2113726955937730604.md)
