---
tags: [agents, tools]
sources: [tweet-2116905923109089285.md]
created: 2026-11-02
updated: 2026-11-02
---

# DeepSeek Superagent

## Überblick (Stand 2026-11)

dsh-superagent ist laut kimmonismus ein von DeepSeek als Open Source veröffentlichter Super-agent-Prototyp. Eine Router-Session spricht mit Menschen und verteilt Arbeit; isolierte Worker bearbeiten Aufgaben parallel und werden von GitHub-Ereignissen ausgelöst. [tweet-2116905923109089285](../sources/tweet-2116905923109089285.md)

Der gespeicherte Screenshot der Dokumentation beschreibt den Prototyp als proaktiven Coding-Agenten, der GitHub-Ereignisse überwacht und in isolierten Sitzungen parallel arbeitet. Das Ziel ist, menschliche Aufmerksamkeit zu minimieren und den Wert zu maximieren. Die Dokumentation nennt das Projekt einen nicht offiziellen, unausgereiften Forschungs-Prototyp. [tweet-2116905923109089285](../sources/tweet-2116905923109089285.md)

## Messung (Herstellerangabe)

Im eigenen Test sank die p95-Abschlusszeit von 29,5 auf 15,7 Minuten gegenüber einer Einzelsession mit Subagents. Testaufbau, Aufgabenmix und Stichprobe stehen nicht in Raw; die Zahl ist eine Selbstangabe. [tweet-2116905923109089285](../sources/tweet-2116905923109089285.md)

## Evidenzgrenze

Raw enthält nur den Post, den Screenshot und einen zitierten Post mit einem t.co-Link ohne Repo-URL. Die Architektur ist nicht aus dem Code geprüft. Verwandt: [Agent Workflow Graphs](../concepts/Agent%20Workflow%20Graphs.md) (Orchestrierung paralleler Agenten) und [Claude Code](Claude%20Code.md) (Subagent-Vergleich). [tweet-2116905923109089285](../sources/tweet-2116905923109089285.md)
