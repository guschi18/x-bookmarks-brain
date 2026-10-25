---
tags: [agents, tools]
sources: [tweet-2106455605925822967.md, tweet-2106412212978098295.md, tweet-2106143340794454346.md, tweet-2106118517447876618.md, tweet-2105721441622884802.md, tweet-2113026278504755415.md, tweet-2109822699174559748.md]
created: 2026-10-04
updated: 2026-10-23
---

# Claude Code Mods

## Prompt cache control (Stand 2026-10)

Daniel San recommends npx claude-code-templates@latest --mod observability/prompt-cache-control for a [Claude Code](Claude%20Code.md) cache timer and notifications. [tweet-2106455605925822967](../sources/tweet-2106455605925822967.md)

The post describes five minutes and claims savings and longer sessions, without a measurement; the saved video transcript is empty. See [Prompt Caching](../concepts/Prompt%20Caching.md) for cache behavior. [tweet-2106455605925822967](../sources/tweet-2106455605925822967.md)

## Goal Meter (Stand 2026-10)

Nate Herk's screenshot shows a goal, task list, progress, elapsed time, estimated time left and an all-tasks control. ETA accuracy is not evidenced. [tweet-2106412212978098295](../sources/tweet-2106412212978098295.md)

The user supplied [Nate Herk's mods resource](https://www.skool.com/ai-automation-society/new-video-5-claude-code-mods-that-everyone-needs); the public post promises installation guidance and access to his mods, but community files were not inspected. [tweet-2106412212978098295](../sources/tweet-2106412212978098295.md)

These extensions relate to [Claude Plugins](Claude%20Plugins.md), which package additions to the coding environment. [tweet-2106455605925822967](../sources/tweet-2106455605925822967.md) [tweet-2106412212978098295](../sources/tweet-2106412212978098295.md)

## Additions (Stand 2026-10)

### Derive mods from session logs

Nate Herk uses repeated instructions, recurring tasks and workflow friction to choose mods, then reviews the suggestions before building; this is an application of [Session History Review](../concepts/Session%20History%20Review.md). [tweet-2106143340794454346](../sources/tweet-2106143340794454346.md)

Reusable prompt from the saved article: [tweet-2106143340794454346](../sources/tweet-2106143340794454346.md)

> Look through my session logs and identify the tasks I do often, the instructions I repeat, and the friction in my workflow. Suggest five useful Claude Code mods based on those patterns, and explain what each would do. [tweet-2106143340794454346](../sources/tweet-2106143340794454346.md)

### Four workflow examples

- Cache Keeper shows context, five-hour/weekly usage and an API-equivalent cost estimate, plus handoff and Clear and Continue buttons. The dollar estimate is not the subscription bill; its demonstrated timer is about 60 minutes, explicitly not a universal cache guarantee. [tweet-2106143340794454346](../sources/tweet-2106143340794454346.md)
- Recording Mode masks displayed email/financial values while source files can still contain and receive real values; on-screen masking does not sanitize files or other windows. [tweet-2106143340794454346](../sources/tweet-2106143340794454346.md)
- Goal Meter shows tasks and elapsed time across chats; task completion does not establish exact remaining time. [tweet-2106143340794454346](../sources/tweet-2106143340794454346.md)
- Collision Guard warns before editing a file another chat touched within the author's 30-minute window; choices include proceed, worktree and cancel. [tweet-2106143340794454346](../sources/tweet-2106143340794454346.md)

### You Should Know

ClaudeDevs describes an output scanner for important information users might miss. Enable: /plugin enable cc-plugin-you-should-know@builtin. The demo transcript is empty, and detection accuracy or complete behavior is not documented. [tweet-2106118517447876618](../sources/tweet-2106118517447876618.md)

## Bauanleitung und Beispiele (Stand 2026-10)

Der [Getting-started-Artikel](https://claude.dev/blog/getting-started-with-claude-code-mods/) beschreibt Mods als langlebige JavaScript-/TypeScript-Module in [Claude Plugins](Claude%20Plugins.md): Ein Manifest und hooks/hooks.json laden register(on, options); Hooks können Ereignisse beobachten, umschreiben oder ohne next(e) selbst beantworten. Laut Artikel braucht dies [Claude Code](Claude%20Code.md) 2.1.287+, und die lokal erzeugten Typdeklarationen sind die Referenz für die installierte Version. [tweet-2105721441622884802](../sources/tweet-2105721441622884802.md)

Token Weather liest $.session.usage() nach Hauptagent-Turns und zeichnet Kontextanteil, Tokens, zwölf vergangene Werte und die Änderung des letzten Turns über dem Prompt. Der Artikel enthält den vollständigen Prompt, Code, Typvertrag und Test; historische Werte gehören in $.state, damit sie Hot Reload überleben. [tweet-2105721441622884802](../sources/tweet-2105721441622884802.md)

Ablauf der Anleitung: Pluginordner anlegen, AbovePrompt hooken, Zustandsvertrag deklarieren, mit claude plugin validate und claude plugin test prüfen, dann Marketplace einrichten und Plugin installieren; /reload-plugins beziehungsweise Neustart aktiviert die Installation. Temporär generierte Mods müssen zum Behalten aus dem Sitzungsordner kopiert und installiert werden. [tweet-2105721441622884802](../sources/tweet-2105721441622884802.md)

Blast Radius hält erkannte riskante Bash-Befehle für eine Vorschau mit Proceed/Cancel an. Weil nur der Befehlsstring klassifiziert wird, können Aliase, Substitutionen und indirekte Skripte die Erkennung umgehen; dies ist laut Artikel keine harte Berechtigungsgrenze. Replay Theater beobachtet Edit/Write, gruppiert Änderungen pro Hauptagent-Turn und zeigt über /replay die einzelnen Diffs. [tweet-2105721441622884802](../sources/tweet-2105721441622884802.md)

Der Artikel verweist auf [anthropics/claude-code](https://github.com/anthropics/claude-code), darunter mods/ mit Beispielen und Tests. Verhalten und Beispiele sind gespeicherte Herstellerdokumentation, kein lokaler Funktionstest. [tweet-2105721441622884802](../sources/tweet-2105721441622884802.md)

## Stack Viewer (Stand 2026-10)

Daniel San beschreibt /stack als Mod, der alle installierten und verfügbaren Bestandteile von [Claude Code](Claude%20Code.md) auflistet: Skills, Subagents, Commands, Hooks, MCP-Server, Plugins, Settings und Output Styles, gegliedert nach Enterprise, User, Project, Plugin und CLI-Flags. [tweet-2113026278504755415](../sources/tweet-2113026278504755415.md)

Das Panel zeigt, was aktiv, deaktiviert oder von anderen Komponenten überschrieben ist, und listet eingebaute Commands, Skills und Subagents, auch solche ohne Erwähnung in der offiziellen Dokumentation. Installation: npx claude-code-templates@latest --mod ui/stack-viewer. [tweet-2113026278504755415](../sources/tweet-2113026278504755415.md)

Evidenzgrenze: Das gespeicherte Demo-Video hat kein Transkript. Der Zusammenhang zwischen Panel und Tokenverbrauch ist eine Aussage des Autors ohne Messung. [tweet-2113026278504755415](../sources/tweet-2113026278504755415.md)

## Turn Inspector (Stand 2026-10)

Daniel San beschreibt Turn Inspector als Mod, der pro Turn aufschlüsselt, woraus das Kontextfenster von [Claude Code](Claude%20Code.md) besteht: Systemprompt, Tools, Memory, vorherige Turns, Modellausgabe und Tool-Ergebnisse. Ziel ist zu sehen, wohin die Tokens einer Sitzung gehen. Installation: npx claude-code-templates@latest --mod ui/turn-inspector. [tweet-2109822699174559748](../sources/tweet-2109822699174559748.md)

Die gespeicherte README zeigt den Mod-Installationsweg der Vorlagensammlung claude-code-templates; die Mod-Funktion selbst wird nur im Post beschrieben. Das Demo-Video hat kein Transkript, Messungen fehlen. Hintergrund zur Kontextaufteilung: [Context Engineering](../concepts/Context%20Engineering.md). [tweet-2109822699174559748](../sources/tweet-2109822699174559748.md)
