---
tags: [agents, tools]
sources: [tweet-2102198213067612337.md]
created: 2026-10-03
updated: 2026-10-03
---

# Kaku

## Editor und Daten (Stand 2026-09)

Die gespeicherte japanische Produktseite beschreibt Kaku als lokalen Markdown-Editor: Notizen bleiben Dateien im gewählten Ordner, Chatverläufe liegen daneben in SQLite; Obsidian-Wikilinks werden unterstützt. Die Seite nennt macOS 13+ auf Apple Silicon und Windows x64. [tweet-2102198213067612337](../sources/tweet-2102198213067612337.md)

## Agentenarbeit (Stand 2026-09)

Laut Anbieter können externe Agenten wie [Claude Code](Claude%20Code.md) oder [Codex](Codex.md) Markdown direkt bearbeiten; Änderungen erscheinen als Diff mit Übernehmen und Zurücksetzen. Kontext wird aus Links, Backlinks und verwandten Notizen gesammelt, Gespräche können verzweigt werden; CRDT soll gleichzeitige Änderungen erhalten. [tweet-2102198213067612337](../sources/tweet-2102198213067612337.md)

Optional bewertet [Jev](Jev.md) alle Kombinationen aus Notizen und bestehendem Tagvokabular probabilistisch. Eine verschiebbare Schwelle steuert die vorgeschlagenen Tags, die dieselbe Änderungsprüfung durchlaufen. Dafür braucht es einen TypeSafe-API-Key; die API-Nutzung wird separat berechnet. [tweet-2102198213067612337](../sources/tweet-2102198213067612337.md)

## Grenzen (Stand 2026-09)

Lokale Speicherung bedeutet laut Seite nicht rein lokale AI: Bei einer Anfrage geht ausgewählter Kontext an den Provider. Synchronisation, Datenschutz und Kompatibilität wurden nicht getestet; die kostenlose App ersetzt keine kostenpflichtige Provider-Nutzung. [tweet-2102198213067612337](../sources/tweet-2102198213067612337.md)
