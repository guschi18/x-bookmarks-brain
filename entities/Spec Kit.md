---
tags: [agents, tools, product-building]
sources: [tweet-2052753384503922855.md, tweet-2114486060730237224.md]
created: 2026-10-14
updated: 2026-10-27
---

# Spec Kit

## Projekt und Quellenstand (Stand 2026-05; später erfasste README)

[github/spec-kit](https://github.com/github/spec-kit) ist laut gespeicherter README ein Open-Source-Toolkit für strukturierte Agentenprozesse, Vorlagen und dokumentierte Ergebnisse. Der Bookmark vom 08.05.2026 verlinkt das Repository; die später erfasste README darf nicht vollständig auf das Tweetdatum zurückdatiert werden. [tweet-2052753384503922855](../sources/tweet-2052753384503922855.md)

## Einstieg und Feature-Ablauf (gespeicherter README-Stand)

Die README nennt Python 3.11+, uv und einen unterstützten Coding-Agenten unter Linux, macOS oder Windows. Ihr CLI-Beispiel lautet `uv tool install specify-cli`, danach `specify init my-project --integration copilot` und `cd my-project`; der Integrationsschlüssel richtet sich nach dem verwendeten Agenten, etwa [Claude Code](Claude%20Code.md). [tweet-2052753384503922855](../sources/tweet-2052753384503922855.md)

Die Agenten-Skills werden einzeln im Agenten-Chat aufgerufen und ihre Ergebnisse vor dem nächsten Schritt geprüft: einmal pro Projekt `/speckit-constitution`, danach pro Feature `/speckit-specify`, `/speckit-plan`, `/speckit-tasks`, `/speckit-implement` und `/speckit-converge`. Implementierung und Konvergenzprüfung werden wiederholt, bis die Prüfung Konvergenz meldet; zusätzliche Klärung, Checklisten und Konsistenzanalyse sind optional. Aufrufsyntax und verfügbare Befehle hängen vom Integrationsmodus ab. [tweet-2052753384503922855](../sources/tweet-2052753384503922855.md)

## Separate Prozesse (gespeicherter README-Stand)

Bugfixes setzen keinen vorherigen Feature-SDD-Lauf voraus: `specify extension add bug` installiert die optionale Erweiterung; die Agentenfolge assess → fix → test hält Ursache, begrenzte Reparatur und Verifikation getrennt. Berichte liegen unter `.specify/bugs/<slug>/`; mögliche Ergebnisse sind verified, partial oder failed. Fehlende Verifikation gilt nicht als erfolgreicher Fix. [tweet-2052753384503922855](../sources/tweet-2052753384503922855.md)

Die optionale Erweiterung `specify extension add assess` führt Ideen durch intake → research → define → shape → decide. Die Markdown-Artefakte unter `.specify/assessments/<slug>/` enden mit go, needs-clarification oder kill; offene Punkte werden in bestehenden Artefakten geklärt, statt ganze Phasen neu zu erzeugen. Ein go kann anschließend an die Spezifikation übergeben werden. [tweet-2052753384503922855](../sources/tweet-2052753384503922855.md)

## Anpassung und Grenzen

Die README unterscheidet Extensions für zusätzliche Fähigkeiten, Presets für angepasstes Verhalten, Workflows für automatisierte Schritte, Bundles für Rollenpakete und lokale Template-Overrides. Sie nennt MIT als Lizenz. Die Quelle dokumentiert Prozesse; ihre Umsetzung wurde hier weder installiert noch auf Ergebnisqualität getestet. [tweet-2052753384503922855](../sources/tweet-2052753384503922855.md)

Einordnung: Das CMU/Google-Paper nennt Spec Kit unter den SDD-Werkzeugen, deren Repository-Zahl 2025 bis 2026 wächst; Befunde dazu stehen unter [Spec-Driven Development](../concepts/Spec-Driven%20Development.md). [tweet-2114486060730237224](../sources/tweet-2114486060730237224.md)
