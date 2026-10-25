---
tags: [agents, tools]
sources: [tweet-2080710971228918066.md, tweet-2080439126390636661.md, tweet-2097369738968195513.md, tweet-2097242863964958760.md, tweet-2102198213067612337.md, tweet-2101888707259256903.md, tweet-2101411232771113143.md, tweet-2104744961904394699.md, tweet-2105367927394615364.md, tweet-2104241432467067343.md, tweet-2100739055923425589.md, tweet-2098480213244117065.md, tweet-2094138777178403057.md, tweet-2093559715150303691.md, tweet-2108891293749526823.md, tweet-2090862143402860859.md, tweet-2085817074816070014.md, tweet-2084753070437609606.md, tweet-2085052988981199064.md, tweet-2053770348353724666.md, tweet-2012378465664745795.md, tweet-2004129820335124948.md, tweet-2113990583241125942.md]
created: 2026-10-02
updated: 2026-10-25
---

# Context Engineering

## Definition (Stand 2026-07)

Thariq bezeichnet als Context Engineering den Kontext, den ein Agent über den einzelnen Prompt hinaus erhält: Systemprompt, Skills, CLAUDE.md-Dateien, Memory und weitere Quellen. Weil dieser Kontext für viele Anfragen gilt, kann er nicht so spezifisch sein wie ein Prompt. [tweet-2080710971228918066](../sources/tweet-2080710971228918066.md)

## Befund des Claude-Code-Teams (Stand 2026-07)

Das Team habe (Stand 2026-07) über 80 Prozent des Systemprompts von [Claude Code](../entities/Claude%20Code.md) für Modelle wie Claude Opus 5 und Claude Fable 5 ([Fable](../entities/Fable.md)) entfernt, ohne messbaren Verlust in den eigenen Coding-Evaluierungen. Als Ursache nennt der Artikel Überregulierung: In internen Transkripten widersprachen sich Systemprompt, Skills und Nutzeranfragen, etwa „leave documentation as appropriate“ gegen „DO NOT add comments“. Die Eval-Angabe ist eine Herstelleraussage ohne veröffentlichte Daten. [tweet-2080710971228918066](../sources/tweet-2080710971228918066.md)

## Sechs Verschiebungen (Stand 2026-07)

| Früher | Jetzt | Beispiel aus dem Artikel |
| --- | --- | --- |
| Regeln | Urteil | Statt starrer Kommentarregeln: „Write code that reads like the surrounding code: match its comment density, naming, and idiom.“ |
| Beispiele | Schnittstellendesign | Beispiele engen den Suchraum ein; eine Statusaufzählung pending, in_progress, completed zeigt die Nutzung des Todo-Tools. |
| Alles vorab | Progressive Disclosure | Verifikation und Code-Review als eigene Skills; verzögert geladene Tools über ToolSearch. |
| Wiederholung | Einfache Tool-Beschreibungen | Tool-Anleitungen in die Tool-Beschreibung statt zusätzlich in den Systemprompt. |
| Memory in CLAUDE.md | Auto-Memory | Claude speichert relevante Erinnerungen selbst. |
| Einfache Specs | Reichhaltige Referenzen | HTML-Artefakte, Testsuiten, zu portierender Code oder Rubriken mit Verifier-Agenten. |

Alle Zeilen: [tweet-2080710971228918066](../sources/tweet-2080710971228918066.md)

## Empfehlungen je Kontextquelle (Stand 2026-07)

- **Systemprompt:** beschreibt Produkt und Aufgabe; in Claude Code meist unverändert, beim eigenen Agenten-Harness der Ort für den größten Aufwand. [tweet-2080710971228918066](../sources/tweet-2080710971228918066.md)
- **CLAUDE.md:** kurz beschreiben, wofür das Repository da ist, und die meisten Tokens für Fallstricke verwenden; Offensichtliches weglassen, Details per Progressive Disclosure etwa in einen Verifikations-Skill auslagern. [tweet-2080710971228918066](../sources/tweet-2080710971228918066.md)
- **Skills:** leichte Wegweiser, nur in wichtigen Bereichen streng; lange Skills auf mehrere Dateien aufteilen; am nützlichsten für eigene Meinungen, Wissen und Praktiken von Person, Team oder Produkt. [tweet-2080710971228918066](../sources/tweet-2080710971228918066.md)
- **Referenzen:** per @ eingebundene Dateien; Code-nahe Formate bevorzugen, etwa ein HTML-Mockup statt Beschreibung oder Screenshot eines Designs. [tweet-2080710971228918066](../sources/tweet-2080710971228918066.md)

