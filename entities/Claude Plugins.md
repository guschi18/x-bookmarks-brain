---
tags: [agents, tools]
sources: [tweet-2103577007938228300.md, tweet-2106153410697564235.md, tweet-2106143340794454346.md, tweet-2106118517447876618.md, tweet-2098531560643539440.md, tweet-2052331797640515960.md, tweet-2050941624578920535.md, tweet-2037907310136484036.md, tweet-2029697412701282511.md, tweet-2009450715081789767.md, tweet-2114910356170522999.md]
created: 2026-10-03
updated: 2026-10-29
---

# Claude Plugins

## Rolle

[Claude Plugins](Claude%20Plugins.md) bündeln laut Anthropic MCP-Connectoren, Agent Skills oder beides und sind der Hauptweg für Drittanbieter-Erweiterungen; in [Claude Code](Claude%20Code.md) können sie zusätzlich LSPs, Commands, Hooks und Agents enthalten. [tweet-2103577007938228300](../sources/tweet-2103577007938228300.md)

## Einreichung und Betrieb

- Das Portal unter claude.ai/directory/manage/new steht Entwicklern mit bezahltem Plan offen; eingereicht wird ein einzelner Remote-MCP-Server oder ein GitHub-Repo als Bundle. [tweet-2103577007938228300](../sources/tweet-2103577007938228300.md)
- Jede Einreichung wird automatisch validiert und safety-gescannt; Review-Status, Empfehlungen und Veröffentlichungszeitpunkt liegen beim Entwickler. [tweet-2103577007938228300](../sources/tweet-2103577007938228300.md)
- Nach Veröffentlichung zeigen Analytics Installationen nach Produktfläche und Version, Listing-Aufrufe und Suchbegriffe. [tweet-2103577007938228300](../sources/tweet-2103577007938228300.md)

## MCP-Stand

Claude unterstützt laut Artikel MCP 2.0 mit zustandslosem Kern sowie MCP Apps für interaktive UI und Enterprise Managed Auth für OAuth ohne Nutzereingriff. Die 110-fache MCP-Nutzungssteigerung ist eine Herstellerangabe ohne Basiswert. [tweet-2103577007938228300](../sources/tweet-2103577007938228300.md)

## Ausblick

Anthropic kündigte am 2026-09-25 eine gemeinsame Discovery für Claude und Claude Code "in den kommenden Wochen" an; eine Auslieferung ist Stand 2026-10-08 nicht belegt; bestehende Skills, Connectoren und Plugins im Verzeichnis brauchen keine Änderung. [tweet-2103577007938228300](../sources/tweet-2103577007938228300.md)

## Additions (Stand 2026-10)

[Claude Image View](Claude%20Image%20View.md) uses marketplace add, plugin install and reload-plugins to enable image previews in [Claude Code](Claude%20Code.md). [tweet-2106153410697564235](../sources/tweet-2106153410697564235.md)

## Additions (Stand 2026-10)

Nate Herk describes [Claude Code Mods](Claude%20Code%20Mods.md) as code shipped inside plugins and installed through /plugin. His examples add cache/handoff, recording, goal and shared-file controls. [tweet-2106143340794454346](../sources/tweet-2106143340794454346.md)

You Should Know is announced with /plugin enable cc-plugin-you-should-know@builtin; the saved demo has no transcript. [tweet-2106118517447876618](../sources/tweet-2106118517447876618.md)

## Plugin-Evaluierungen (Stand 2026-09)

Thariq empfiehlt `claude plugin eval init` im Pluginordner, um nach Modellwechseln zu prüfen, ob Skills weiterhin funktionieren. Der zitierte ClaudeDevs-Post beschreibt Testfälle, bewertete Ausführungen und einen Vergleich ohne Plugin; das ergänzt die bisherigen Installations- und Portalhinweise. [tweet-2098531560643539440](../sources/tweet-2098531560643539440.md)

