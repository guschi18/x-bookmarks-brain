---
tags: [agents, tools]
sources: [tweet-2095651107645145538.md]
created: 2026-10-03
updated: 2026-10-03
---

# Ant Apply

## Überblick (Stand 2026-09)

`ant apply` ist ein Befehl der ant-CLI (ab Version 1.30.0), der Claude-API-Ressourcen aus Dateien im Repository anlegt und aktualisiert: Agenten, Umgebungen, Skills, Speicher (memory stores) und Deployments. Sie ändern sich über dasselbe Review wie Code; man beschreibt jede Ressource in einer Datei, führt den Befehl aus und bestätigt den angezeigten Plan. [tweet-2095651107645145538](../sources/tweet-2095651107645145538.md)

## Funktionsweise (Stand 2026-09)

- Dateiformate: Ein Agent ist eine Markdown-Datei unter `agents/` (Frontmatter als Konfiguration, Text als Systemprompt); Umgebungen und Speicher sind YAML in `environments/` und `memory_stores/`; ein Deployment ist Markdown in `deployments/`; ein Skill ist ein Verzeichnis mit SKILL.md. [tweet-2095651107645145538](../sources/tweet-2095651107645145538.md)
- Lockfile: Der erste Lauf schreibt `claude-lock.json` mit den Ressourcen-IDs sowie Organisation und Workspace; es wird eingecheckt, damit spätere Läufe aktualisieren statt neu anzulegen. Zwei Hashes erkennen geänderte Dateien oder außerhalb geänderte Ressourcen. [tweet-2095651107645145538](../sources/tweet-2095651107645145538.md)
- Verweise: Ressourcen verweisen per relativem Pfad aufeinander; `ant apply` legt sie in Abhängigkeitsreihenfolge an und pinnt Versionen. Skills können auch per GitHub-URL eingebunden werden. [tweet-2095651107645145538](../sources/tweet-2095651107645145538.md)
- Sicherheit: Wurde eine Ressource außerhalb der Dateien geändert, bricht der Plan mit „refusing to apply“ ab; `--force` überschreibt. Gelöschte Dateien lassen die Ressource stehen, `--prune` entfernt sie. In der Konsole angelegte Ressourcen lassen sich nicht übernehmen. [tweet-2095651107645145538](../sources/tweet-2095651107645145538.md)

## CI (Stand 2026-09)

Ohne Terminal braucht der Befehl `--yes` oder `--dry-run`. Empfohlen: nach dem Merge `ant apply --yes .`, bei Pull Requests `--dry-run .`, das Lockfile am Jobende auch nach Teilfehlern einchecken, nur einen Lauf gleichzeitig und Authentifizierung per Workload Identity Federation. [tweet-2095651107645145538](../sources/tweet-2095651107645145538.md)

## Grenzen (Stand 2026-09)

Es ist Herstellerdokumentation ohne eigene Erprobung. Das Lockfile wird nicht gesperrt, parallele Läufe sind nicht abgesichert. Die zugrunde liegenden Konzepte stehen in der verlinkten Managed-Agents-Dokumentation, die hier nicht gespeichert ist. Zur Claude-Seite siehe auch [Claude API Skill](Claude%20API%20Skill.md). [tweet-2095651107645145538](../sources/tweet-2095651107645145538.md)
