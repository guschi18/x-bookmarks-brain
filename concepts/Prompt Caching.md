---
tags: [llm-training, tools]
sources: [tweet-2060432688281251998.md, tweet-2024574133011673516.md, tweet-2024573404888911886.md, tweet-2058676383912431842.md, tweet-2097369738968195513.md, tweet-2101355584305943031.md, tweet-2101872112977781180.md, tweet-2106455605925822967.md, tweet-2108637982005833973.md]
created: 2026-09-30
updated: 2026-10-12
---

# Prompt Caching

## Ausgangspunkt und Herkunft

Der Post bewirbt zusätzliche Systemanweisungen ohne Cache-Unterbrechung für Opus 4.8; die Modellliste hat sich seither erweitert (siehe Abschnitt unten). Die zwei vom Nutzer ergänzten Hersteller-Docs wurden am 2026-09-30 gelesen und sind als Nachtrag auf der Source verlinkt; ihre Angaben ergänzen den ursprünglichen Post, gehören aber nicht zu dessen Raw-Beleg. [tweet-2060432688281251998](../sources/tweet-2060432688281251998.md)

## Automatic Caching

Laut [Dokumentation](https://platform.claude.com/docs/en/build-with-claude/prompt-caching#automatic-caching) aktiviert ein requestweites cache_control mit type ephemeral automatisches Caching am letzten geeigneten Block; die Grenze wandert mit wachsender Historie. Identische frühere Präfixe werden wiederverwendet. [tweet-2060432688281251998](../sources/tweet-2060432688281251998.md)

Die Standarddauer ist fünf Minuten; ttl 1h ist eine kostenpflichtige Alternative. Mindestlänge, höchstens vier Breakpoints und das 20-Block-Rücksuchfenster gelten weiterhin. Bei einem wechselnden Suffix empfiehlt die Dokumentation einen expliziten Breakpoint am Ende des stabilen Präfixes. [tweet-2060432688281251998](../sources/tweet-2060432688281251998.md)

## Systemanweisungen während der Unterhaltung

Die [zweite Dokumentation](https://platform.claude.com/docs/en/build-with-claude/mid-conversation-system-messages) beschreibt eine zusätzliche Nachricht mit role system im messages-Array statt einer Änderung des obersten system-Felds. Sie wirkt ab ihrer Position; spätere Systeminstruktionen haben bei Konflikten Vorrang. Laut Dokumentation (geprüft 2026-10-08) unterstützen Opus 4.8, Opus 5, Opus 5.5, Fable 5, Fable 5.1, Sonnet 5.5 und Haiku 5.5 diese Funktion; Sonnet 5 nicht (dort bleibt das oberste system-Feld). Der Post nannte nur Opus 4.8. [tweet-2060432688281251998](../sources/tweet-2060432688281251998.md)

Caching muss ausdrücklich aktiviert sein. Frühere Nachrichten unverändert lassen und die neue Instruktion nach dem gecachten Präfix anhängen; bereits gesendete Instruktionen durch weitere Nachrichten ergänzen, statt sie umzuschreiben oder zu löschen. [tweet-2060432688281251998](../sources/tweet-2060432688281251998.md)

## Platzierung und Evidenzgrenze

Die Systemnachricht darf nicht zuerst stehen. Sie folgt einem User-Turn, einschließlich Tool-Ergebnissen, oder einem Assistant-Turn mit abschließendem Server-Tool-Ergebnis und steht vor einem Assistant-Turn oder am Array-Ende. Unvertrauenswürdige externe Inhalte gehören in Tool-Ergebnisse, nicht in Systeminstruktionen. [tweet-2060432688281251998](../sources/tweet-2060432688281251998.md)

Dies sind Herstellerregeln, keine im Wiki gemessenen Einsparungen. [Model Selection Evals](Model%20Selection%20Evals.md) behandelt die aufgabenspezifische Prüfung von Qualität, Kosten und Latenz. [tweet-2060432688281251998](../sources/tweet-2060432688281251998.md)

## Stabiles Präfix als Harness-Vertrag

Thariq beschreibt folgende Reihenfolge für [Claude Code](../entities/Claude%20Code.md): stabile Systemanweisungen und Tools, projektbezogene CLAUDE.md, Sitzungskontext, danach Gesprächsnachrichten. Präzise Zeitstempel, wechselnde Tool-Reihenfolge oder geänderte Tool-Parameter können das gemeinsame Präfix zerstören. [tweet-2024574133011673516](../sources/tweet-2024574133011673516.md)

Aktualisierte Zeit- oder Dateiinformation soll laut Artikel als neue Nachricht beziehungsweise Tool-Ergebnis angehängt werden. Planmodus wird durch Instruktionen und EnterPlanMode/ExitPlanMode modelliert, während die Tools gleich bleiben; Tool Search verwendet stabile defer_loading-Stubs. [tweet-2024574133011673516](../sources/tweet-2024574133011673516.md)

Caches sind modellgebunden: Der Wechsel zu einem günstigeren Modell kann bei langem Kontext wegen eines neu aufzubauenden Caches teurer sein. Der Artikel schlägt stattdessen einen kompakten Handoff an Teilagenten vor; das ist keine gemessene allgemeine Kostenregel. [tweet-2024574133011673516](../sources/tweet-2024574133011673516.md)

## Automatic Caching und Compaction

Lance Martin beschreibt requestweites cache_control mit type ephemeral: Die Grenze wandert zum letzten geeigneten Block, und explizite Blockgrenzen bleiben möglich. Identischer Inhalt wird für Cachetreffer vorausgesetzt; der Artikel nennt eine Rücksuche von höchstens 20 Blöcken. [tweet-2024573404888911886](../sources/tweet-2024573404888911886.md)

Für Compaction beschreibt Thariq einen Fork mit demselben System-, Nutzer-, Tool- und Historienpräfix und einer zusätzlichen Zusammenfassungsanweisung am Ende. Ein reservierter Puffer muss Anweisung und Zusammenfassung noch in das Kontextfenster passen lassen. [tweet-2024574133011673516](../sources/tweet-2024574133011673516.md)

Der Autor berichtet von Alarmen und Incidents bei niedriger Cachetrefferrate; damit wird Caching als Betriebskennzahl statt als einmalige Promptoptimierung behandelt. [tweet-2024574133011673516](../sources/tweet-2024574133011673516.md)

## Grenze des Settings-Artikels

Der separate Sparartikel empfiehlt stabile Inhalte vor dynamischen und berichtet von einer Rechnungssenkung von $340 auf $87. Diese Rechnung und die historischen Preisfaktoren sind nicht unabhängig geprüft. [tweet-2058676383912431842](../sources/tweet-2058676383912431842.md)

Sein pauschal als falsch bezeichnetes Beispiel setzt einen Breakpoint hinter die dynamische User-Nachricht. Daraus folgt nicht, dass ein später Breakpoint keine Wiederverwendung früherer Präfixe erlauben kann: Martins Artikel beschreibt gerade diese Rücksuche und wandernde Grenze. Die Beispielsyntax des Sparartikels ist deshalb als Originalbeleg, nicht als vollständige API-Anleitung zu lesen. [tweet-2058676383912431842](../sources/tweet-2058676383912431842.md) [tweet-2024573404888911886](../sources/tweet-2024573404888911886.md)

## Hersteller-Docs-Abgleich des Sparartikels (Stand 2026-05)

Die [Prompt-Caching-Dokumentation](https://platform.claude.com/docs/en/build-with-claude/prompt-caching) bestätigt identische Präfixe, stabile Inhalte zuerst und explicit cache_control am Contentblock. Im Artikel sitzt cache_control fälschlich direkt auf dem messages-Objekt; für das dort behandelte Modell gehört der Systemprompt in das separate system-Feld, nicht als role system in die Historie. Die oben beschriebene spätere Systemnachrichtenfunktion für Opus 4.8 ist eine andere, ausdrücklich dokumentierte Variante. [tweet-2058676383912431842](../sources/tweet-2058676383912431842.md)

Bei unabhängigen wechselnden Fragen empfiehlt sich der explizite Breakpoint am stabilen System-/Tool-Kontext. Bei wachsender Gesprächshistorie funktioniert ein Breakpoint am letzten geeigneten User-Contentblock beziehungsweise requestweites Automatic Caching: Das Rücksuchfenster findet frühere gespeicherte Präfixe. Ein später Breakpoint ist deshalb nicht grundsätzlich falsch. Modellabhängige Mindestlänge und die gemeldeten cache_creation_input_tokens/ cache_read_input_tokens entscheiden, ob tatsächlich ein Treffer erreicht wird. [tweet-2058676383912431842](../sources/tweet-2058676383912431842.md)

### TTL-abhängige Preise

Die [Preistabelle] (Stand der Quelle 2026-09-30)(https://platform.claude.com/docs/en/about-claude/pricing#prompt-caching) nennt 1,25× Basisinputpreis für fünfminütige Writes, aber 2× für einstündige Writes. Die 25-Prozent-Prämie des Artikels gilt nicht für beide TTLs. Cache-Reads kosten standardmäßig 0,1×, mit modellabhängigen niedrigeren Ausnahmen; der Faktor ist am konkreten Modell zu prüfen. [tweet-2058676383912431842](../sources/tweet-2058676383912431842.md)

Bei Standard-Readpreis lohnt sich fünfminütiges Caching gegenüber wiederholtem uncached Input bereits nach einem Read zusätzlich zum Write; einstündiges nach zwei Reads. Der Artikel verallgemeinert den zweiten Fall. $340→$87 bleibt eine persönliche, nicht reproduzierte Rechnung. [tweet-2058676383912431842](../sources/tweet-2058676383912431842.md)

### Residency und Workspace-Limits

Die [Residency-Dokumentation](https://platform.claude.com/docs/en/manage-claude/data-residency) beschreibt inference_geo als us/global, keinen EU-Wert. US-only hat bei Claude 4.6 und neuer einen öffentlich dokumentierten Faktor 1,1×; Workspace-Vorgaben können auch ohne Requestparameter US erzwingen. Das ist keine ausschließlich versteckte Opus-4.7-Prämie. [tweet-2058676383912431842](../sources/tweet-2058676383912431842.md)

[Workspace-Limits](https://platform.claude.com/docs/en/api/rate-limits#setting-lower-limits-for-workspaces) für Ausgaben und Requests/Input-/Output-Tokens sind dokumentiert; Organisationslimits gelten zusätzlich, und der Default-Workspace lässt sich nicht entsprechend begrenzen. Ein verstecktes zusätzliches Per-feature-Limit in der behaupteten Console-Karte ist nicht durch die konsultierten Docs belegt. Diese Betriebsgrenzen sind getrennt von Cache-Breakpoints zu betrachten. [tweet-2058676383912431842](../sources/tweet-2058676383912431842.md)

## Betriebshinweise im Kostenartikel (Stand 2026-09)

Der Anthropic-Artikel nennt als Grenzen: Der Cache ist an ein Modell gebunden, Treffer erfordern ein byte-identisches Präfix, und die Lebensdauer ist begrenzt. Praktische Hinweise: Effort nicht mitten im Gespräch ändern (nur bei ausgewählten Modellen wie Opus 5 und [Fable](../entities/Fable.md) 5.1 ohne Cache-Bruch), flüchtige Werte wie Zeitstempel aus dem Präfix halten, Tool-Definitionen nicht umsortieren, bei Gesprächs-Forks identisches Präfix, Modell und Effort wahren. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

Empfehlungen: Cache-Trefferrate in Claude Console und Cache-Diagnostics-API überwachen, selten genutzte Tools mit defer_loading zurückstellen, Systemanweisungen als Nachricht im Gespräch ergänzen, Modell- oder Effort-Wechsel in den Moment der ohnehin fälligen Kompaktierung legen, den Breakpoint per Automatic Caching mitwandern lassen, den Cache mit einer Anfrage mit max_tokens 0 vorwärmen und bei Agenten mit Wartezeiten über fünf Minuten eine einstündige TTL erwägen. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

Die Einsparungen des Artikels (etwa 72 bis 73 Prozent bei tau2-bench retail) sind Herstellermessungen, siehe [Claude API Skill](../entities/Claude%20API%20Skill.md). [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

## Ergänzungen (Stand 2026-09)

Die README von [Jev Model Router](../entities/Jev%20Model%20Router.md) lässt Hauptmodellrouting standardmäßig aus, weil Modellwechsel laut Projekt den Cache invalidieren können; Subagenten starten mit eigenem Kontext. Das zitierte Launch-Verhalten „nur bei Sitzungsstart“ und die gespeicherte turn.step-Option sind verschiedene Beschreibungen. [tweet-2101355584305943031](../sources/tweet-2101355584305943031.md)

Bei [Adaptive Reasoning Effort](Adaptive%20Reasoning%20Effort.md) behauptet der Autor, native Codex-Effort-Updates erhielten Präfix und Cache. Diese produktspezifische Aussage ist ohne Implementierung oder Messung gespeichert und nicht auf beliebige Modelle übertragbar. [tweet-2101872112977781180](../sources/tweet-2101872112977781180.md)

## Additions (Stand 2026-10)

[Claude Code Mods](../entities/Claude%20Code%20Mods.md) includes a cache timer advertised as five minutes with notifications. The savings claim is unmeasured; a UI timer alone does not establish actual cache hits or billing savings. [tweet-2106455605925822967](../sources/tweet-2106455605925822967.md)

## TTL getrennt einstellen (Stand 2026-10)

Lydia Hallie nennt promptCacheTtl für das Hauptgespräch und subagentPromptCacheTtl für Subagents in settings.json. Der kurze Post ist ein konkreter Bedienhinweis, keine gemessene Einsparung. [tweet-2108637982005833973](../sources/tweet-2108637982005833973.md)

Die am 12.10.2026 ergänzend gelesene [Claude-Code-Dokumentation](https://code.claude.com/docs/en/prompt-caching#choose-the-ttl-yourself) bestätigt die Werte 5m und 1h sowie die entsprechenden Umgebungsvariablen CLAUDE_CODE_PROMPT_CACHE_TTL und CLAUDE_CODE_SUBAGENT_PROMPT_CACHE_TTL, ab v2.1.242. Die zweite Einstellung betrifft alle Requests außerhalb des Hauptgesprächs, unter anderem Subagents, Workflows, Forks und Compaction. Dieser Doku-Nachtrag ist nicht in Raw gespeichert. [tweet-2108637982005833973](../sources/tweet-2108637982005833973.md)

Eine Stunde ist der Hauptgesprächs-Default im Claude-Abo innerhalb der Inklusivnutzung; Usage Credits, API und Cloud-Abrechnung verwenden standardmäßig fünf Minuten. Externe Requests nutzen meist ebenfalls fünf Minuten. FORCE_PROMPT_CACHING_5M kann längere Werte übersteuern; bei expliziter Wahl hat die Bucket-Umgebungsvariable Vorrang vor dem Setting. Längere TTL schreibt teureren Cache und bringt ohne entsprechende Pausen keinen automatischen Kostenvorteil. [tweet-2108637982005833973](../sources/tweet-2108637982005833973.md)
