---
tags: [agents, tools, product-building]
sources: [tweet-2054255152555545079.md, tweet-2077826623320023303.md, tweet-2097178140413972948.md, tweet-2097369738968195513.md, tweet-2096675504229138541.md, tweet-2097242863964958760.md, tweet-2097742952013656260.md, tweet-2103920741481848861.md, tweet-2103901384135295088.md, tweet-2103552376380457454.md, tweet-2103190313624039620.md, tweet-2102377493705740417.md, tweet-2102436540488315361.md, tweet-2052306848221680015.md, tweet-2102061534956662818.md]
created: 2026-09-29
updated: 2026-10-25
---

# AI Coding Cost Claims

## Behauptungen

Der Post und der verlinkte Artikel behaupten hohe Einsparungen durch gezielte Kontextauswahl, Prompt-Caching und Modellrouting. Die genannten Dollarbeträge und Prozentsätze sind Autorenangaben ohne hier dokumentierte Messmethode. [tweet-2054255152555545079](../sources/tweet-2054255152555545079.md)

## Beleggrenze

Das gespeicherte Videotranskript enthält eine allgemeine Einführung von Andrej Karpathy in Sprachmodelle und Anwendungen. Es stützt die im Post Karpathy zugeschriebene Zahl von 90 Prozent Kontextkosten nicht. Der Videoinhalt und die Kostenbehauptungen sollten daher getrennt gelesen werden. [tweet-2054255152555545079](../sources/tweet-2054255152555545079.md)

## Delegierte Ausführung (Stand 2026-07)

Die [Kimi First](../entities/Kimi%20First.md)-README behauptet eine günstige Ausführung über Flat-Rate-Mitgliedschaft und getrennte Rollen. Sie liefert weder Kosten pro akzeptierter Änderung noch Benchmark-/Preisbelege für Kimi 3, Opus und Sonnet 5. Der Rollenvertrag ist belegt, die pauschale Überlegenheit aus dem Post nicht. [tweet-2077826623320023303](../sources/tweet-2077826623320023303.md)

## Weitere Sparbehauptungen (Stand 2026-09)

Ein chinesischer Post berichtet 90 Prozent weniger Tokenverbrauch beim Lesen großer Dateien durch Hook-Sperre und günstige Worker; die Methode ist in den Posts nicht dokumentiert; der nachgereichte Spotify-Artikel nennt Java-Monorepo-Benchmarks in vier Szenarien ohne Ausgangswert und Stichprobe, Details bei [Hook-Enforced Model Routing](Hook-Enforced%20Model%20Routing.md). [tweet-2097178140413972948](../sources/tweet-2097178140413972948.md)

Die Anthropic-Messungen zu Prompt-Cache, Anti-Mustern und Effort (14,6 Prozent weniger Kosten nach prompt-audit, 52 bis 73 Prozent mit cost-optimize) stammen vom Hersteller auf ausgewählten Benchmarks; siehe [Claude API Skill](../entities/Claude%20API%20Skill.md) und [Instruction Debt Audit](Instruction%20Debt%20Audit.md). [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

Der Codex-Tipp `context_management = true` gegen hohen Astra-Limitverbrauch kommt ohne Messung. [tweet-2096675504229138541](../sources/tweet-2096675504229138541.md)

## Weitere Kostenbehauptungen (Stand 2026-09)

- Ein Autor misst für eine mit [Claude Code](../entities/Claude%20Code.md) gebaute App 10,4 Mio. Tokens und 9,21 Dollar auf Supabase gegen 3,7 Mio. und 2,81 Dollar auf [InsForge](../entities/InsForge.md); ein Lauf je Seite, unterschiedliche Prompts, werbender Autor. [tweet-2097242863964958760](../sources/tweet-2097242863964958760.md)
- [Straitly](../entities/Straitly.md) versprach (Stand 2026-09-09; die Startseite nennt am 2026-10-08 keinen Cashback mehr) 5 bis 10 Prozent Cashback und bis 25 Prozent Ersparnis gegenüber anderen Routern; der Post stellt Cashback gegen Kaufgebühren, das Video nennt bis 20 Prozent. [tweet-2097742952013656260](../sources/tweet-2097742952013656260.md)

## Jev-basierte Kostenangaben (Stand 2026-09)

- [Jevgrep](../entities/Jevgrep.md): Der Post nennt 40 Prozent geringere Kosten, die README ~30 Prozent bei gleichen 8 von 10 SWE-bench-Aufgaben; Widerspruch zwischen beiden Angaben, nur zehn Aufgaben. [tweet-2103920741481848861](../sources/tweet-2103920741481848861.md)
- Der TypeSafe-Skill für [Jev](../entities/Jev.md) nennt eine 12,2-fache Kostensenkung bei 13 in einem Call gebündelten Fragen, gemessen im eigenen Cookbook des Anbieters. [tweet-2103901384135295088](../sources/tweet-2103901384135295088.md)

## Opus-5.5- und Jev-Harness-Angaben (Stand 2026-09)

- [Claude Opus 5.5](../entities/Claude%20Opus%205.5.md): Anthropic nennt 20 Prozent niedrigere Input-/Output-Preise und 60 Prozent niedrigere Cache-Read-Preise als Opus 5. [tweet-2103552376380457454](../sources/tweet-2103552376380457454.md) Die Angabe "40 Prozent günstiger" ist laut Artikel eine Schätzung für typische Workloads bei Default-Einstellungen, kein Preisnachlass je Token. [tweet-2103552376380457454](../sources/tweet-2103552376380457454.md) [tweet-2102436540488315361](../sources/tweet-2102436540488315361.md)
- Ein Nutzer meldet etwa 80 Prozent weniger Kosten und Zeit mit Jev plus Opus 5.5, ohne Messaufbau im Post. [tweet-2103190313624039620](../sources/tweet-2103190313624039620.md)
- Ein PDF-Teaser verspricht 200-fach schnellere und 400-fach günstigere Coding-Agenten; der Artikel selbst belegt nur Preisvergleiche und das 12,2-fache Cookbook-Ergebnis für gebündelte Fragen. [tweet-2102377493705740417](../sources/tweet-2102377493705740417.md)

## Lokale Nutzungsauswertung (Stand 2026-05; gespeicherte README)

[CodeBurn](../entities/CodeBurn.md) dokumentiert eine Auswertung vorhandener Sessiondaten nach Modell, Projekt und Kontext statt einer pauschalen Sparquote. Seine API-äquivalenten Dollarwerte sind keine Abo-Rechnungen; ein Teil der Usage und Optimierungshinweise wird geschätzt oder modelliert. Vergleiche brauchen dieselbe Datengrundlage und müssen die jeweilige Metrikherkunft berücksichtigen. Das Tool wurde hier nicht ausgeführt. [tweet-2052306848221680015](../sources/tweet-2052306848221680015.md)

## AgentRun-Compliance-Beispiel (Stand 2026-09; Repo-Nachtrag 2026-10-25)

[AgentRun](../entities/AgentRun.md) zeigt einen Autorenchart von 2,95 auf 0,25 USD pro Alert über rund 1.000 Alerts; der Post rechnet auf 100.000 Alerts hoch. Weder die beiden fehlenden Originaltexte noch die geskripteten Demos der separat geprüften README belegen einen reproduzierbaren Live-Vergleich bei gleicher Entscheidungsqualität. Die 90-Prozent-Angabe bleibt eine begrenzte Autorenbehauptung. [tweet-2102061534956662818](../sources/tweet-2102061534956662818.md)
