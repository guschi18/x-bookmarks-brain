---
tags: [agents, tools]
sources: [tweet-2104656567505211685.md]
created: 2026-10-06
updated: 2026-10-06
---

# Agent Scripts

## Kanonisches Repository (Stand 2026-09)

[Agent Scripts](https://github.com/steipete/agent-scripts) ist laut gespeicherter README Peter Steinbergers zentrale Quelle für AGENTS.MD, skills/, portable scripts/ und Validierungshooks. Der Post empfiehlt Fork, eigene Regeln und Entfernung unbenötigter Skills; persönliche Hosts und Accounts sind anzupassen. [tweet-2104656567505211685](../sources/tweet-2104656567505211685.md)

## Instruktionen und Skill-Discovery (Stand 2026-09)

Die dokumentierte globale Konfiguration verweist ~/.codex/AGENTS.md sowie ~/.claude/CLAUDE.md und ~/.claude/AGENTS.md auf die gemeinsame AGENTS.MD. Downstream-Repositories beginnen mit READ ~/Projects/agent-scripts/AGENTS.MD BEFORE ANYTHING (skip if missing) und setzen lokale Regeln darunter. [tweet-2104656567505211685](../sources/tweet-2104656567505211685.md)

scripts/sync-skills verknüpft für [Codex](Codex.md) ganze Skill-Wurzeln und für Claude einzelne Skills flach nach ~/.claude/skills/<name>/SKILL.md. Die README beschreibt unterschiedliche Discovery-Konventionen; das sind dokumentierte Clientstände, kein hier getesteter plattformübergreifender Standard. [tweet-2104656567505211685](../sources/tweet-2104656567505211685.md)

Namenskollisionen werden agent-scripts vor manager vor codex-local aufgelöst; reale Zieldateien bleiben erhalten. Der Sync ist laut README idempotent, meldet Konflikte und entfernt verwaltete kaputte oder alte Links. Besondere Reparaturmodi haben explizite Allowlisten. [tweet-2104656567505211685](../sources/tweet-2104656567505211685.md)

## Pflege und Verbindungen (Stand 2026-09)

Skill-Beschreibungen sollen kurz auf den Einsatz routen, Körper operational bleiben und wiederholbare Kommandos in Helferskripten liegen. scripts/validate-skills prüft Frontmatter, scripts/docs-list.ts dokumentiert Onboarding; [Skill Cleaner](Skill%20Cleaner.md) und die Vorlage hinter [Kimi First](Kimi%20First.md) sind Teile beziehungsweise Ableitungen derselben Sammlung. [tweet-2104656567505211685](../sources/tweet-2104656567505211685.md)

Installation, Symlink-Verhalten auf Windows und die behauptete Skillzahl wurden nicht geprüft. Der zusätzlich gespeicherte, Viktor-gesponserte Fünfschichten-Artikel ist eine separate Quelle für Context, Loops, Routing, Harness und Evals, kein Test dieses Sync-Repositories. [tweet-2104656567505211685](../sources/tweet-2104656567505211685.md)