Das Repository anthropics/html-effectiveness sammelt eigenständige HTML-Beispiele für Code-Review, Designsysteme, Prototypen, Berichte, Diagramme und kleine Editier-Oberflächen als Agentenausgabe; die Beispieldaten sind fiktiv, der zugehörige Blogpost ist nicht gespeichert. [tweet-2080439126390636661](../sources/tweet-2080439126390636661.md)

## Werkzeug und Grenzen (Stand 2026-07)

Der Artikel nennt claude doctor beziehungsweise /doctor, um Skills und CLAUDE.md-Dateien zu verkleinern. Einzelne verlinkte Begriffe fehlen in der gespeicherten Extraktion; Wirkung und Verfügbarkeit des Befehls sind nicht geprüft, und der Befund gilt laut Artikel für die damals neueste Modellgeneration (Stand 2026-07: Opus 5, Fable 5), nicht allgemein. [tweet-2080710971228918066](../sources/tweet-2080710971228918066.md)

Verwandt: [Prompt Caching](Prompt%20Caching.md) für stabile Präfixe, [Codebase Maps](Codebase%20Maps.md) für HTML als Übersicht für Menschen. [tweet-2080710971228918066](../sources/tweet-2080710971228918066.md) [tweet-2080439126390636661](../sources/tweet-2080439126390636661.md)

## Überholte Anweisungen prüfen (Stand 2026-09)

Anweisungen, die Schwächen älterer Modelle ausgleichen, können bei neuen Modellen Kontext und Werkzeugaufrufe kosten. Das Vorgehen beschreibt [Instruction Debt Audit](Instruction%20Debt%20Audit.md); die Messwerte sind Herstellerangaben. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

## Backend als Teil des Kontexts (Stand 2026-09)

Der InsForge-Artikel überträgt den Gedanken auf Backends: Ein Agent kann das Dashboard nicht sehen, braucht deshalb eine strukturierte Gesamtsicht, schmale Skills und Fehler, die zeigen, woher sie stammen. Der berichtete Vergleich (Supabase gegenüber [InsForge](../entities/InsForge.md)) ist ein Einzelfall mit Werbecharakter. [tweet-2097242863964958760](../sources/tweet-2097242863964958760.md)

## Ergänzungen (Stand 2026-09)

[Kaku](../entities/Kaku.md) sammelt laut Produktseite Kontext aus Links, Backlinks und verwandten Notizen. [Jev Skill Suggestion](../entities/Jev%20Skill%20Suggestion.md) schlägt vor, Skills erst nach separater Entscheidung in den Hauptkontext einzufügen; Implementierungsdoku und gemessener Kontextgewinn fehlen dort. [tweet-2102198213067612337](../sources/tweet-2102198213067612337.md) [tweet-2101888707259256903](../sources/tweet-2101888707259256903.md)

## Ergänzungen (Stand 2026-09)

[Minimal Claude Code Setup](Minimal%20Claude%20Code%20Setup.md) treibt die Kontextreduktion auf die Spitze: Werkzeuge entfernen, Startkontext unter 2k Token und ein früher kompaktierendes 200k-Fenster. Die Wirkung auf Limits ist laut Autor noch ungeprüft. [tweet-2101411232771113143](../sources/tweet-2101411232771113143.md)

## Zielverständnis zurückspiegeln (Stand 2026-09)

Lauren (@poteto) nennt diesen direkt verwendbaren Prompt, um die Modellinterpretation sichtbar zu machen: [tweet-2104744961904394699](../sources/tweet-2104744961904394699.md)

