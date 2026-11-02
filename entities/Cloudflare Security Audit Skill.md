---
tags: [security, agents, tools]
sources: [tweet-2112973191157252103.md, tweet-2112623636905591040.md]
created: 2026-10-23
updated: 2026-11-01
---

# Cloudflare Security Audit Skill

## Überblick (Stand 2026-10)

Das Repository cloudflare/security-audit-skill ist ein Skill für Coding-Agents, der den Agent zum Sicherheitsprüfer macht. Er lenkt isolierte Agents durch Aufklärung, abdeckungsgeführte Suche, Kandidatenprüfung, strukturierte Ausgabe, unabhängige Verifikation und neutrale Berichte. Laut README ist er der Ausgangspunkt von Cloudflares Harness zur Schwachstellensuche (Blogartikel "Build your own vulnerability harness"). [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)

Juraj Bednar empfiehlt, den Skill auf jeder Software auszuführen, auch mit kostenlosen Modellen und zusätzlich zu einem Modell-Audit; er finde deutlich mehr. Das ist eine persönliche Empfehlung ohne Messwerte. [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)

## Sechs Phasen

1. Aufklärung: Architektur, Vertrauensgrenzen, Eingabeflächen und Abdeckung in architecture.md und coverage-ledger.json. [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)
2. Abdeckungsgeführte Suche: isolierte Hunter je Ledger-Einheit, Kritiker suchen Lücken. [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)
3. Kandidatenprüfung: Jeder Kandidat geht an einen frischen Prüfer, der ihn zu widerlegen versucht. [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)
4. Strukturierte Ausgabe: Verdikte confirmed, needs_validation und rejected in findings.json, geprüft gegen report-schema.json. [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)
5. Unabhängige Verifikation der Quellenangaben durch frische Agents. [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)
6. Neutraler Bericht: REPORT.md, FINDINGS-DETAIL.md und NEEDS-VALIDATION.md. [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)

Die Validatoren validate-coverage-ledger.cjs und validate-findings.cjs sind ohne Abhängigkeiten und laufen nach Ledger-Änderungen beziehungsweise in Phase 4 und 5. Wiederholte Läufe auf demselben Repository sind additiv. [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)

## Nutzung und Voraussetzungen

Installation über die Skills CLI: npx skills add https://github.com/cloudflare/security-audit-skill --skill security-audit (mit --global für Nutzerebene). Aktivierung durch Anfragen wie "security audit this codebase". Ohne Ausgabeordner schreibt der Vollmodus nach ~/security-audit-skill/<repo-name>/run-<N>. [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)

Voraussetzungen: ein Agent mit Tool-Nutzung und parallelen Subagents, Node.js für die Validatoren und eine vom Betriebssystem erzwungene Sandbox für Ziel-Code (ohne Netz, bereinigte Umgebung, Ressourcenlimits). Ohne Sandbox bleibt ein Lead als needs_validation, statt Ziel-Code auszuführen. [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)

Designprinzipien laut README: nur belegte Grenzverletzungen bestätigen, adversariale Validierung (Prüfer ist nie der Finder) und Schweregrad nur mit Auswirkung. [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)

## Evidenzgrenze

Alles stammt aus der gespeicherten README und dem Empfehlungspost. Der Skill wurde hier nicht ausgeführt; Trefferquote und Aussagen wie "findet viel mehr" sind unbelegt. Verwandt: [Claude Code Security Hardening](../concepts/Claude%20Code%20Security%20Hardening.md) (Absicherung von Claude Code selbst, nicht Code-Audit). [tweet-2112973191157252103](../sources/tweet-2112973191157252103.md)

## Nachbarwerkzeuge (Stand 2026-10)

Ein Sammelpost empfiehlt den Skill zusammen mit zwei weiteren Open-Source-Werkzeugen: [SkillSpector](SkillSpector.md) prüft fremde Agent-Skills vor der Installation, [Strix](Strix.md) führt Pentests gegen laufende Anwendungen aus. Die drei decken unterschiedliche Stufen ab (Code-Audit, Skill-Prüfung, dynamischer Test); der Post belegt keinen gemeinsamen Einsatz. [tweet-2112623636905591040](../sources/tweet-2112623636905591040.md)
