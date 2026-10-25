---
tags: [agents, tools]
sources: [tweet-2105346502096994602.md]
created: 2026-10-06
updated: 2026-10-06
---

# AutoHarness

## Rolle und Installation (Stand 2026-09)

[AutoHarness](https://github.com/tigerless-labs/autoharness) von Tigerless Labs ist laut README eine selbstlernende Skill-Ebene für [Claude Code](Claude%20Code.md), die reale Sitzungen auswertet und nur die von ihr selbst geschriebenen Skills verändert. Python 3.11+ als python3 im PATH ist Voraussetzung; laut Projekt gibt es keine Drittanbieter-Python-Abhängigkeiten und eine MIT-Lizenz. [tweet-2105346502096994602](../sources/tweet-2105346502096994602.md)

Plugininstallation laut README: /plugin marketplace add tigerless-labs/autoharness, dann /plugin install autoharness@autoharness und /reload-plugins oder Neustart. /learn hält eine Lektion der aktuellen Sitzung über dieselbe Validierungskette fest. Für Updates zuerst den Marketplace aktualisieren, dann das Plugin und Claude Code neu starten. [tweet-2105346502096994602](../sources/tweet-2105346502096994602.md)

## Lern- und Schreibgrenzen (Stand 2026-09)

Die CAP-Stufe erfasst Werkzeugarbeit und verweist auf den Host-Verlauf; REF schlägt neue oder geänderte Skills vor, besitzt aber keine Schreibwerkzeuge. Nur der Promoter prüft Struktur, Evidenz und Selbstautorschaft und schreibt akzeptierte Vorschläge atomar. Ein pro Skill geführtes Ledger und geschwärzte Evidenzauszüge halten den Anlass jeder Änderung fest. [tweet-2105346502096994602](../sources/tweet-2105346502096994602.md)

Standardmäßig löst die Arbeit nach 50 Werkzeugaufrufen eine Reflexion aus; eine seltenere Konsolidierung führt nahe Duplikate zusammen. Der Sitzungsstart zeigt einen gruppierten Index eigener Skills; die native Recall-Mechanik des Hosts bleibt daneben bestehen. Dies verbindet [Session History Review](../concepts/Session%20History%20Review.md) mit dauerhaftem [Context Engineering](../concepts/Context%20Engineering.md). [tweet-2105346502096994602](../sources/tweet-2105346502096994602.md)

## Lebenszyklus und Grenzen (Stand 2026-09)

Loads, bloße Views und Patches werden getrennt erfasst. Während der Bewährungsphase sind Skills nicht archivierungsfähig; danach führt Kapazitätsdruck zur Archivierung der schwächsten Nutzungsraten. Zusammengelegte Skills behalten einen Ledger-Verweis auf das aufnehmende Skill. Archive können wiederhergestellt werden; Deinstallation lässt erzeugte Skills und Zustandsdaten auf der Platte. [tweet-2105346502096994602](../sources/tweet-2105346502096994602.md)

Diese Validierung misst Nutzung und strukturelle Akzeptanz, keinen unabhängigen Aufgabenerfolg. Der zitierte CORE-Bench-Anstieg von 42 auf 78 Prozent stammt aus einem anderen Harness-Vergleich und ist keine AutoHarness-Messung. Defaultschwellen sind laut README noch nicht empirisch kalibriert; automatische Skill-Indizes können Kontext kosten. [tweet-2105346502096994602](../sources/tweet-2105346502096994602.md)

Native Windows-Unterstützung ist nicht belegt: Die Installationsbeschreibung verlangt python3, und die dokumentierten Desktopbenachrichtigungen nennen macOS und Linux. Installation und automatisches Lernen wurden hier nicht ausgeführt. [tweet-2105346502096994602](../sources/tweet-2105346502096994602.md)