Die am 08.10.2026 ergänzend gelesene [Herstellerdokumentation](https://code.claude.com/docs/en/plugin-evals) bestätigt `init`: Fälle und Grader erstellen, Ergebnisse mit und ohne Plugin vergleichen. Sie nennt Claude Code ab v2.1.269 und reale Modellaufrufe auf dem eigenen Account; der dokumentierte Standard wiederholt jeden Fall dreimal pro Arm. Kein Eval wurde hier ausgeführt. [tweet-2098531560643539440](../sources/tweet-2098531560643539440.md)

## Rollenworkflow als Plugin (Stand 2026-05)

Der separat gespeicherte Khairallah-Kurs ergänzt die späteren Portal- und Eval-Hinweise um einen historischen Autorenworkflow: Rollenwissen recherchieren, eigene Qualitätsregeln festhalten, Skill und Command mit Referenzvorlagen bündeln und auf realen Eingaben iterativ prüfen. [Claude Cowork](Claude%20Cowork.md) enthält den vollständigen Rechercheprompt und die Schrittfolge; der Kurs ist nicht Boris Cherny zuzuschreiben. Seine vorgeschlagenen Datei- und Installationswege sind keine hier gegen heutige Produktdokumentation geprüfte Anleitung. [tweet-2052331797640515960](../sources/tweet-2052331797640515960.md)

## Nate Herks Arbeitsablauf und Installationen (Stand 2026-05)

Der vollständig gespeicherte Artikel vom 03.05.2026 kombiniert Werkzeuge für unterschiedliche Aufgaben: Skill Creator wandelt eine Aufgabenbeschreibung oder SOP in einen wiederverwendbaren Skill um; Superpowers strukturiert Planung, Tests und Review; GSD zerlegt Arbeit in frische Aufgabenkontexte. Das ist die Empfehlung des Autors, kein hier getesteter gemeinsamer Stack. [tweet-2050941624578920535](../sources/tweet-2050941624578920535.md)

Historische Installationsbefehle aus dem Artikel, ohne Ausführung oder Prüfung gegen heutige Versionen: [tweet-2050941624578920535](../sources/tweet-2050941624578920535.md)

```text
/plugin install skill-creator@claude-plugins-official
/plugin install superpowers@claude-plugins-official
npx get-shit-done-cc --claude --global
/plugin marketplace add mksglu/context-mode
/plugin install context-mode@context-mode
/plugin marketplace add thedotmack/claude-mem
/plugin install claude-mem
/plugin install frontend-design@claude-plugins-official
```

Nach der GSD-Installation nennt der Autor /gsd-help. Context Mode soll Tool-Ausgaben in einem separaten Prozess filtern und bei Kompaktierung einen Sitzungs-Snapshot aus einer lokalen SQL-Datenbank wiederherstellen; nach dessen Installation verlangt der Artikel einen Neustart von [Claude Code](Claude%20Code.md) und nennt /context-mode:ctx-stats zur Kontrolle. Das sind konkrete Ansatzpunkte für [Context Engineering](../concepts/Context%20Engineering.md), keine Garantie vollständiger Erinnerung. [tweet-2050941624578920535](../sources/tweet-2050941624578920535.md)

Claude Mem beschreibt der Artikel als sitzungsübergreifende Erfassung und verdichtete Wiedergewinnung über SQLite und Vektorsuche, mit kompaktem Suchindex, Zeitlinienkontext und erst danach vollständigen Details. Die Warnung vor npm install betrifft den Unterschied zwischen SDK-Bibliothek und Plugin-Hooks. Die damalige Aussage, alles laufe lokal, gilt hier nur als Beschreibung dieses Artikels und nicht als geprüfte Aussage über spätere Editionen oder optionale Dienste. [tweet-2050941624578920535](../sources/tweet-2050941624578920535.md)

Für Codeprüfung unterscheidet der Artikel /review von dem dort /ultra-review geschriebenen Cloud-Review. Er nennt ab v2.1.86, Claude-Account statt reinem API-Key, 10–20 Minuten und damals drei Pro-/Max-Probeläufe mit später 5–20 Dollar pro Lauf. Diese Angaben bleiben historischer Autorenstand; sie bestätigen weder aktuelle Syntax noch heutigen Preis oder Zugang. Die berichteten Kontext-, Qualitäts- und Laufzeitgewinne wurden nicht unabhängig gemessen. [tweet-2050941624578920535](../sources/tweet-2050941624578920535.md)

Für Dienstleistungen empfiehlt der Autor, mit einem beherrschten Skill und einer konkreten Kundendemo zu beginnen und den Zeit- oder Fehlergewinn statt des technischen Workflows zu verkaufen. [tweet-2050941624578920535](../sources/tweet-2050941624578920535.md)

## Repo-Liste für Claude Code (Stand 2026-03)

Eine Empfehlungsliste vom 28.03.2026 nennt neun Repositories: claude-mem, UI UX Pro Max, n8n-MCP, Obsidian Skills, LightRAG, Everything Claude Code, Superpowers, Awesome Claude Code und GSD. Die Wirkungsbehauptung ("10x") ist unbelegt. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)

