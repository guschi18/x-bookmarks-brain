---
tags: [agents, tools]
sources: [tweet-2093370341418582346.md]
created: 2026-10-10
updated: 2026-10-10
---

# Skill Doctor

## Zweck und gespeicherte Evidenz (Stand 2026-08)

Skill Doctor wird als Skill angekündigt, der vergangene Gespräche aus [Claude Code](Claude%20Code.md), [Codex](Codex.md) oder Warp einsammelt, Effizienz und Codequalität bewertet und konkrete Skill-Diffs vorschlägt. Der gespeicherte Website-Ausschnitt enthält hauptsächlich Werbung für Warp Factories; das Raw-Videotranskript ist leer. [tweet-2093370341418582346](../sources/tweet-2093370341418582346.md)

Bei der Triage wurden Frames des Demo-Videos geprüft: Sie zeigen einen Agent Skill Report mit zwölf Gesprächen, sechzehn installierten und dreizehn verwendeten Skills sowie konkrete Vorschläge gegen wiederholte Dev-Server-Starts, übergangene Auth-Fehler und übersehene UI-Regressionen. Das sind sichtbare Demo-Inhalte, keine hier reproduzierten Ergebnisse. [tweet-2093370341418582346](../sources/tweet-2093370341418582346.md)

## Primärquellen-Nachtrag (Stand 2026-10-10)

Die ergänzend gelesene [offizielle Seite](https://www.warp.dev/skill-doctor) verlinkt [warpdotdev/common-skills](https://github.com/warpdotdev/common-skills/blob/main/.agents/skills/skill-doctor/SKILL.md). Der separat unter output/skill-doctor-upstream-2026-10-10.md gesicherte aktuelle Skill beschreibt Scope-Auswahl, einen lokalen Collector und Rubriken für Effizienz, Codequalität, Prozedurtreue und Ausführlichkeit; Default sind 45 Tage Rückblick und höchstens zwölf Gespräche. Diese Angaben sind ein späterer Primärquellenstand, kein Inhalt des gespeicherten Website-Fragments. [tweet-2093370341418582346](../sources/tweet-2093370341418582346.md)

Er schlägt Änderungen nur aus fehlgeschlagenen bewertbaren Gesprächsteilen vor; ohne Codeänderungen bleibt Codequalität insufficient_evidence. Qualitative Scores werden für den Bericht angehoben, weshalb Buchstabennoten keine unabhängige Wirksamkeitsmessung darstellen. Das Werkzeug ergänzt [Instruction Debt Audit](../concepts/Instruction%20Debt%20Audit.md) um Gesprächsbelege statt alleiniger Instruktionsprüfung. [tweet-2093370341418582346](../sources/tweet-2093370341418582346.md)

## Grenzen

Der aktuelle Skill verlangt lokale Verarbeitung und verbietet Uploads der Transkripte; nur ein bewusst gewählter Bericht darf geteilt werden. Die Installation, der Collector und die Änderungen wurden nicht ausgeführt. Warp-Factories-Werbeaussagen sind vom eigenständigen Skill zu unterscheiden. [tweet-2093370341418582346](../sources/tweet-2093370341418582346.md)
