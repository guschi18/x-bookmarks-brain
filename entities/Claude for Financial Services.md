---
tags: [agents, tools, research]
sources: [tweet-2051679629488865498.md]
created: 2026-10-15
updated: 2026-10-15
---

# Claude for Financial Services

## Ankündigung (Stand 2026-05)

Der offizielle Post vom 05.05.2026 kündigt Finanzagenten für Pitch-Erstellung, Bewertungsprüfung, Monatsabschluss und weitere Aufgaben an. Er nennt Plugins in [Claude Cowork](Claude%20Cowork.md) und [Claude Code](Claude%20Code.md) sowie Cookbooks für Managed Agents. Der Raw-Datensatz enthält keinen aufgelösten externen Artikellink; das gespeicherte Videotranskript enthält nur „Thanks for watching!“. Die Implementierungsdetails unten stammen deshalb aus einer getrennten Primärrecherche. [tweet-2051679629488865498](../sources/tweet-2051679629488865498.md)

## Originalimplementierung (ergänzend geprüft 2026-10-15)

Das [offizielle Repository](https://github.com/anthropics/financial-services/tree/574ed3624aebd0418c7e96cd101262f30210ab26) enthält Agent-Plugins, Fachpakete und Managed-Agent-Cookbooks. Geprüfter Dateistand ist Commit 574ed3624aebd0418c7e96cd101262f30210ab26; acht abgerufene Originaldateien sind im Recherchebericht unter output/finance-agents-2026-10-15-primary.json gesichert. Dieser spätere Stand ist keine Rückdatierung sämtlicher Funktionen auf den Mai-Post. [tweet-2051679629488865498](../sources/tweet-2051679629488865498.md)

Die [README](https://github.com/anthropics/financial-services/blob/574ed3624aebd0418c7e96cd101262f30210ab26/README.md) nennt zehn Agenten: Pitch Agent und Meeting Prep Agent für Kundenarbeit; Market Researcher, Earnings Reviewer und Model Builder für Research und Modelle; Valuation Reviewer, GL Reconciler, Month-End Closer und Statement Auditor für Bewertungen und Finanzbetrieb; KYC Screener für Onboarding. Eigenständige Fachpakete bündeln darunterliegende Skills, Commands und Datenanschlüsse. Die Lizenz ist Apache 2.0. [tweet-2051679629488865498](../sources/tweet-2051679629488865498.md)

## Installation und Fach-Skills (ergänzend geprüft 2026-10-15)

Die [Installation](https://github.com/anthropics/financial-services/blob/574ed3624aebd0418c7e96cd101262f30210ab26/README.md#getting-started) beginnt in Claude Code mit dem Marketplace und dem Fachpaket financial-analysis; einzelne Agenten werden nach Bedarf ergänzt. In Cowork lässt sich die Repository-URL über Settings → Plugins → Add plugin hinzufügen. Die folgenden dokumentierten Befehle wurden hier nicht ausgeführt. [tweet-2051679629488865498](../sources/tweet-2051679629488865498.md)

```sh
claude plugin marketplace add anthropics/financial-services
claude plugin install financial-analysis@claude-for-financial-services
claude plugin install market-researcher@claude-for-financial-services
```

financial-analysis enthält laut README unter anderem /comps, /dcf, /lbo, /3-statement-model und /debug-model sowie Datenanschlüsse; equity-research ergänzt etwa /earnings, /model-update, /sector, /thesis und /catalysts. Die Dateien lassen sich an eigene Datenquellen, Modellkonventionen und Ausgabevorlagen anpassen. Das beschreibt dokumentierte Arbeitsmittel, keine geprüfte Ergebnisqualität. [tweet-2051679629488865498](../sources/tweet-2051679629488865498.md)

Der [DCF-Skill](https://github.com/anthropics/financial-services/blob/574ed3624aebd0418c7e96cd101262f30210ab26/plugins/vertical-plugins/financial-analysis/skills/dcf-model/SKILL.md) verlangt unter anderem lebende Formeln für abgeleitete Werte, Quellenkommentare an Eingabezellen, Bear-/Base-/Bull-Szenarien, Sensitivitätstabellen und schrittweise Nutzerprüfung. Er unterscheidet eine aktive Excel-Sitzung von einer separat erzeugten XLSX-Datei. Diese Vorgaben wurden weder praktisch getestet noch fachlich oder rechnerisch abgenommen. [tweet-2051679629488865498](../sources/tweet-2051679629488865498.md)

## Beispiel: Market Researcher (ergänzend geprüft 2026-10-15)

Die [Agentenbeschreibung](https://github.com/anthropics/financial-services/blob/574ed3624aebd0418c7e96cd101262f30210ab26/plugins/agent-plugins/market-researcher/agents/market-researcher.md) führt von Sektor oder Thema über Branchenüberblick und Wettbewerbslandschaft zu Peer-Multiples, einer Ideenliste und einer Research-Notiz; Folien sind optional. Zahlen sollen aus Datenanbietern oder Filings belegt und andernfalls als UNSOURCED markiert werden. Nach Peer-Vergleich und Entwurf sind menschliche Prüfpunkte vorgesehen; Veröffentlichung und Verteilung erfolgen außerhalb des Agenten. [tweet-2051679629488865498](../sources/tweet-2051679629488865498.md)

Das [Cookbook](https://github.com/anthropics/financial-services/blob/574ed3624aebd0418c7e96cd101262f30210ab26/managed-agent-cookbooks/market-researcher/README.md) erwartet Anthropic-API-Zugang und CapIQ-/FactSet-Endpunkte. Es trennt einen Dokumentleser ohne MCP-Zugang, Datenanalyse mit lesenden Connectors und einen Ausgabeschreiber ohne Connectors. Das [Manifest](https://github.com/anthropics/financial-services/blob/574ed3624aebd0418c7e96cd101262f30210ab26/managed-agent-cookbooks/market-researcher/agent.yaml) bindet die Endpunkte explizit ein und nennt claude-opus-4-7 als Vorlagenmodell; dies ist keine aktuelle Modellwahlempfehlung. [tweet-2051679629488865498](../sources/tweet-2051679629488865498.md)

## Betrieb und Grenzen (ergänzend geprüft 2026-10-15)

Die [Cookbook-Übersicht](https://github.com/anthropics/financial-services/blob/574ed3624aebd0418c7e96cd101262f30210ab26/managed-agent-cookbooks/README.md) beschreibt Manifeste, die dieselben Systemanweisungen und Skills wie die Plugins referenzieren. Ein Deploy-Skript lädt Skills hoch und erstellt Agenten; agentenübergreifende Übergaben laufen über eine eigene Orchestrierung. callable_agents ist als Research Preview auf eine Delegationsebene begrenzt. Ein produktiver End-to-End-Betrieb wurde hier nicht erprobt. [tweet-2051679629488865498](../sources/tweet-2051679629488865498.md)

Die README weist darauf hin, dass Anbieterzugänge eigene Abonnements oder Schlüssel erfordern können. Die Vorlagen müssen an Daten, Risikoregeln und Freigabeprozesse angepasst werden. Der [Month-End Closer](https://github.com/anthropics/financial-services/blob/574ed3624aebd0418c7e96cd101262f30210ab26/plugins/agent-plugins/month-end-closer/agents/month-end-closer.md) entwirft Buchungen, bucht aber nicht selbst ins Hauptbuch; der [Valuation Reviewer](https://github.com/anthropics/financial-services/blob/574ed3624aebd0418c7e96cd101262f30210ab26/plugins/agent-plugins/valuation-reviewer/agents/valuation-reviewer.md) bereitet Berichte vor, verteilt sie jedoch nicht selbst. Dokumentierte Sicherheits- und Prüfanweisungen sind kein Nachweis ihrer Wirksamkeit. [tweet-2051679629488865498](../sources/tweet-2051679629488865498.md)
