---
tags: [agents, tools, product-building]
sources: [tweet-2052482874126020882.md]
created: 2026-10-14
updated: 2026-10-14
---

# Rowboat

## Rolle und Arbeitsgedächtnis (Stand 2026-05; gespeicherte Quellenstände)

[rowboatlabs/rowboat](https://github.com/rowboatlabs/rowboat) beschreibt einen AI-Coworker für Mac, Windows und Linux. E-Mails, Meetings und weitere Gespräche werden laut README in einen lokalen, verlinkten Markdown-Wissensgraphen integriert; E-Mail, Notizen, Browser, Meeting-Erfassung, Code-Modus und Projektbereiche bilden Arbeitsoberflächen. Das Projekt nutzt eine verwandte Ablageidee wie [LLM Wiki Pattern](../concepts/LLM%20Wiki%20Pattern.md), erweitert sie jedoch um laufenden Arbeitskontext und Aktionen. [tweet-2052482874126020882](../sources/tweet-2052482874126020882.md)

Der gespeicherte Einrichtungsartikel nennt `~/.rowboat/knowledge/` mit People, Organizations, Projects, Topics, Meetings und eigenen Notes. Entscheidungen, Zusagen und Terminänderungen sollen mit beteiligten Personen und Projekten verknüpft werden; Entitäten entstehen erst bei ausreichendem Signal. `Today(.)md` dient laut Artikel als Einstieg, bevor relevante Entitätsdateien geladen werden. Das sind dokumentierte Projekt-/Autorenangaben ohne eigene Coverage-Prüfung. [tweet-2052482874126020882](../sources/tweet-2052482874126020882.md)

## Einrichtung und Modelle (Stand 2026-05; Artikel)

Der Artikel konfiguriert Modelle über Settings → Models oder `~/.rowboat/config/models.json`. Er nennt Ollama mit `http://localhost:11434`, LM Studio und gehostete Anbieter mit eigenem API-Schlüssel. Lokale Markdown-Speicherung legt den Inferenzort nicht fest: Bei einem gehosteten Modell gehen Prompts an dessen Anbieter. [tweet-2052482874126020882](../sources/tweet-2052482874126020882.md)

Für Gmail, Kalender und Drive beschreibt er ein eigenes Google-Cloud-Projekt, aktivierte APIs, OAuth-Consent mit Testnutzer, einen Web-OAuth-Client und `http://localhost:8080/oauth/callback` als Redirect. Der im Repository verlinkte Google-Setup-Leitfaden ist der Einstieg für diese Integration. Fireflies-/Granola-Zugangsdaten ermöglichen laut Artikel den Import von Meeting-Inhalten. [tweet-2052482874126020882](../sources/tweet-2052482874126020882.md)

## Laufende Aufgaben und Erweiterungen (gespeicherter Quellenstand)

`@rowboat` soll eine Notiz als Live Note markieren, die bei neuen relevanten Informationen fortgeschrieben wird. Hintergrundagenten können laut Quellen zeitgesteuert oder durch Ereignisse wie neue E-Mails starten. Die README nennt auch Browseraktionen und Code-Arbeit mit [Claude Code](Claude%20Code.md) oder [Codex](Codex.md); das sind Produktangaben, keine hier getesteten Automationen. [tweet-2052482874126020882](../sources/tweet-2052482874126020882.md)

Optionale Integrationen umfassen Deepgram für Spracheingabe, ElevenLabs für Sprachausgabe, Exa für Webrecherche sowie MCP beziehungsweise Composio für weitere Werkzeuge. API-Schlüssel liegen laut Anleitung unter `~/.rowboat/config/`; lokale Ausführung der Integrationen ist mit externen API-Aufrufen vereinbar. Die README nennt Apache-2.0. [tweet-2052482874126020882](../sources/tweet-2052482874126020882.md)

## Evidenzgrenze

Die Quelle zeigt eine eigene Implementierung für Arbeitsgedächtnis, aber keinen kontrollierten Vergleich mit einem gepflegten Wiki. Die Artikelaussage, Wikis könnten geänderte Termine oder Zusagen grundsätzlich nicht abbilden, ist eine Autorenabgrenzung und keine nachgewiesene technische Grenze des [LLM Wiki Pattern](../concepts/LLM%20Wiki%20Pattern.md). Die kurze gespeicherte Videotranskription ersetzt weder Einrichtungsnachweis noch Laufzeittest. [tweet-2052482874126020882](../sources/tweet-2052482874126020882.md)