> restate in your own words what you think my goals are and what the problem i'm trying to solve is [tweet-2104744961904394699](../sources/tweet-2104744961904394699.md)

Die Quelle beschreibt persönliche häufige Nutzung, ohne Wirksamkeitsmessung. Der Prompt betrifft das Verständnis der aktuellen Aufgabe; er liefert keine zusätzliche Projektinformation. [tweet-2104744961904394699](../sources/tweet-2104744961904394699.md)

## Sechsteilige AGENTS.md-Vorlage (Stand 2026-09)

Die gespeicherte Voxyz-Vorlage macht eine Instruktionsdatei zur Arbeitsvereinbarung für [Codex](../entities/Codex.md) und [Claude Code](../entities/Claude%20Code.md). Der vollständige Bildwortlaut ist auf der Source-Seite transkribiert; die Vorlage wurde hier nicht als Repository-Anweisung übernommen. [tweet-2105367927394615364](../sources/tweet-2105367927394615364.md)

1. Lange Aufgaben in zwei bis drei Sätzen zurückspiegeln, auf das Ja warten, Schritte samt Nachweis in PLAN.md führen, nach zwei Fehlversuchen neu planen und bei Unterbrechung einen Übergabestand hinterlassen. [tweet-2105367927394615364](../sources/tweet-2105367927394615364.md)
2. Im Auftragsumfang bleiben, funktionierendes Verhalten erhalten, Nutzer-/Entwickler-/Agentenaufwand abwägen, keine ungefragten Abhängigkeiten oder Refactors und vor überschreiben sichern. [tweet-2105367927394615364](../sources/tweet-2105367927394615364.md)
3. Explorer liest, Worker editiert, Reviewer berichtet; jede Delegation hat eine Aufgabe, Fertigbedingung und Kurzbericht. Keine gleichzeitigen Änderungen derselben Datei; Kernbehauptungen der Berichte prüfen. [tweet-2105367927394615364](../sources/tweet-2105367927394615364.md)
4. Bugs mit Nutzerschritten reproduzieren, Ursache beheben und dieselben Schritte erneut testen; fehlende Reproduktionsangaben benennen und Fehler nicht stummschalten. [tweet-2105367927394615364](../sources/tweet-2105367927394615364.md)
5. Tests selbst ausführen und lesen, UI unter anderem mit leerer Eingabe, Doppelsubmit und Refresh prüfen und ausgelassene Checks ausdrücklich nennen. [tweet-2105367927394615364](../sources/tweet-2105367927394615364.md)
6. Nutzerkorrekturen als When-X-do-Y-Regel in Lessons aufnehmen, bei Wiederholung die Regel verbessern; den übrigen Vorlagentext nur nach Nachfrage ändern. Neueste Lessons oben, überholte Regeln entfernen. [tweet-2105367927394615364](../sources/tweet-2105367927394615364.md)

Der Post nennt /plugin install claude-code-setup@claude-plugins-official als zusätzlichen Setup-Einstieg. Die behauptete zehnfache Produktivität und das clientabhängige automatische Lesen der Datei sind nicht geprüft. [Astra Agent Instructions](../entities/Astra%20Agent%20Instructions.md) ist eine andere persönliche Arbeitsvereinbarung; Lessons entsprechen dem Pflegegedanken einer [Coding Standards File](Coding%20Standards%20File.md). [tweet-2105367927394615364](../sources/tweet-2105367927394615364.md)

## Instruktionspflege aus Session-Evidenz (Stand 2026-09)

[Backpass](../entities/Backpass.md) bewertet vorhandene Regeln anhand tatsächlicher Sitzungen und lagert situative Verfahren bei belegten Triggern in Skills aus. Die Firstmate-Fallstudie berichtet 48 Prozent weniger ständig geladene Tokens; ihre PR-Historie enthält nachträgliche Korrekturen an Skill-Ladezeitpunkten und inline belassene Regeln. Kontextkürzung braucht deshalb auch Kontrolle, ob die Regel im richtigen Moment verfügbar bleibt. [tweet-2104241432467067343](../sources/tweet-2104241432467067343.md)