- claude-mem (thedotmack/claude-mem): Die README beschreibt ein Speichersystem, das Werkzeugnutzung erfasst, per KI verdichtet und in spätere Sitzungen einspeist. Installation über `/plugin marketplace add thedotmack/claude-mem` und `/plugin install claude-mem` oder `npx claude-mem install`; `npm install -g claude-mem` installiert nur die SDK-Bibliothek, nicht die Hooks. Mit `<private>`-Tags lassen sich Inhalte von der Speicherung ausnehmen. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
- Obsidian Skills (kepano/obsidian-skills): Agent Skills nach der Agent-Skills-Spezifikation für Claude Code, Codex und OpenCode; Installation über `/plugin marketplace add kepano/obsidian-skills` und `/plugin install obsidian@obsidian-skills`. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
- GSD (gsd-build/get-shit-done): Die später gespeicherte README meldet, das Repository sei nicht mehr die aktive Heimat; die Entwicklung laufe als GSD Core im Repository open-gsd/gsd-core weiter. Der Post-Stand 2026-03 nennt noch das alte Repository. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
- Awesome Claude Code (hesreallyhim/awesome-claude-code): kuratierte Sammlung von Skills, Agents, Statuszeilen und Plugins; die gespeicherte Seite nennt 52,8k Sterne. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
- Superpowers (obra/superpowers): agentisches Skill-Framework und Entwicklungsmethodik laut README-Screenshot. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
- Weitere Seiten: [LightRAG](LightRAG.md), [n8n-MCP](n8n-MCP.md), [UI UX Pro Max](UI%20UX%20Pro%20Max.md), [Everything Claude Code](Everything%20Claude%20Code.md). [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)

## Beispiel PM Skills Marketplace (Stand 2026-03)

Ein Drittanbieter-Beispiel ist der [PM Skills Marketplace](PM%20Skills%20Marketplace.md): acht Plugins mit über 100 Produktmanagement-Skills, gebaut für Claude Code und Cowork und laut Autor auch mit Gemini CLI, Cursor, Codex CLI und Kiro nutzbar. [tweet-2029697412701282511](../sources/tweet-2029697412701282511.md)

## code-simplifier-Plugin (Stand 2026-01)

Boris Cherny gibt an, das im Claude-Code-Team genutzte code-simplifier-Agent als Plugin veröffentlicht zu haben. Installation per `claude plugin install code-simplifier` oder in der Sitzung per `/plugin marketplace update claude-plugins-official` und `/plugin install code-simplifier`. [tweet-2009450715081789767](../sources/tweet-2009450715081789767.md) Empfohlener Einsatz laut Post: am Ende einer langen Sitzung oder zum Bereinigen komplexer PRs. [tweet-2009450715081789767](../sources/tweet-2009450715081789767.md) Die Wirkung ist Herstellerangabe und nicht unabhängig geprüft. [tweet-2009450715081789767](../sources/tweet-2009450715081789767.md)

## claude-md-management-Plugin (Stand 2026-10)

Das offizielle Plugin claude-md-management aus dem Marketplace claude-plugins-official prüft CLAUDE.md-Dateien und hält Erkenntnisse aus Sitzungen fest. Installation per `/plugin install claude-md-management@claude-plugins-official`, Erkenntnisse sichert `/revise-claude-md`. [tweet-2114910356170522999](../sources/tweet-2114910356170522999.md) Der enthaltene Skill claude-md-improver arbeitet in fünf Phasen: Dateien finden, nach sechs gewichteten Kriterien bewerten (Noten A bis F), Bericht ausgeben, Ergänzungen als Diff vorschlagen, nach Freigabe anwenden. [tweet-2114910356170522999](../sources/tweet-2114910356170522999.md) Die Empfehlung stammt von einem Drittautor; Wirkung und Qualitätskriterien wurden nicht geprüft, die Referenzdateien fehlen in der Quelle. [tweet-2114910356170522999](../sources/tweet-2114910356170522999.md)
