---
tags: [agents, tools]
sources: [tweet-2079234800766816633.md, tweet-2080776965070496115.md, tweet-2081707421756457213.md, tweet-2108591328732856655.md, tweet-2088682533278077382.md, tweet-2087026930323247306.md]
created: 2026-10-02
updated: 2026-10-12
---

# Agent Workflow Graphs

## Definition (Stand 2026-07)

Der gespeicherte Artikel beschreibt mehrstufige Agentenarbeit als Graph: Ein Knoten ist eine begrenzte Aufgabe mit einem Eingang und einem Ausgang, eine Kante existiert nur, wenn die Ausgabe eines Knotens tatsächlich in die Eingabe eines anderen fließt. Ein „und dann“ ohne Datenfluss ist keine Kante; solche Wartezeiten sind vermeidbar. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

## Bausteine (Stand 2026-07)

- **Knotenvertrag:** explizite Eingabe und per JSON-Schema validierte Ausgabe, damit nachfolgende Knoten keine freie Textausgabe parsen müssen. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)
- **Kanten als Code:** Flatten, Dedupe und Filtern zwischen Stufen sind deterministischer Code ohne Modelltoken; Agenten sollen für Urteile eingesetzt werden, nicht fürs Durchreichen. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)
- **Fan-out und Fan-in:** unabhängige Knoten laufen parallel; eine Barriere ist nur dort gerechtfertigt, wo eine Stufe alle Ergebnisse zugleich braucht, etwa zum quellenübergreifenden Deduplizieren und Ranken. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)
- **Diamant:** Fan-out, Reduktion per Code, Synthese durch einen letzten Agenten. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)
- **Router:** Ein Agent klassifiziert, Code wählt den Pfad, zum Beispiel kurze Prüfung bei kleinem Diff und paralleles Audit bei hohem Risiko. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)
- **Verifier:** mehrere unabhängige Skeptiker, verschiedene Prüfperspektiven (Korrektheit, Sicherheit, Reproduzierbarkeit) oder ein Jurypanel vor der Übernahme eines Befunds. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)
- **Loop-until-dry:** Finder wiederholen, bis K Runden nichts Neues liefern; dedupliziert wird gegen alles bisher Gesehene, nicht nur gegen bestätigte Befunde, sonst konvergiert die Schleife nicht. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

## Laufzeit und Kosten (Stand 2026-07)

Der Artikel empfiehlt pipeline() als Standard, weil jedes Element die Stufen unabhängig durchläuft, und parallel() nur bei echter Abhängigkeit vom Gesamtergebnis. Fehlschläge einzelner Knoten sollen enthalten bleiben; Fan-in-Stufen sollen fehlende Eingaben tolerieren. Repetitive Knoten können auf ein günstigeres Modell gelegt werden, Synthese- und Urteilsknoten auf das stärkere. Parallel schreibende Knoten brauchen Isolation, etwa getrennte Git-Worktrees. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

## Gezeichneter Graph als Spezifikation (Stand 2026-07)

Alex Kotliarskyi beschreibt den kürzesten Weg mit [Codex](../entities/Codex.md): den Workflow als Graph zeichnen, auch auf Papier, und Codex bitten, daraus ein Code-Mode-Skript zu schreiben und mit den eigenen Eingaben auszuführen. Sein Beispielbild trennt residente Agenten von ephemeren Workern und führt eine Eingabe über Planer, Worker, mehrere Reviewer und Synthese zu einem Haiku. Belegt ist das Vorgehen, kein gespeicherter Lauf oder Qualitätsvergleich. [tweet-2080776965070496115](../sources/tweet-2080776965070496115.md)

## Zuschreibung an Claude Code und Grenzen (Stand 2026-07)

Der Artikel schreibt [Claude Code](../entities/Claude%20Code.md) „dynamic workflows“ zu: Claude schreibe ein JavaScript-Orchestrierungsskript mit agent(), parallel(), pipeline() und phase(), die Koordination koste keine Modelltoken, /deep-research sei ein mitgelieferter Graph und gespeicherte Skripte lägen in .claude/workflows/. Diese API- und Befehlsangaben stammen nur aus dem Artikel und wurden nicht gegen Dokumentation geprüft. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

Der Artikel ist ein Lehrtext mit Beispielcode und ohne Messung von Laufzeit- oder Qualitätsgewinnen; die Bun-Portierung wird nur erwähnt. [Loop Engineering](Loop%20Engineering.md) behandelt verwandte Fan-out-, Verifier- und Stoppmuster; [Agentic Knowledge Graph Construction](Agentic%20Knowledge%20Graph%20Construction.md) meint dagegen Graphen aus Daten. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

## Zugeschriebenes Graph-Engineering-Manual (Stand 2026-07)