## Kontext auswählen statt umschreiben (Stand 2026-09)

Der Bericht zu fast-jev-compaction lässt [Jev](../entities/Jev.md) Tool-Aufrufe und Ergebnisse nach Relevanz behalten, kürzen oder entfernen, während der übrige Dialog wortgetreu bleibt. Installation, Parameter und der begrenzte Screenshot-Nachweis stehen in [Jev Project Directory](../synthesis/Jev%20Project%20Directory.md). Kontextverkleinerung ist hier kein gemessener Nachweis gleicher Ergebnisqualität. [tweet-2100739055923425589](../sources/tweet-2100739055923425589.md)

## Skill-Trigger und Fertigbedingungen nach OpenAI (Stand 2026-09)

Der OpenAI-Leitfaden für GPT-6 Astra empfiehlt kurze, präzise Skill-Beschreibungen: eine Migrations-Skill soll Migrationen und Rollout-Reviews auslösen, nicht jede Datenbankaufgabe. Zu viele lange Beschreibungen können laut Artikel gekürzt werden und die Auswahl erschweren. [tweet-2098480213244117065](../sources/tweet-2098480213244117065.md)

Mehrteilige Skills sollen einen kleinen Router und bedarfsgerecht geladene Referenzen nutzen. AGENTS.md sollte Dokumente nach Aufgabe zuordnen statt vor jeder kleinen Änderung einen Vollüberblick zu erzwingen. [tweet-2098480213244117065](../sources/tweet-2098480213244117065.md)

Der Artikel empfiehlt konkrete sichere Arbeitsfreigaben und explizite Fertigbedingungen, einschließlich Ausführen, Ergebnisinspektion und Fehlerbehebung, wenn dies zum Auftrag gehört. Das sind modellbezogene Herstellerempfehlungen; andere persönliche Vorlagen bleiben separate, datierte Verfahren. [tweet-2098480213244117065](../sources/tweet-2098480213244117065.md)

## Projektwissen auf dem Dateisystem (Stand 2026-08)

Das vom Nutzer ergänzte Ondrej-/Dex-Gespräch empfiehlt, Kontext als für den Agenten direkt lesbare Dateien vorzuhalten: Architekturentscheidungen unter docs/adr, externe Betriebsbedingungen unter docs/external, API-Verträge, Testzugänge und Konfigurationsnamen; Umgebungsvariablenwerte beziehungsweise Geheimnisse gehören nicht in diese Dokumente. Das ergänzt die bereits gespeicherte ADR-Praxis, ohne eine neue Wirkungsmessung zu liefern. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)

Wiederkehrende Kontextbeschaffung kann vor Sitzungsbeginn deterministisch laufen, etwa ein Hook für die letzten Sentry-Issues. Der Vorschlag spart laut Sprecher Modellarbeit beim Beschaffen von Kontext; er ist kein Beleg, dass externe API-Aufrufe oder CPU-Zeit kostenlos sind. Read, write, edit, grep und bash sollen auf ein gut vorbereitetes Dateisystem zugreifen. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)

Die frühere „Dumb Zone“ um halbe Kontextfüllung beschreibt Dex im Interview als Lernhilfe für ältere Modelle, keine universelle 100k-Grenze. Er berichtet inzwischen auch über längere Verläufe und bessere Kompaktierung. Bei schlechteren Ergebnissen bleibt ein Verfahren: Erkenntnisse in einem Dokument sichern, eine neue Sitzung starten und daraus weiterarbeiten. Die historischen Modellbeispiele und Sprechererfahrungen überschreiben keine neueren Limits. Verwandt: [Agentic Engineering](Agentic%20Engineering.md) für Programmdesign und frühe Verständnisprüfung. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)

## Lehrquelle für Agenten-Harnesses (Stand 2026-08)

