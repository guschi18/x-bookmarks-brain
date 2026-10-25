---
tags: [agents, tools]
sources: [tweet-2047007924279767332.md]
created: 2026-10-18
updated: 2026-10-18
---

# OpenChronicle

## Projekt und gespeicherter Stand (Post 2026-04; README v0.1.0)

Das Repository [Einsia/OpenChronicle](https://github.com/Einsia/OpenChronicle) beschreibt eine lokale, inspizierbare Memory-Schicht für toolfähige Agenten. Die gespeicherte README kennzeichnet v0.1.0 als frühe Alpha ausschließlich für macOS, MIT-lizenziert; sie nennt macOS 13 oder neuer und Xcode Command Line Tools als Voraussetzungen. Ein historischer Tag oder Commit der gespeicherten README liegt nicht vor. [tweet-2047007924279767332](../sources/tweet-2047007924279767332.md)

## Kontext erfassen und verdichten (gespeicherte README v0.1.0)

Accessibility-/AX-Ereignisse sind das primäre Signal: aktive App, fokussiertes Element, sichtbarer Text und URL werden dedupliziert und normalisiert. Screenshots sind ein ergänzendes Signal; die behaupteten Kosten- und Intentionsvorteile von AX stammen vom Anbieter. [tweet-2047007924279767332](../sources/tweet-2047007924279767332.md)

Die dokumentierte Kette führt von Watcher, Dispatcher und Parser über Capture-Buffer und minutenweise Timeline zu Session-Reduktion und Klassifikation. Das Diagramm nennt fünf Minuten Idle, drei Minuten beim App-Wechsel und zwei Stunden maximale Sessionlänge; daraus folgt keine hier getestete universelle Segmentierung. [tweet-2047007924279767332](../sources/tweet-2047007924279767332.md)

Dauerhafte Fakten und tägliche Ereignisse werden in Markdown-Dateien für Nutzer, Projekte, Tools, Themen, Personen und Organisationen sowie lokalem SQLite FTS5 gespeichert. Änderungen sollen frühere Fakten superseden statt die Historie zu löschen. Das ist Arbeitskontext-Gedächtnis und kein Repository-Codegraph wie bei [Codebase Memory MCP](Codebase%20Memory%20MCP.md). [tweet-2047007924279767332](../sources/tweet-2047007924279767332.md)

## Agentenzugang und Betrieb (gespeicherte README v0.1.0)

MCP ist der am besten unterstützte Pfad; der Daemon nennt http://127.0.0.1:8742/mcp und Integrationen für [Claude Code](Claude%20Code.md), Claude Desktop, [Codex](Codex.md), opencode und eigene Agenten. Die README verlinkt eine getrennte MCP-Anleitung; deren Detailkonfiguration ist nicht als vollständiger Text gespeichert. [tweet-2047007924279767332](../sources/tweet-2047007924279767332.md)

Dokumentierte Befehle sind openchronicle start/status/pause/resume/stop sowie capture-once, timeline tick/list, writer run und rebuild-index. Als Modellwege nennt die README Ollama, LM Studio und LiteLLM-kompatible lokale oder Cloud-Anbieter; lokaler Speicher bedeutet daher nicht, dass jede Modellverarbeitung auf dem Gerät bleibt. [tweet-2047007924279767332](../sources/tweet-2047007924279767332.md)

## Evidenzgrenzen (Post 2026-04; gespeicherte README v0.1.0)

Die ursprüngliche Chronicle-Preisgegenüberstellung und Aussagen zu allgemeiner Agentenkompatibilität, Kosten und Kontextqualität sind Anbieterbehauptungen. Das Logo liefert keinen technischen Nachweis; weder macOS-Capture noch Retrieval, Datenschutz oder Integrationen wurden hier installiert oder geprüft. Der vollständige README-Text und alle 31 strukturierten Links bleiben auf der Source-Seite erhalten. [tweet-2047007924279767332](../sources/tweet-2047007924279767332.md)
