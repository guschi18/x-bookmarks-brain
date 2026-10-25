---
tags: [agents, tools]
sources: [tweet-2100962426439000484.md]
created: 2026-10-07
updated: 2026-10-08
---

# Jev Codex Router

## Rolle und Bezug (Stand 2026-09)

[Jev Codex Router](https://github.com/0xNatoshi/jev-codex-router) nutzt [Jev](Jev.md) für die Wahl von Modell und Thinking-Effort bei einzelnen [Codex](Codex.md)-Aufrufen, einschließlich Fortsetzungen nach Tools. Der ebenfalls verlinkte [Codex Router](https://codex-router.com/) stellt den lokalen Proxy bereit; das gespeicherte aktuelle README des Jev-Projekts enthält dessen gepflegten Fork direkt im Monorepo. [tweet-2100962426439000484](../sources/tweet-2100962426439000484.md)

Jev erhält einen begrenzten Entscheidungszustand; das ausführende Modell bekommt laut README den vollständigen kanonischen Codex-Request. Responses und SSE werden weitergereicht. Damit unterscheidet sich das Projekt vom Claude-Code-Mod [Jev Model Router](Jev%20Model%20Router.md). [tweet-2100962426439000484](../sources/tweet-2100962426439000484.md)

## Policy-Gist und abweichende Stände (Stand 2026-09)

Antonio Leiva berichtet, dass sein erster Aufbau fast alles an Sol leitete, auch einfache Aufgaben. Er ließ Astra die Jev-Anweisungen verbessern und verlinkt den vollständigen [Python-Gist](https://gist.github.com/antoniolg/62f82f2a5d191fe074e3f5065501993d). Die subjektiv bessere Delegation und langsamere Kontingentabnahme sind ein Einzelbericht ohne kontrollierten Vergleich. [tweet-2100962426439000484](../sources/tweet-2100962426439000484.md)

Der Gist lädt eine lokale Policy aus JEV_POLICY_FILE beziehungsweise ~/.codex/codex-router/jev-policy.json. Sie verlangt version 1, name, instructions und Kriterien für genau Luna, Sol und Astra; instructions und Kriterien ersetzen die Standardfrage zur Modellstufe. Die separate Effort-Frage bleibt erhalten. [tweet-2100962426439000484](../sources/tweet-2100962426439000484.md)

Dieser Gist verwendet bei Konfidenz unter 0,5 Sol, außer bei einer sauberen mechanischen Tool-Fortsetzung, die Jev als Luna mit low/medium gewählt hat. Luna erhält priority, Sol und Astra standard; Kompaktierungs-Checkpoints werden auf Sol/high festgelegt. [tweet-2100962426439000484](../sources/tweet-2100962426439000484.md)

Die gespeicherte README (Stand 2026-09-18) beschreibt dagegen vier unabhängige Choices für Pflicht-Astra, ausreichende Modellstufe, Effort und Route-Lease, die Leiter Luna → Terra → Sol → Astra und durchgehend standard. Es nennt ausdrücklich keinen Sol-Fallback bei niedriger Konfidenz, keine mechanische Ausnahme und kein Compaction-Pinning. Gist und README sind verschiedene Policy-Stände und dürfen nicht als identische Konfiguration zusammengeführt werden. [tweet-2100962426439000484](../sources/tweet-2100962426439000484.md)

## Einrichtung und Diagnose (Stand 2026-09)

Die README nennt macOS mit Codex Desktop, Node.js 22.19+, Python 3.11+ und einen TypeSafe-Key als Quickstart-Voraussetzungen. Nach Key-Konfiguration installiert ./install.sh den Stack; danach Codex neu öffnen und Jev Codex Router wählen. Die Befehle wurden hier nicht ausgeführt. [tweet-2100962426439000484](../sources/tweet-2100962426439000484.md)

bin/jev-codex-router smoke prüft die laufende Integration; bin/jev-codex-router report --days 7 zeigt Entscheidungen und Nutzung. Fehlendes Jev oder ein Providerfehler nutzt laut aktuellem README Astra/medium; die Datei ~/.codex/codex-router/jev-router.off ist der manuelle Bypass. [tweet-2100962426439000484](../sources/tweet-2100962426439000484.md)

## Messgrenzen und Kontext (Stand 2026-09)

Das README bezeichnet rund 60 Prozent Ersparnis auf 237 historischen Turns als Simulation einer alten Policy, nicht als gemessene Codex-Kontingentersparnis. Aktuelle Credit-Berichte rechnen beobachtete Token mit veröffentlichten Raten gegen Gegenannahmen; Aufgabenqualität und tatsächliche Kontingentabbuchungen sind damit nicht belegt. [tweet-2100962426439000484](../sources/tweet-2100962426439000484.md)

Der Router soll den vollständigen Kontext weiterreichen, auch bei Modellwechseln. [Prompt Caching](../concepts/Prompt%20Caching.md) bleibt modellbezogen; ein Wechsel kann zusätzlichen Input verursachen. Das README nennt bei beobachteten Wechseln etwa ein Fünftel Cache-Reuse, begrenzt auf diese Messung; Leiva lässt Cache- und Kontexteffekte ausdrücklich offen. [tweet-2100962426439000484](../sources/tweet-2100962426439000484.md)