[AI Agents in Depth](../entities/AI%20Agents%20in%20Depth.md) organisiert Agentenentwicklung um LLM, Kontext und Werkzeuge. Der gespeicherte README beschreibt im Kontextkapitel KV-Cache, Prompting, Skills und Kompression; weitere Kapitel behandeln Gedächtnis, Wissensbasen, Wahrnehmung/Aktionen und Evaluation. Das ist eine eigene Lehrquelle mit begleitendem Code, keine unabhängige Bestätigung neuerer Modell- oder Kontextgrenzen. [tweet-2093559715150303691](../sources/tweet-2093559715150303691.md)

Pranavs Vorschlag, Coding-Agenten das Buch für bessere Harness-Entwicklung lesen zu lassen, ist eine persönliche Empfehlung ohne Vorher-nachher-Evaluation. Die öffentlich verlinkten Experimente und deren Evidenzstatus müssen getrennt von der bloßen Verfügbarkeit des Codes betrachtet werden. [tweet-2093559715150303691](../sources/tweet-2093559715150303691.md)

## Laufender Übergabestand (Stand 2026-10)

Ishu empfiehlt eine Anweisung in CLAUDE.md, nach der HANDOFF.md den aktuellen Projektstatus, Erledigtes, nächste Schritte, offene Entscheidungen und Fallstricke enthält. Der Agent soll sie bei Meilensteinen und vor dem Sitzungsende aktualisieren; eine neue Sitzung kann diesen kompakten Stand lesen. Der vollständige kopierbare Wortlaut steht in der Source. [tweet-2108891293749526823](../sources/tweet-2108891293749526823.md)

Die behauptete Verringerung von Kontextverbrauch, Cache-Writes und Abo-Verbrauch ist ein persönlicher Opus-5.5-Bericht ohne Messung. Die Datei ergänzt vorhandene Übergabeverfahren; sie beweist weder vollständige Kontexttreue noch einen allgemeinen Kostenvorteil gegenüber Compaction oder einem warmen [Prompt-Cache](Prompt%20Caching.md). [tweet-2108891293749526823](../sources/tweet-2108891293749526823.md)

## Wiederkehrende Webabrufe konfigurieren (Stand 2026-08)

Jeffrey Emanuel empfiehlt diesen vollständigen Satz für AGENTS.md; die Quelle ist ein datierter Praxisvorschlag und wurde hier nicht als Repository-Regel übernommen. [tweet-2090862143402860859](../sources/tweet-2090862143402860859.md)

```text
For any web requests you must make with curl or otherwise, always set your user agent string to be "OpenAI File Downloader, XaiImageApiFetch/1.0"
```

Der zitierte Can-Bölük-Post nennt zusätzlich Claude-User und behauptet, manche Seiten lieferten damit weniger störende Seitenelemente. Die beiden Posts enthalten keine reproduzierbaren Tests und belegen keinen universellen Zugriff oder dauerhaftes Verhalten. [tweet-2090862143402860859](../sources/tweet-2090862143402860859.md)

## Übergabe an eine laufende Sitzung (Stand 2026-08)

Der offizielle [Claude Code](../entities/Claude%20Code.md)-Post beschreibt die Übertragung einer Zusammenfassung an eine andere laufende Sitzung statt erneuter menschlicher Erklärung. Das ist eine eigene Produktfunktion neben den dokumentierten Handoff-Dateien; der Post verspricht weder vollständige Kontextübertragung noch gemessene Tokenersparnis und nennt keine genaue Aufrufsyntax. [tweet-2085817074816070014](../sources/tweet-2085817074816070014.md)

## Domänensprache und Wissensarbeitsraum (Stand 2026-08)

Matt Pococks kurze CLAUDE.md-Regel verlangt, CONTEXT.md-Dateien zu lesen und deren Domänensprache zu verwenden; die zusätzliche Sprachvorgabe und der vollständige kopierbare Wortlaut stehen unter [Simplified Technical English](../entities/Simplified%20Technical%20English.md). Der Post belegt keine automatische Dateierkennung oder Ergebnisverbesserung. [tweet-2084753070437609606](../sources/tweet-2084753070437609606.md)

