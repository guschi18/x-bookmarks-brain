---
tags: [tools, agents]
sources: [tweet-2112371824696901818.md]
created: 2026-10-23
updated: 2026-10-23
---

# PandaCode

## Überblick (Stand 2026-10)

PandaCode (aicodeking/pandacode) ist ein nativer Desktop-Arbeitsplatz für Coding-Agents. Er startet die vorhandenen Coding-CLIs nebeneinander, darunter [Claude Code](Claude%20Code.md), Codex, Kimi Code, OpenCode, GLM Coding Plan, GitHub Copilot CLI, Antigravity, Grok Build und DeepSeek, und bietet Projekte, Git, Terminal und Browser in einem Fenster. [tweet-2112371824696901818](../sources/tweet-2112371824696901818.md)

Gebaut mit Tauri 2, Rust, SQLite und TypeScript über das Webview des Betriebssystems; ohne gebündeltes Chromium, Node-Server oder React. Lizenz: MIT mit Zusatz, dass kommerziell genutzte oder öffentlich veröffentlichte Forks auf PandaCode hinweisen müssen. Kein Konto, kein Lizenzschlüssel, keine Telemetrie. [tweet-2112371824696901818](../sources/tweet-2112371824696901818.md)

## Funktionen laut README und Post

- Task-Board (Pending, In progress, Review, Completed) und parallele Aufgaben über Projekte. [tweet-2112371824696901818](../sources/tweet-2112371824696901818.md)
- Agent-Teams aus einem Architekten und bis zu drei Workern über verschiedene Harnesses und Modelle. [tweet-2112371824696901818](../sources/tweet-2112371824696901818.md)
- Bots hinter Telegram, Slack, Discord, WhatsApp oder lokalem Web-Chat. [tweet-2112371824696901818](../sources/tweet-2112371824696901818.md)
- Lokale VMs (Tart auf Apple Silicon) und Cloud-Sandboxes (Daytona, Cloudflare, AWS), iOS- und Android-Simulatoren. [tweet-2112371824696901818](../sources/tweet-2112371824696901818.md)
- Deploy-Aufgaben für Vercel, Cloudflare, Railway, AWS und Google Cloud mit Freigabe je CLI-Lauf. [tweet-2112371824696901818](../sources/tweet-2112371824696901818.md)
- GitHub-Ansicht, Git-Worktrees je Task, Token-Saver-Antwortstile und Anzeige von Kontolimits und Kosten. [tweet-2112371824696901818](../sources/tweet-2112371824696901818.md)

## Evidenzgrenze

Die Leistungszahlen im Post (12 MB, erstes Bild unter 0,3 s, 180 MB bei etwa 30 Agents, rund 4x schneller als [T3 Code](T3%20Code.md), bis zu 30 Prozent Leistungsgewinn durch Orchestrierung, 60 bis 90 Prozent Tokenersparnis durch den Saver) sind Eigenangaben des Autors ohne Messmethode. Der Autor räumt Fehler ein, da er die App allein gebaut hat. Die App wurde nicht getestet. Verwandt: [Harp](Harp.md). [tweet-2112371824696901818](../sources/tweet-2112371824696901818.md)
