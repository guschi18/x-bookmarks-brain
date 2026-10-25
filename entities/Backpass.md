---
tags: [agents, tools]
sources: [tweet-2104241432467067343.md]
created: 2026-10-06
updated: 2026-10-06
---

# Backpass

## Werkzeug und Einstieg (Stand 2026-09)

[Backpass](https://github.com/kunchenguid/backpass) analysiert laut README tatsächliche Agentensitzungen und schlägt begrenzte Änderungen an AGENTS.md, CLAUDE.md und Skills vor. Voraussetzung sind Node ab 22.5 und acpx; Modellaufrufe verwenden einen bereits authentifizierten Harness. [tweet-2104241432467067343](../sources/tweet-2104241432467067343.md)

Im Projekt: npx backpass, backpass init, backpass zur Analyse und backpass apply zur Auswahl und Übernahme. Analyse verändert die Zieldateien nicht; Synthese editiert eine Staging-Kopie. --scope user und --target grenzen andere beziehungsweise einzelne Instruktionsbereiche ein. [tweet-2104241432467067343](../sources/tweet-2104241432467067343.md)

## Evidenz und Budget (Stand 2026-09)

Die dokumentierte Kette sammelt lokale oder eigene SSH-Sitzungen, verdichtet Transkripte, bewertet Regeln und wiederkehrende Lücken und erzeugt Änderungen. Add, Rewrite und Remove benötigen Zitate aus mindestens zwei verschiedenen Sitzungen; Entfernung verlangt Schadensbelege, bloße Nichtbefolgung unterstützt Verstärkung. [tweet-2104241432467067343](../sources/tweet-2104241432467067343.md)

Das Defaultbudget beträgt 5.000 geschätzte Tokens für stets geladene Memory-Dateien plus Skill-Beschreibungen. Eng bedingte Verfahren können in Skills wandern; deren Inhalt wird erst bei Bedarf geladen. Extract und Move erhalten den entfernten Inhalt und haben andere Evidenzanforderungen. [tweet-2104241432467067343](../sources/tweet-2104241432467067343.md)

Apply zeigt Diff, Belegzitate und Budget; Auswahl kann akzeptieren oder ablehnen. Fingerprints verweigern veraltete Vorschläge, und inkompatible Auswahl schreibt nichts. Abgelehnte Vorschläge werden gespeichert, bis stärkere Evidenz vorliegt. [tweet-2104241432467067343](../sources/tweet-2104241432467067343.md)

## Fallstudie und Grenzen (Stand 2026-09)

Kun Chen berichtet über 100 Firstmate-Sitzungen, zwei abgelehnte Vorschläge, 48 Prozent weniger Tokens und private Regressionsevaluierung. Die gespeicherte PR-Historie zu #5872 zeigt ausgelagerte situative Verträge und danach korrigierte Skill-Trigger sowie inline belassene Regeln. Der private Eval-Satz und vollständige Vorschlagskarten sind nicht gespeichert. [tweet-2104241432467067343](../sources/tweet-2104241432467067343.md)

Das README nennt kausale Zuschreibung durch Modelle ausdrücklich als schwierig und warnt vor sich ändernden Transkriptformaten. Eigene Ausführung und Einsparung wurden nicht geprüft. Im Unterschied zu [AutoHarness](AutoHarness.md) trainiert Backpass ausdrücklich vorhandene Instruktionsdateien und verlangt menschliche Übernahme; das verbindet [Session History Review](../concepts/Session%20History%20Review.md) und [Context Engineering](../concepts/Context%20Engineering.md). [tweet-2104241432467067343](../sources/tweet-2104241432467067343.md)