[Cabinet](../entities/Cabinet.md) beschreibt einen separaten selbst gehosteten Markdown-/Git-Arbeitsraum mit Agenten und versioniertem Wissen. Die angekündigte Graphvorschau und Anbieterangaben sind keine unabhängig geprüfte Wissensqualität oder Sicherheitsgarantie. [tweet-2085052988981199064](../sources/tweet-2085052988981199064.md)

## Vier Karpathy-Regeln für Coding-Agenten (Stand 2026-05)

Der gespeicherte Artikel schreibt diese vier Ausgangsregeln Andrej Karpathy und ihre Aufbereitung als CLAUDE.md Forrest Chang zu. Sie sind eine im Artikel wiedergegebene Arbeitsvereinbarung für [Claude Code](../entities/Claude%20Code.md), keine hier gemessene Wirksamkeitsgarantie. [tweet-2053770348353724666](../sources/tweet-2053770348353724666.md)

1. **Think Before Coding:** Annahmen offenlegen, bei Unsicherheit nachfragen, mehrere plausible Interpretationen sichtbar machen und auf einen einfacheren Weg hinweisen; bei ungeklärtem Verständnis stoppen und das Problem benennen. [tweet-2053770348353724666](../sources/tweet-2053770348353724666.md)
2. **Simplicity First:** Nur die angeforderte Funktion mit möglichst wenig verständlichem Code umsetzen; keine spekulativen Features oder Abstraktionen für einen einzelnen Einsatz hinzufügen. [tweet-2053770348353724666](../sources/tweet-2053770348353724666.md)
3. **Surgical Changes:** Nur notwendige Stellen ändern, ausschließlich den eigenen verursachten Ballast bereinigen, keine benachbarten Kommentare oder Formatierungen ungefragt verbessern und dem vorhandenen Stil folgen. [tweet-2053770348353724666](../sources/tweet-2053770348353724666.md)
4. **Goal-Driven Execution:** Prüffähige Erfolgskriterien definieren und bis zum verifizierten Ergebnis iterieren; Ziele sollen eigenständige Ausführung ermöglichen, statt nur eine Schrittfolge abzuarbeiten. [tweet-2053770348353724666](../sources/tweet-2053770348353724666.md)

## MCP- und Plugin-Budget (Stand 2026-01)

Affaan warnt in seinem Setup-Artikel, dass zu viele aktive MCP-Server und Plugins das Kontextfenster stark verkleinern: Ein Fenster von 200k Token vor der Kompaktierung könne auf etwa 70k schrumpfen. [tweet-2012378465664745795](../sources/tweet-2012378465664745795.md) Seine Faustregel lautet 20 bis 30 konfigurierte MCPs, aber weniger als 10 aktiv und weniger als 80 aktive Werkzeuge; ungenutzte werden pro Projekt über disabledMcpServers in ~/.claude.json abgeschaltet. [tweet-2012378465664745795](../sources/tweet-2012378465664745795.md) Er selbst hatte 14 MCPs konfiguriert und nur etwa 5 bis 6 pro Projekt aktiv. [tweet-2012378465664745795](../sources/tweet-2012378465664745795.md) Die Zahlen sind Erfahrungswerte des Autors, keine Messung.

## Projektentwicklung vor dem Kontext (Stand 2025-12)

Muratcan Koylan ergänzt die Laufzeit-Skills seiner Context-Engineering-Sammlung um einen Skill eine Ebene darüber: Er soll entscheiden helfen, was gebaut wird und wie das Projekt für schnelle Iteration aufgebaut ist. Details stehen in [LLM Project Development Methodology](LLM%20Project%20Development%20Methodology.md). [tweet-2004129820335124948](../sources/tweet-2004129820335124948.md)

## Erfahrungsspeicher als Kontextquelle (Stand 2026-10)

Das REM-Paper behandelt frühere Agentenläufe als Kontext, der gespeichert, zum richtigen Zeitpunkt eingespielt und wieder entfernt werden muss. Details und Zahlen: [Experience Memory for Coding Agents](Experience%20Memory%20for%20Coding%20Agents.md). [tweet-2113990583241125942](../sources/tweet-2113990583241125942.md)
