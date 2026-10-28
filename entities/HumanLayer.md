---
tags: [agents, tools]
sources: [tweet-2114403120377626859.md]
created: 2026-10-27
updated: 2026-10-27
---

# HumanLayer

## Überblick (Stand 2026-10)

HumanLayer ist laut gespeicherter GitHub-README eine Plattform, die Coding-Agenten (Claude Code, Codex, OpenCode, Pi) auf eigenen Rechnern ausführt und dem Team erlaubt, sie von einem Ort aus zu steuern: Aufgaben, Sitzungen, Pläne und Reviews, synchronisiert zwischen Desktop-App, Web-App und einem Daemon je Host. [tweet-2114403120377626859](../sources/tweet-2114403120377626859.md)

## Aufbau laut README (Stand 2026-10)

- Turborepo-Monorepo mit Bun; Apps u. a. riptide-ui, riptide-daemon, CLI `humanlayer`, API (oRPC + Hono), Admin-Web-App und Lambda-Jobs. [tweet-2114403120377626859](../sources/tweet-2114403120377626859.md)
- Plugins spiegeln Sitzungen von Claude Code, OpenCode und Pi in HumanLayer; mitgeliefert sind Research-Plan-Implement-Skills und ein Linear-CLI. [tweet-2114403120377626859](../sources/tweet-2114403120377626859.md)
- Lizenz Apache 2.0; ein Build aus dem Quellcode sendet laut README nichts an den Anbieter (Sentry, PostHog, WorkOS nur per Umgebungsvariable). Anleitungen zum Selbsthosting sind noch in Arbeit; die Docker-Compose-Datei nutzt einfache Standardpasswörter. [tweet-2114403120377626859](../sources/tweet-2114403120377626859.md)

## Beleglage

__arch3r berichtet, das Projekt löse in einigen Projekten seine Herausforderungen "sehr gut", und fand es, weil es als Open Source erschien. Das ist ein Einzelerfahrungsbericht; Messwerte fehlen, die Funktionsangaben sind Projektbeschreibung. Verwandt: [Agentic Engineering](../concepts/Agentic%20Engineering.md). [tweet-2114403120377626859](../sources/tweet-2114403120377626859.md)
