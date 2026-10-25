---
tags: [agents, tools]
sources: [tweet-2088742864310481025.md]
created: 2026-10-12
updated: 2026-10-12
---

# Unlazy

## Zweck und Belegstand (Stand 2026-08; gespeicherte v2-README)

[Leonxlnx/unlazy](https://github.com/Leonxlnx/unlazy) ist ein Anti-Laziness-Skill für Coding-Agenten. Der August-Post berichtet Tests mit Opus 5 und empfiehlt die Kombination mit [Ponytail](Ponytail.md); die gespeicherte README beschreibt v2 und darf nicht als identischer historischer Release-Stand behandelt werden. [tweet-2088742864310481025](../sources/tweet-2088742864310481025.md)

## Mechanismus

GATES.md beziehungsweise gates/*.md halten Abschlusskriterien mit CHECK, EXPECT und EVIDENCE fest. gate-check.mjs führt die Prüfkommandos aus und markiert Kriterien nur bei passender Ausgabe als erfüllt; ein Häkchen mit pending-Evidenz gilt weiterhin als offen. [tweet-2088742864310481025](../sources/tweet-2088742864310481025.md)

Depth Tree zerlegt Arbeit an natürlichen Grenzen. Größere Aufgaben erhalten vor paralleler Arbeit einen PLAN.md-Vertrag für Schnittstellen und Dateizuständigkeiten, eigene Gate-Dateien pro Teil und Integrationsprüfungen an den übergeordneten Knoten. Der Parent prüft die Leaf-Ergebnisse erneut statt Selbstbestätigung zu übernehmen. [tweet-2088742864310481025](../sources/tweet-2088742864310481025.md)

## Nutzung und Grenzen

Die README bietet npx skills add Leonxlnx/unlazy, manuelle Installation und /unlazy tree N als Aufruf; Markdown und Node-Skripte werden als agentenübergreifend beschrieben. Ein optionaler Stop-Hook verhindert offenen Abschluss nur in [Claude Code](Claude%20Code.md), gibt nach sechs blockierten Stopps ohne Gate-Fortschritt frei und respektiert einen begründeten ABANDON-Eintrag. [tweet-2088742864310481025](../sources/tweet-2088742864310481025.md)

Der Hersteller verwirft die frühere mathematische Aufwand-Multiplikation mit der Baumtiefe ausdrücklich: Tiefe beschreibt Zerlegung, keinen garantierten Compute-Faktor. Seine zwei kontrollierten Bauaufgaben und berichteten Aufwand-/Fehlerzahlen sind Eigenmessungen, kein unabhängiger Wirksamkeitsnachweis; die Ponytail-Kombination bleibt persönliche Erfahrung. [tweet-2088742864310481025](../sources/tweet-2088742864310481025.md)

[Agentic Engineering](../concepts/Agentic%20Engineering.md) ordnet den Ablauf als Abschlussprüfung gegen reale Belege ein. [tweet-2088742864310481025](../sources/tweet-2088742864310481025.md)
