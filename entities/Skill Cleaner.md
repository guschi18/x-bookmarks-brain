---
tags: [agents, tools]
sources: [tweet-2058917897590673525.md]
created: 2026-10-01
updated: 2026-10-03
---

# Skill Cleaner

## Zweck und Artefakt (Stand 2026-05)

Skill Cleaner ist Steinbergers dokumentiertes Audit für Skill-Inventar, lange Beschreibungen, Dubletten und vermutete ungenutzte Skills; [Skill-Datei](https://github.com/steipete/agent-scripts/blob/main/skills/skill-cleaner/SKILL.md). [tweet-2058917897590673525](../sources/tweet-2058917897590673525.md)

## Ablauf und Budgetmodell (Stand 2026-05)

Der Skill startet den Analyzer mit node --experimental-strip-types skills/skill-cleaner/scripts/skill-cleaner.ts --months 3. Die Auswertung priorisiert Live-Inventar und Budget vor Beschreibungen, Dubletten, Nutzungskandidaten und Herkunftsordnern. [tweet-2058917897590673525](../sources/tweet-2058917897590673525.md)

Laut Dokument nutzt der Analyzer standardmäßig das sichtbare Inventar aus codex debug prompt-input; --no-live schaltet auf einen breiteren Dateisystemscan um. Geladene Skills werden von deaktivierten oder archivierten Kopien unterschieden, reale Pfade dedupliziert. [tweet-2058917897590673525](../sources/tweet-2058917897590673525.md)

Das Dokument modelliert ein Zwei-Prozent-Kontextbudget, schätzt Tokens mit UTF-8-Bytes geteilt durch vier und beschreibt Kürzung beziehungsweise Auslassung von Beschreibungen. Modellcache und ein Fallback von 272.000 Tokens werden genannt; das sind dokumentierte Annahmen des Analyzers, keine hier verifizierten aktuellen [Codex](Codex.md)-Interna. [tweet-2058917897590673525](../sources/tweet-2058917897590673525.md)

## Löschgrenzen (Stand 2026-05)

Nutzung wird heuristisch aus Erwähnungen und Skill-Dateizugriffen in Logs abgeleitet. Vor Entfernen soll geprüft werden, dass die behaltene Kopie existiert und geladen wird; Repository-Richtlinien und konkrete Triggerwörter sollen erhalten bleiben. Fehlende Logtreffer allein beweisen keine Nutzlosigkeit, und der Skill verlangt zunächst Vorschläge statt automatischer Änderungen. [tweet-2058917897590673525](../sources/tweet-2058917897590673525.md)
