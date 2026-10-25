---
tags: [agents, tools]
sources: [tweet-2053441168189612337.md]
created: 2026-10-13
updated: 2026-10-13
---

# Riley Todo Skill

## Workflow im Video (Stand 2026-05)

Das gespeicherte Video beschreibt `/todo` für [Codex](Codex.md) und [Claude Code](Claude%20Code.md): Aufgaben aus mehreren Agenten-Chats landen in einer angepinnten Liste mit Links zu erzeugten Dokumenten und zur jeweiligen Sitzung. Als Beispiel wird Interviewrecherche anhand eines Kalendereintrags mit einem Google Doc gezeigt. [tweet-2053441168189612337](../sources/tweet-2053441168189612337.md)

Der Sprecher richtet zusätzlich eine Automation ein, die zweimal täglich die Liste untersucht, passende Arbeit fortführt und Ergebnisse im Chat zusammenfasst. Der Zeitplan ist eine separat gezeigte Einrichtung; das Transkript enthält keine vollständige Skill-Datei. [tweet-2053441168189612337](../sources/tweet-2053441168189612337.md)

## Originaldatei und Einrichtung (Online-Nachtrag 2026-10-13)

Auf Nutzerwunsch geprüft: [rbrown101010/rileys-skills/todo](https://github.com/rbrown101010/rileys-skills/tree/b4cc41e4414b6f27b768ad2d78e9d7b837f65227/todo), Commit `b4cc41e4414b6f27b768ad2d78e9d7b837f65227` vom 2026-05-10. Die Originaldatei enthält feste Mac-Pfade für eine gemeinsame Markdown-Liste, Redirect-Seiten und einen LaunchAgent. Aufgaben werden nach offen, erledigt und später sortiert; Artefaktlinks stehen am jeweiligen Eintrag. [tweet-2053441168189612337](../sources/tweet-2053441168189612337.md)

Für unsere Einrichtung den Ordner `todo` aus diesem Commit nach `.codex/skills/todo/` kopieren und die persönlichen Pfade in `SKILL.md` durch eigene Pfade ersetzen. Eine konkrete Todo-Datei und ein Verzeichnis für die Chat-Weiterleitungen müssen vorhanden sein. Die Originaldatei verlangt einen Server ausschließlich auf `127.0.0.1:8796`; den Mac-LaunchAgent unter Windows durch einen passenden lokalen Serverstart ersetzen. Ein Link verwendet eine echte Sitzungs-ID und leitet zur Codex-Sitzung weiter. Das ist eine aus der Originaldatei abgeleitete Einrichtung, keine getestete Installation auf diesem Rechner. [tweet-2053441168189612337](../sources/tweet-2053441168189612337.md)

Der Skill enthält keinen eigenen zweimal täglichen Zeitplan. Dieser muss separat eingerichtet werden. Die geprüfte Originaldatei ist als Rechercheartefakt `output/todo-upstream-b4cc41e.md` gespeichert; Raw bleibt unverändert. [tweet-2053441168189612337](../sources/tweet-2053441168189612337.md)
