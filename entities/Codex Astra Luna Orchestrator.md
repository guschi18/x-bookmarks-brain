---
tags: [agents, tools]
sources: [tweet-2096631909539606638.md, tweet-2103185949341491513.md, tweet-2101956340877000754.md]
created: 2026-10-03
updated: 2026-10-08
---

# Codex Astra Luna Orchestrator

## Überblick

Das Repository donvito/codex-astra-luna-orchestrator beschreibt laut README ein konfigurierbares Codex-Setup: GPT-6 Astra ist Root-Orchestrator und Reviewer, GPT-5.6 Luna (Namensstand der README vom 2026-09-06; ein Artikel vom 2026-09-24 nennt GPT-6 Luna, ob dieselbe Modellfamilie gemeint ist, ist offen) das standardmäßig festgelegte Modell der Ausführungs-Subagenten. [tweet-2096631909539606638](../sources/tweet-2096631909539606638.md)

Der Post meldet eine aktualisierte Skill "Astra Orchestrator + Luna Subagents" mit strengerer Durchsetzung von Luna für Aufgaben wie Recherche und Erkundung. Der Screenshot zeigt Aufrufe für explore_repo und research_news mit dem Modell gpt-5.6-luna. [tweet-2096631909539606638](../sources/tweet-2096631909539606638.md)

## Aufbau

- Rollen: explorer, worker, tester, researcher laufen auf Luna; reviewer läuft auf Astra, damit die Abschlussprüfung von einem anderen Modell kommt als dem, das den Code schrieb. [tweet-2096631909539606638](../sources/tweet-2096631909539606638.md)
- Pläne: Der Installer fragt nach dem Codex-Plan. Pro installiert Astra als Root; Plus nutzt Luna mit maximalem Reasoning als Root, damit orchestrierte Sitzungen in den Limitfenstern von Plus bleiben. Die Subagentenrollen sind gleich. [tweet-2096631909539606638](../sources/tweet-2096631909539606638.md)
- Konfiguration: `[agents]` mit bis zu vier parallelen Threads pro Sitzung, `default_subagent_model = "gpt-5.6-luna"` und mittlerem Subagent-Reasoning. Jede Rollendatei pinnt ihr Modell; wer einen einzigen Schalter will, entfernt die Overrides aus den Rollendateien. [tweet-2096631909539606638](../sources/tweet-2096631909539606638.md)
- Dateien: `.codex/config.toml`, `.codex/agents/*.toml`, die Skill `astra-orchestrator`, `AGENTS.md`, Anleitungen und `scripts/token_usage.py`; Installer für macOS/Linux (setup.sh) und Windows (setup.ps1). [tweet-2096631909539606638](../sources/tweet-2096631909539606638.md)

## Grenzen

Kosten- oder Qualitätsvorteile gegenüber einem Einzelmodell sind in den gespeicherten Quellen nicht gemessen. Die Modellnamen stammen aus Repo und Post. Das Muster der Aufgabenteilung ähnelt [Hook-Enforced Model Routing](../concepts/Hook-Enforced%20Model%20Routing.md); dort erzwingt ein Hook die Delegation, hier Skill und Rollenkonfiguration. Siehe auch [Codex](Codex.md). [tweet-2096631909539606638](../sources/tweet-2096631909539606638.md)

## Variante mit GPT-6 Luna, Sol und Jev (Stand 2026-09)

Eine andere Codex-Konfiguration nutzt eine Eskalationsleiter Luna Low, Medium, High bis Sol High und lässt [Jev](Jev.md) über Retry, Eskalation und Abschluss entscheiden, während Compiler, Tests und Lint als Wahrheitsschicht dienen; siehe [Typed Decision Layer](../concepts/Typed%20Decision%20Layer.md). Die genannten Preise (Luna 0,10, Sol 2,00 Dollar je Million Input) stammen aus dem Artikel. [tweet-2103185949341491513](../sources/tweet-2103185949341491513.md)

## Ergänzungen (Stand 2026-09)

[Astra Agent Instructions](Astra%20Agent%20Instructions.md) zeigt eine andere Delegation: Astra als Hauptagent, Sol (gpt-5.6-sol, mittleres Reasoning) für klar umrissene größere Umsetzungen. Es ist eine persönliche Instruktionsdatei, keine Orchestrator-Konfiguration. [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md)
