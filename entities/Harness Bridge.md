---
tags: [agents, tools]
sources: [tweet-2100643846086389857.md]
created: 2026-10-08
updated: 2026-10-08
---

# Harness Bridge

## Rolle und Aufbau (Stand 2026-09)

[Harness Bridge](https://github.com/0xSero/harness-bridge) verbindet laut README Coding-Harnesses wie [Claude Code](Claude%20Code.md) und [Codex](Codex.md) mit OpenAI-, Anthropic- oder Responses-kompatiblen Inferenz-Endpunkten. Ein gemeinsamer Core trägt CLI, macOS-Menüleisten-App Local AI und Web-UI. [tweet-2100643846086389857](../sources/tweet-2100643846086389857.md)

Endpunkt, Schlüssel und Modell werden über die Startumgebung beziehungsweise Startargumente übergeben; bestehende Claude-, Codex- und OpenCode-Konfigurationen sollen dabei unverändert bleiben. Persistiert werden werkzeugeigene Auswahl und Provider-Konfiguration. [tweet-2100643846086389857](../sources/tweet-2100643846086389857.md)

## Einstieg und Auswahl (Stand 2026-09)

Das README verlangt Bun ab 1.1: Repository klonen, bun install ausführen und im Verzeichnis packages/cli mit bun link die Executables harness-bridge und hbr registrieren. Danach Provider mit providers add konfigurieren, mit models die angebotenen Modelle prüfen, mit use ein Modell wählen und mit run claude einen Harness starten. Die macOS-App benötigt zusätzlich Xcode Command Line Tools. [tweet-2100643846086389857](../sources/tweet-2100643846086389857.md)

providers scan prüft chat/completions, messages und responses mit kleinen Requests. Ein Harness wird nur angeboten, wenn sein Protokoll beantwortet wird; Claude nutzt messages, Codex responses, andere Clients meist chat. Das reale Kontextfenster soll aus der Modellliste des Endpunkts stammen. [tweet-2100643846086389857](../sources/tweet-2100643846086389857.md)

Reasoning bleibt bei auto unverändert; providers reasoning high setzt dokumentierte Harness-spezifische Parameter. Modelle und Snapshots werden 30 Sekunden gecacht; --fresh fragt erneut ab, bei Endpunktfehlern bleibt die letzte Modellliste verfügbar. [tweet-2100643846086389857](../sources/tweet-2100643846086389857.md)

## Ausführung und Grenzen (Stand 2026-09)

Claude Code und Codex starten laut README standardmäßig mit --dangerously-skip-permissions beziehungsweise --dangerously-bypass-approvals-and-sandbox. run --safe claude lässt die eingebauten Bypass-Flags für diesen Start weg; args zeigt oder ändert die gespeicherten Startflags. [tweet-2100643846086389857](../sources/tweet-2100643846086389857.md)

Der Schlüssel wird laut README in ~/.config/harness-bridge/config.json mit Modus 0600 gespeichert; der beschriebene Startpfad soll ihn weder in Session-Kommandos noch Logs schreiben. Der dokumentierte providers-add-Einrichtungsbefehl enthält dagegen einen --key-Parameter: die Aussage über Session-Starts ersetzt keine Prüfung der Einrichtungsumgebung. [tweet-2100643846086389857](../sources/tweet-2100643846086389857.md)

Die Web-UI bindet an 127.0.0.1:4141 ohne Authentifizierung. Fehlende Harnesses können beim Start installiert werden; --no-install verhindert dies. Warp-Tab-Config ist eine ausdrücklich genannte Ausnahme zum Schreiben ausschließlich eigener Konfigurationen. [tweet-2100643846086389857](../sources/tweet-2100643846086389857.md)

Das README berichtet Tests auf macOS arm64 und Linux x86_64/aarch64; Windows ist in der gespeicherten Testmatrix nicht enthalten. MIT-Lizenz und vorhandene Unit-/CLI-Tests sind Projektangaben, hier wurde das Werkzeug nicht installiert oder ausgeführt. [tweet-2100643846086389857](../sources/tweet-2100643846086389857.md)
