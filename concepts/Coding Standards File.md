---
tags: [agents, product-building]
sources: [tweet-2103748049906397613.md, tweet-2105367927394615364.md, tweet-2107062474914550098.md, tweet-2090744569960824949.md]
created: 2026-10-03
updated: 2026-10-12
---

# Coding Standards File

## Definition

Eine [Coding Standards File](Coding%20Standards%20File.md) (CODING_STANDARDS.md) sammelt laut Matt Pocock jeden bedeutsamen Fehler, den ein Coding-Agent macht, als künftige Regel; bei richtiger Nutzung bleibe sie nur etwa fünf Minuten leer. [tweet-2103748049906397613](../sources/tweet-2103748049906397613.md)

## Beispiele und Pflege

Genannt werden vergessener Dark Mode, eine fehlende Validierungsregel und ein falsches Framework-Primitive. Gefüllt wird sie per /retro oder von Hand. [tweet-2103748049906397613](../sources/tweet-2103748049906397613.md)

## Grenze

Der Post ist eine Arbeitsempfehlung ohne Vorlage oder Wirkungsmessung; Inhalt und Code des /retro-Skills sind nicht gespeichert. [tweet-2103748049906397613](../sources/tweet-2103748049906397613.md)

Verwandt: [Matt Pocock Skills](../entities/Matt%20Pocock%20Skills.md).

## Lessons als konkrete Pflegevorlage (Stand 2026-09)

Die Voxyz-AGENTS.md ergänzt eine vollständig sichtbare Lessons-Regel: Nach einer Nutzerkorrektur When X, do Y notieren; bei derselben Wiederholung die unklare Regel neu schreiben, neue Lessons oben eintragen und überholte entfernen. Der restliche Vertrag soll nur nach Nachfrage verändert werden. Der vollständige Wortlaut steht in der Source, die sechs Abschnitte sind unter [Context Engineering](Context%20Engineering.md) eingeordnet. [tweet-2105367927394615364](../sources/tweet-2105367927394615364.md)

## Fehler aus realen Sitzungen ableiten (Stand 2026-10)

Das v1.3-Tutorial von [Matt Pocock Skills](../entities/Matt%20Pocock%20Skills.md) ergänzt den kurzen September-Post um /retro: reale Agentensitzungen lesen, wiederkehrende Probleme in Navigation, Prüfungen, Kontext oder Werkzeugkosten finden und passende Repo-/Skill-Regeln vorschlagen. Der Nutzer priorisiert die Vorschläge; Pocock warnt vor automatischen Fix-Schleifen mit Fehlalarmen. Das Video belegt den beschriebenen Ablauf, nicht dessen allgemeine Wirksamkeit. [tweet-2107062474914550098](../sources/tweet-2107062474914550098.md)

## Aktuelle Präzisierung durch /retro (Stand 2026-10)

Der auf Nutzerwunsch am 12.10.2026 ergänzend geprüfte [aktuelle /retro-Skill](https://github.com/mattpocock/skills/blob/49dd158d1076134a641b33efb035946536778336/skills/engineering/retro/SKILL.md) präzisiert die oben wiedergegebene September-Empfehlung: Mechanische Verstöße gehören in deterministische Lint-, Hook- oder CI-Prüfungen; CODING_STANDARDS.md bleibt echten Ermessensfragen vorbehalten. Vor neuen Checks werden vorhandene Repo-Checks und ihre tatsächliche Ausführung geprüft. [tweet-2090744569960824949](../sources/tweet-2090744569960824949.md)
