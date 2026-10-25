---
tags: [agents, tools, product-building]
sources: [tweet-2092988408050360798.md]
created: 2026-10-10
updated: 2026-10-10
---

# Simplify Codebase

## Zweck und Beweisgrenze (Stand 2026-08)

[tt-a1i/simplify-codebase](https://github.com/tt-a1i/simplify-codebase) ist laut gespeicherter README ein Agent-Skill zum Erkennen und sicheren Entfernen zufälliger Codekomplexität; Ziel ist weniger dauerhaft zu pflegende Zustände, Fakten und Verträge statt möglichst vieler gelöschter Zeilen. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)

Die README verlangt für Kandidaten Verbraucherbelege aus Produktion, Tests, dynamischer Registrierung und externen Schnittstellen sowie einen vollständigen Löschumfang und eine Prüfung, die eine falsche Löschung sichtbar machen würde. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)

Öffentliche APIs, Persistenzformate, Migrationen, Plugins, Berechtigungen, Nebenläufigkeit und Lebenszyklen müssen berücksichtigt werden; bei echten Verbrauchern oder ungeklärten Grenzen soll der Agent behalten oder offene Belege nennen. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)

## Vollständiger Bildprompt als deutsche Übertragung (Stand 2026-08)

1. **Scope:** Auf Grundlage der simplify-codebase-Regeln die aktuelle Codebasis umfassend vereinfachen. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)
2. **Divide:** Aufgaben nach tatsächlichen großen Modulen und Eigentumsgrenzen aufteilen; parallele Unteragenten bearbeiten Teilbereiche, der Hauptagent koordiniert Modulverträge, integriert Änderungen und prüft das Gesamtergebnis. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)
3. **Reduce:** Unnötige Abstraktionen, doppelte Definitionen, redundante Schnittstellen und Zustände, sinnlose Weiterleitung, übermäßige Verallgemeinerung und unwirksame Kompatibilität entfernen; Verantwortlichkeiten, Typen, Interfaces und Datenflüsse sollen direkter und wartbarer werden. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)
4. **Preserve:** Unteragenten dürfen nach Codebefund direkt ändern, müssen aber tatsächliche Aufrufbeziehungen prüfen und gültiges Verhalten und Verträge erhalten; alle Vereinfachungen mit hoher Beweissicherheit ausführen, statt nur einen Auditbericht abzugeben. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)
5. **Verify:** Bestehende Tests, Typprüfung, Lint und Build laufen lassen; tatsächliche Änderungen, Prüfergebnisse und Restgefahren zusammenfassen. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)

Optional empfiehlt das Bild: ein Web-Pro-Modell liest das Repository und erstellt den Bereinigungsplan, [Codex](Codex.md) setzt ihn lokal um und prüft ihn. Das ist ein wiederverwendbarer Arbeitsauftrag, kein gemessener Qualitätsvergleich. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)

## Gespeicherter Repository-Stand und Grenzen (Stand 2026-08; README ohne historischen Commit)

Die gespeicherte README unterscheidet fokussierte und breite Untersuchung sowie reine Survey-Prüfung und Change-Umsetzung; Change soll Prüfergebnisse, Arbeitsbeleg und ausführbaren Rücknahmeweg liefern. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)

Sie enthält einen optionalen Cleanup-Map-Renderer mit Node.js 18+, der schriftliche Beweise begleitet, sie aber nicht ersetzt; Graph-Erreichbarkeit soll nicht als bewiesene Laufzeitwirkung ausgegeben werden. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)

MIT-Lizenz, Repository-Szenarien und ein berichteter Audit eines 973-Dateien-Projekts sind README-Angaben; Wirksamkeit und Sicherheit wurden hier nicht selbst getestet. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)

Die Quelle ergänzt [Agentic Engineering](../concepts/Agentic%20Engineering.md) um einen spezifischen Bereinigungsablauf; [Ponytail](Ponytail.md) ist ein verwandtes, separat dokumentiertes Werkzeug und kein Alias dieses Repositorys. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)