Ein Post schreibt Andrej Karpathy einen zwölfseitigen Leitfaden „From 1 Loop to 1,000 Agents - The Graph Engineering Manual“ zu. Gespeichert ist nur ein Bild mit einem Wissensgraph-Schema für Multi-Agenten-Systeme, einem zentralen AGENT und acht verbundenen Entitäten. Das Dokument, seine Quelle und die Autorschaft sind nicht belegt; die Zuschreibung bleibt eine Behauptung des Posts. Der Nutzer hat den [PDF-Link auf Google Drive](https://drive.google.com/file/d/1-GOg0kxcp8tx1BMUECMj2yJq6JYGmfhb/view) nachgereicht (Dateiname Karpathy-Graph-Engineering-Systems.pdf); der Inhalt war nicht lesbar und ist daher noch nicht ausgewertet. [tweet-2081707421756457213](../sources/tweet-2081707421756457213.md)

Die sichtbare Einleitung verweist auf Karpathys autoresearch: ein 630-Zeilen-Skript habe 700 ML-Experimente in 48 Stunden ausgeführt. Das knüpft an den [LLM Autoresearch Loop](LLM%20Autoresearch%20Loop.md) an, ist hier aber nur als Bildtext gespeichert. [tweet-2081707421756457213](../sources/tweet-2081707421756457213.md)

## Managed-Agents-Produktbeispiel (Stand 2026-10)

[Claude Managed Agents](../entities/Claude%20Managed%20Agents.md) erweitert den allgemeinen Graph-Gedanken um eine konkrete Herstellerfunktion: Ein Lead schreibt den Ablauf, viele Agenten arbeiten in Phasen, ihre Ergebnisse werden kombiniert. Die Ankündigung beschreibt eine öffentliche Beta; der hier ergänzend gelesene Doku-Nachtrag unterscheidet dieses programmatische Orchestrieren von einzelnen Subagent-Delegationen. Ein eigener Lauf oder Qualitätsvergleich liegt nicht vor. [tweet-2108591328732856655](../sources/tweet-2108591328732856655.md)

## Ausführbarer Graph und Rollenpolitik (Stand 2026-08)

Das vollständige Video im Post trennt vier Teile: Knoten als begrenzte Arbeitseinheiten, Kanten als Übergänge, Zustand für Aufgaben/Evidenz/Budget und Policy für Rechte. Ein Workflow-Graph organisiert Ausführung; ein Wissensgraph organisiert Fakten. Diamant, Supervisor und Pipeline sind kombinierbare Topologien; Routing und Evaluator-Optimizer ergänzen sie. [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

Das Briefing-Beispiel trennt Recherche mit strukturierten Notizen, Schreiben und unabhängiges Review mit frischem Kontext. Code übernimmt deterministische Prüfungen und Datenreduktion; Tests oder echte Kundenergebnisse dienen als Realitätsanker. Einmalige einfache Aufgaben rechtfertigen den zusätzlichen Graph-Aufwand laut Sprecher häufig nicht. [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

Der Sprecher unterscheidet flexibel geplante Arbeitsabläufe von langsam veränderbaren, auditierbaren Rollen und Rechten: Das Modell soll keine dauerhaften Berechtigungen improvisieren. Framework-, Kosten- und Erfolgszahlen im Transkript sind nicht unabhängig geprüft; Namens- und Produktfehler der automatischen Transkription bleiben im Source-Beleg. [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

Der verknüpfte Artikel behandelt überwiegend Wissensgraphen und GraphRAG statt Ablaufgraphen. Seine fünf Promptvorlagen sind unter [Agentic Knowledge Graph Construction](Agentic%20Knowledge%20Graph%20Construction.md) abgelegt; [Loop Engineering](Loop%20Engineering.md) behandelt die verwandten Stopp- und Prüfprinzipien. [tweet-2088682533278077382](../sources/tweet-2088682533278077382.md)

## Offizieller SDK-Nachtrag (Stand 2026-08; Primärquelle geprüft 2026-10-12)

Der August-Post verlinkt ein offizielles Cookbook; Raw enthält nur dessen GitHub-Ladeansicht. Das am 12.10.2026 separat gelesene [aktuelle Notebook](https://raw.githubusercontent.com/anthropics/claude-cookbooks/main/claude_agent_sdk/08_Dynamic_workflows.ipynb) dokumentiert [Claude Code](../entities/Claude%20Code.md)-Orchestrierung aus dem Python Agent SDK: Workflow in allowed_tools erlauben und im Auftrag ausdrücklich verlangen. Die Mindeststände sind Python 3.11, CLI v2.1.154 und SDK 0.2.90. Diese aktuellen Angaben sind vom historischen Tweet getrennt. [tweet-2087026930323247306](../sources/tweet-2087026930323247306.md)

Das Beispiel extrahiert zehn nummerierte Aussagen, prüft jede parallel gegen Quelldateien, lässt nur bestätigte Aussagen durch einen Skeptiker angreifen und erzeugt einen Bericht. Das vollständige Prompt-Rezept verlangt strukturierte confirmed/contradicted/unverifiable-Ergebnisse und genaue Belegzeilen; die Daten sind ausdrücklich fiktiv. [tweet-2087026930323247306](../sources/tweet-2087026930323247306.md)

Die aktuelle Primärquelle bestätigt agent(), parallel(), pipeline(), phase(), Skriptvariablen und wiederverwendbare Skripte unter .claude/workflows/ für diesen Runtime-/SDK-Kontext. Maximal 16 Agenten laufen gleichzeitig, bei schwächerer CPU weniger; 1.000 ist das Limit pro Lauf insgesamt. Abgebrochene Läufe sind in derselben Sitzung fortsetzbar; eine neue Sitzung startet frisch. Diese Quelle bestätigt keine identischen Grenzen für [Claude Managed Agents](../entities/Claude%20Managed%20Agents.md). [tweet-2087026930323247306](../sources/tweet-2087026930323247306.md)

Ein kleiner Einzelauftrag soll weiterhin bei einem Agenten bleiben; Workflows passen laut Notebook bei vielen unabhängigen Prüfungen oder wiederverwendbarer Orchestrierung. Mehrere Agenten erhöhen den Tokenbedarf. Das Cookbook wurde gelesen, nicht ausgeführt; Beispiele sind kein unabhängiger Zuverlässigkeitsnachweis. [tweet-2087026930323247306](../sources/tweet-2087026930323247306.md)
