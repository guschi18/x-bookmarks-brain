---
tags: [tools, agents]
sources: [tweet-2112922431237062936.md]
created: 2026-10-23
updated: 2026-10-23
---

# Chops

## Überblick (Stand 2026-10)

Chops (Shpigford/chops) ist eine macOS-App, die Skills und Agents von Claude Code, Cursor, Codex, Windsurf und Amp an einem Ort findet, ordnet und bearbeitet; Copilot und Aider erkennt sie nur auf Projektebene. Tom Dörr stellt sie mit einem Screenshot der Repository-Seite vor. [tweet-2112922431237062936](../sources/tweet-2112922431237062936.md)

## Funktionen laut README

- Scan der Tool-Verzeichnisse, etwa ~/.claude/skills/, ~/.claude/agents/, ~/.codex/skills/, ~/.cursor/skills/ und ~/.agents/skills/. [tweet-2112922431237062936](../sources/tweet-2112922431237062936.md)
- Eingebauter Editor mit Frontmatter-Parsing, Volltextsuche, Sammlungen ohne Änderung der Quelldateien und Dateiüberwachung über FSEvents. [tweet-2112922431237062936](../sources/tweet-2112922431237062936.md)
- Anlegen neuer Skills und Agents mit passendem Gerüst je Tool. [tweet-2112922431237062936](../sources/tweet-2112922431237062936.md)
- Entfernte Server (OpenClaw, Hermes) und Installation aus der skills.sh-Registry. [tweet-2112922431237062936](../sources/tweet-2112922431237062936.md)
- Skills werden über den aufgelösten Symlink-Pfad dedupliziert; die App läuft ohne Sandbox, weil sie Dotfiles im Home-Verzeichnis lesen muss. [tweet-2112922431237062936](../sources/tweet-2112922431237062936.md)

Die App ist in Swift geschrieben und steht unter FSL-1.1-MIT; es gibt keine automatisierte Testsuite. [tweet-2112922431237062936](../sources/tweet-2112922431237062936.md)

## Evidenzgrenze

Die Angaben stammen aus README und Screenshot; die App wurde nicht installiert oder getestet. Verwandte Werkzeuge mit anderem Ansatz: [Skill Doctor](Skill%20Doctor.md) (Audit über Gesprächsverläufe) und [Skill Cleaner](Skill%20Cleaner.md) (Audit des geladenen Inventars). [tweet-2112922431237062936](../sources/tweet-2112922431237062936.md)
