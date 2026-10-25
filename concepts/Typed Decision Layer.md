---
tags: [agents, tools]
sources: [tweet-2103185949341491513.md, tweet-2103190313624039620.md, tweet-2102377493705740417.md, tweet-2102632147303710835.md, tweet-2102386737192607894.md, tweet-2102119751774527859.md, tweet-2101484241762603363.md, tweet-2101888707259256903.md, tweet-2102060095265735085.md, tweet-2101872112977781180.md, tweet-2101894250401271876.md, tweet-2101384465629200656.md, tweet-2101311813908652069.md, tweet-2101289796979077235.md, tweet-2100979911825789393.md, tweet-2100917158922387537.md, tweet-2100659471257366766.md, tweet-2100388704644919662.md, tweet-2100239244501430438.md]
created: 2026-10-03
updated: 2026-10-08
---

# Typed Decision Layer

## Definition

Ein Agentensystem trennt Generierung, Entscheidungen und Wahrheit: ein generierendes Modell schreibt Code, ein Entscheidungsmodell wie [Jev](../entities/Jev.md) liefert typisierte Antworten mit Wahrscheinlichkeit und Konfidenz, Compiler, Tests, Lint und Build prüfen, was Software beweisen kann. [tweet-2103185949341491513](../sources/tweet-2103185949341491513.md)

## Mechanismus

- Der Host bereitet eine gefilterte Optionsliste vor, das Modell wählt oder enthält sich, der Host prüft die Wahl erneut; jede Entscheidung braucht benannte Optionen, ein prüfbares Ergebnis und eine Aufzeichnung des Effekts. [tweet-2103190313624039620](../sources/tweet-2103190313624039620.md)
- Beispiele sind Routenwahl für neue Aufgaben, Fokuswahl inspect/implement/verify/answer, Recovery bei Toolfehlern und fokussierte Checks vor der vollen Testsuite. [tweet-2103190313624039620](../sources/tweet-2103190313624039620.md)
- Fragen werden gebündelt gegen denselben State gestellt, auch spekulative, und erst danach im Code geroutet; Konfidenzschwellen steigen mit der Tragweite, niedrige Konfidenz geht an einen Menschen. [tweet-2102377493705740417](../sources/tweet-2102377493705740417.md)
- Retry, Eskalation und Abschluss werden als typisierte Entscheidung statt als Prosa eines LLM abgefragt. [tweet-2103185949341491513](../sources/tweet-2103185949341491513.md)

## Beispiele

Community-Projekte setzen das Muster für Kontextkompaktierung, Modellrouting, Code-Review und Abschlussnachweise um. [tweet-2102386737192607894](../sources/tweet-2102386737192607894.md) Ein Trading-Loop lässt das Modell alle 15 Sekunden entscheiden, ein zweites Modell die Regeln nachts überarbeiten und ein Gate Selbständerungen der Regeln verhindern; Schlüssel sieht kein Modell. [tweet-2102632147303710835](../sources/tweet-2102632147303710835.md)

## Grenzen

Ein zitierter Artikel nennt für Jev nur Texteingabe und 64k Kontext je Request. [tweet-2102377493705740417](../sources/tweet-2102377493705740417.md) Kosten- und Erfolgsangaben stammen aus Einzelberichten; siehe [AI Coding Cost Claims](AI%20Coding%20Cost%20Claims.md). Die Trading-Ergebnisse umfassen acht Tage. [tweet-2102632147303710835](../sources/tweet-2102632147303710835.md) Verwandt: [Hook-Enforced Model Routing](Hook-Enforced%20Model%20Routing.md), [Codex Astra Luna Orchestrator](../entities/Codex%20Astra%20Luna%20Orchestrator.md). [tweet-2103185949341491513](../sources/tweet-2103185949341491513.md)

## Ergänzungen (Stand 2026-09)

TypeSafes Doku empfiehlt strukturierte JSON-Instructions und Rubriken, wenn Fragen mehrere benannte Teile haben oder bereits Schema-/Taxonomiedaten vorliegen. Choice-Optionen können Unterbäume zeigen; beim Taxonomiewalk werden anschließend Kinder der gewählten Ebene befragt, bei knappen Wahrscheinlichkeiten können mehrere Pfade weiterverfolgt werden. Noul kann true/false-Grenzen durch Definitionen und Beispiele erhalten. Codeblöcke fehlen in der gespeicherten Extraktion. [tweet-2102119751774527859](../sources/tweet-2102119751774527859.md)

[Jev Explained](../entities/Jev%20Explained.md) macht State, Fragen, Verteilungen und decide()-Policy getrennt sichtbar. [Jev Skill Suggestion](../entities/Jev%20Skill%20Suggestion.md) überträgt die Entscheidung auf Kontextwahl, [Adaptive Reasoning Effort](Adaptive%20Reasoning%20Effort.md) auf begrenzte Effort-Fenster. [tweet-2101484241762603363](../sources/tweet-2101484241762603363.md) [tweet-2101888707259256903](../sources/tweet-2101888707259256903.md) [tweet-2101872112977781180](../sources/tweet-2101872112977781180.md)

[Virlo](../entities/Virlo.md) zeigt die Bedeutung einer präzisen Rubrik: Thema als Pflicht und Ton/Format als Präferenz verbessert laut Anbieter sein kleines 44er-Testset von 16 auf 33 richtige Zuordnungen. Das ist ein lokaler Befund, keine allgemeine Genauigkeitsgarantie. [tweet-2102060095265735085](../sources/tweet-2102060095265735085.md)

## Ergänzungen (Stand 2026-09)

Ein weiteres öffentliches Notiz-Doc zu TypeSafe und Coding-Agenten ist nur als Titel gespeichert. [tweet-2101894250401271876](../sources/tweet-2101894250401271876.md)

## Incidents zu überprüften Skills (Stand 2026-09)

Jev Tip 004 schlägt vor, dem Abschlussbericht eines Agenten ein Incident-Feld hinzuzufügen und Incident-Bericht plus aktiven Skill gegen explizite Lückenkriterien bewerten zu lassen. Nur bei qualifizierter Lücke wird der Skill geändert oder neu angelegt; anschließend werden Incidents als Evals wiederholt, bevor die Änderung freigegeben wird. Das ist ein vorgeschlagener Lernzyklus, kein gemessener Wirksamkeitsnachweis. [tweet-2101384465629200656](../sources/tweet-2101384465629200656.md)

## Trading: State, Urteil, Policy und Risiko (Stand 2026-09)

Der Trading-Artikel trennt deterministische Zustandsberechnung, probabilistische Urteile von [Jev](../entities/Jev.md), Policy im Code und Orderausführung. Preise, Spreads, Imbalance, Volatilität, Inventar und Drawdown bleiben Berechnungen; Regime, Flow-Toxizität und Setupqualität sind vorgeschlagene Urteilsfragen. Unabhängige atomare Fragen werden gegen denselben kompakten Snapshot gebündelt, abhängige Fragen brauchen weitere Requests. [tweet-2101311813908652069](../sources/tweet-2101311813908652069.md)

Die Anleitung verlangt nur Daten vor dem Entscheidungszeitpunkt und geloggte State/Decision/Outcome-Datensätze, Modell-Pinning und eine harte Deadline: veraltete oder zu spät eingetroffene Entscheidungen führen zu Hold. Risikolimits bleiben deterministische Vetos vor jeder Order; Konfidenz ersetzt kein überprüfbares Limit. [tweet-2101311813908652069](../sources/tweet-2101311813908652069.md)

Als wirtschaftliche Prüfung nennt der Autor insbesondere Gas für jedes Cancel/Replace. Sein Beispiel von rund 428 MON je Stunde gegenüber 3,5 Basispunkten Spread ist eine Artikelangabe, kein hier repliziertes Ergebnis; Latenz allein belegt keinen profitablen Bot. [tweet-2101311813908652069](../sources/tweet-2101311813908652069.md)

Für den Vergleich fordert der Artikel identische Daten, Features, Kosten und Limits für handgeschriebene Regeln, Frontier-LLM, Jev und Jev mit Konfidenz-Gating. Genannt werden Sharpe, Sortino, Drawdown, Slippage, Adverse Selection, Kosten und Coverage; Kalibrierung soll anhand empirischer Frequenzen, Brier Score, Log Loss und Expected Calibration Error auf dem eigenen Handelsplatz geprüft werden. Herstellerkalibrierung gilt nicht automatisch für dessen Verteilung. [tweet-2101311813908652069](../sources/tweet-2101311813908652069.md)

Die Quelle nennt 32k Kontext. Die TypeSafe-Modelldokumentation (https://docs.typesafe.ai/models.md, Stand 2026-10-08) nennt 64k Tokens je Request, davon 32k für State plus die längste Frage; der scheinbare Widerspruch zu einem gespeicherten Jev-Artikel mit 64k löst sich damit auf. Mehrere angekündigte Code-/Diagrammblöcke fehlen; der Text ist Architekturmaterial, keine vollständig gespeicherte ausführbare Bauanleitung. [tweet-2101311813908652069](../sources/tweet-2101311813908652069.md)

## Legitime Retries und Drift-Sicherung (Stand 2026-09)

Tip 003 verlangt für die Retry-Bewertung Task-Vertrag, Fehlerbericht, fehlgeschlagene Strategie, vorgeschlagene neue Strategie und explizite Kriterien für einen legitimen Wiederholungsversuch. Erfüllt der Retry diese Kriterien nicht, soll der Host neu planen, eskalieren oder stoppen. Konkrete Kriterien und Schwellen legt der kurze Post nicht fest. [tweet-2101289796979077235](../sources/tweet-2101289796979077235.md)

Der zitierte Tip 002 schlägt einen Checker außerhalb des Agentenloops vor: bei jedem Zustandswechsel Task-Vertrag, Delta und Checkliste auf Drift bewerten; bei überschrittenem Schwellwert löst eine Sicherung Umleitung, Eskalation oder Pause aus. Dies ergänzt den bereits beschriebenen Incident-Lernzyklus um Kontrolle während der Ausführung, ohne Wirksamkeitsmessung. [tweet-2101289796979077235](../sources/tweet-2101289796979077235.md)

## Vier Arbeitsabläufe für Wissen und Content (Stand 2026-09)

Shann Holmbergs Diagramm trennt jeweils bereitgestellte Referenzen, [Jev](../entities/Jev.md)-Fragen und Aktionen des Anwendungscodes. Es zeigt vorgeschlagene Abläufe, keine nachgewiesene Prognosequalität; unsichere Entscheidungen gehen zur menschlichen Prüfung. [tweet-2100979911825789393](../sources/tweet-2100979911825789393.md)

- **Second Brain:** Dokument, Nachricht oder Meetingnotiz plus Kategorien, Pflichtfelder und vorhandene Notizen bereitstellen. Jev beurteilt Typ, Thema und mögliche Dubletten; Code prüft Pflichtfelder, speichert mit Quelle und verifiziert das Ergebnis. Unklare Fälle werden geprüft. [tweet-2100979911825789393](../sources/tweet-2100979911825789393.md)
- **Content-Revision:** Entwurf, Anti-Slop-Regeln, Voice-DNA-Datei und frühere Inhalte mit Ergebnissen bereitstellen. Jev prüft generische Sprache, Wiederholungen und Stilabweichungen; ein Schreibagent überarbeitet markierte Stellen. Geschätztes Potenzial wird nach Veröffentlichung mit echten Ergebnissen verglichen. [tweet-2100979911825789393](../sources/tweet-2100979911825789393.md)
- **Post-Analyse:** Hook, Themen-/Formatkriterien und frühere Posts mit Ergebnissen vergleichen. Das Diagramm bewertet einen Hook anhand der Regel, eine konkrete Aufgabe zu benennen, von vage bis spezifisch; der Schreibagent konkretisiert ihn, anschließend wird Engagement gemessen. [tweet-2100979911825789393](../sources/tweet-2100979911825789393.md)
- **SEO-Review:** Zielkeyword, eigener Entwurf und die derzeit führenden Artikel der SERP bereitstellen. Jev vergleicht Query-Fit und Themenabdeckung; das Schreibmodell überarbeitet schwache Abschnitte, der Betreiber verfolgt tatsächliche Rankings. Eine verlässliche Vorhersage von Ranking oder Reichweite ist nicht belegt. [tweet-2100979911825789393](../sources/tweet-2100979911825789393.md)

Die im Post wiedergegebenen 193,6-fache Beschleunigung und 444,6-fache Kostenreduktion sind TypeSafes Workflow-Testangaben, keine Messung dieser vier Anwendungen. Der [Jev Workspace Audit](Jev%20Workspace%20Audit.md) bietet eine verwandte Methode zur Auswahl und Prüfung eines eigenen Tests. [tweet-2100979911825789393](../sources/tweet-2100979911825789393.md)

## Sechs Schritte zur Jev-Integration (Stand 2026-09)

Ronin schlägt den folgenden Ablauf vor; die genannten Schwellen sind seine Orientierung, keine auf dem eigenen Workload geprüften Sicherheitsgrenzen. [tweet-2100917158922387537](../sources/tweet-2100917158922387537.md)

1. Calls identifizieren, die nur eine Auswahl oder Bewertung benötigen, und in typisierte Fragen überführen: Choice für Optionen, Score für geordnete Stufen, Noul für eine 0-1-Antwort. [tweet-2100917158922387537](../sources/tweet-2100917158922387537.md)
2. Unabhängige Fragen gegen denselben State bündeln; erst der Code entscheidet, welche Antworten genutzt werden. [tweet-2100917158922387537](../sources/tweet-2100917158922387537.md)
3. Nach Konfidenz eskalieren: Der Post nennt unter 0,5 ein größeres Modell oder einen Menschen und 0,85+ vor irreversiblen Aktionen. Diese Werte sind Autorenempfehlungen, keine allgemeine Erfolgswahrscheinlichkeit. [tweet-2100917158922387537](../sources/tweet-2100917158922387537.md)
4. Kandidaten in normalem Code aus DOM, Retriever oder Tool-Trace erzeugen; das Modell soll daraus wählen statt Optionen zu erfinden. [tweet-2100917158922387537](../sources/tweet-2100917158922387537.md)
5. Jev im Loop einsetzen: Router vor der Modellauswahl, Gate vor einem Tool-Aufruf und Judge nach dem Ergebnis. [tweet-2100917158922387537](../sources/tweet-2100917158922387537.md)
6. Bei Kompaktierung Tool-Aufrufe und Ergebnisse auf Relevanz bewerten, Unnötiges entfernen und den behaltenen Inhalt wörtlich erhalten. Das ist verwandte Kontextauswahl, keine Verlustfreiheitsgarantie. [tweet-2100917158922387537](../sources/tweet-2100917158922387537.md)

Der offizielle Installationsweg ist bereits bei [Jev](../entities/Jev.md) und [Jev Workspace Audit](Jev%20Workspace%20Audit.md) dokumentiert. Dieser Post wiederholt npx skills add typesafe-ai/skills --skill typesafe-ai sowie für [Claude Code](../entities/Claude%20Code.md) claude plugin marketplace add typesafe-ai/skills und claude plugin install typesafe@typesafe-ai. Anschließend API-Key im Dashboard anlegen und den Agenten mit use the TypeSafe skill ansprechen. [tweet-2100917158922387537](../sources/tweet-2100917158922387537.md)

Der Post beschreibt Jev als auf enge Entscheidungen begrenztes Textmodell und schwächer auf breiten Benchmarks. Sein E-Mail-Beispiel mit 18.514 Nachrichten, 98,33 Prozent Genauigkeit und 1,12 Dollar sowie das 100x-Versprechen sind nicht hier repliziert; sie belegen keinen pauschalen Vorteil. [tweet-2100917158922387537](../sources/tweet-2100917158922387537.md)

## Events vor dem Orchestrator filtern (Stand 2026-09)

Gregor schlägt vor, nicht jede Nutzernachricht, E-Mail oder Subagentenantwort automatisch an den teuren Hauptagenten zu schicken. [Jev](../entities/Jev.md) soll anhand des Events zwischen direktem Subagenten-Routing, einer Warteschlange und dem Aufwecken des Orchestrators entscheiden. Der Post ergänzt damit bekanntes Modellrouting um die Frage, ob ein großer Modellaufruf überhaupt erforderlich ist. [tweet-2100659471257366766](../sources/tweet-2100659471257366766.md)

Der zitierte Browser-Use-Post trennt DOM als State, neu erzeugte Aktionskandidaten pro Schritt und einen kleinen LLM als Texteingabe-Fallback. Die genannten sieben Sekunden und 0,0039 USD sind ein einzelner Autorenbericht; der Hauptpost liefert keine Implementierung des Event-Routers oder geprüfte 10x-Messung. [tweet-2100659471257366766](../sources/tweet-2100659471257366766.md)

## Gemeinsamer Prefill und parallele Optionsbewertung (Stand 2026-09)

Anders Lie beschreibt folgende mögliche Umsetzung mit offenen Sprachmodellen; es ist eine erklärende Hypothese über Jev-artige Inferenz, keine Offenlegung von TypeSafes privater Engine. [tweet-2100388704644919662](../sources/tweet-2100388704644919662.md)

1. Jede gültige Antwortoption mit einem Label wie 1, 2 oder 3 versehen. [tweet-2100388704644919662](../sources/tweet-2100388704644919662.md)
2. Gemeinsame Informationen und die Ausgabestruktur einmal als Prefill verarbeiten. [tweet-2100388704644919662](../sources/tweet-2100388704644919662.md)
3. Den gecachten Kontext pro Eigenschaft verzweigen und jeweils die einzelne Frage hinzufügen. [tweet-2100388704644919662](../sources/tweet-2100388704644919662.md)
4. Fragen parallel auswerten und die Logits auf gültige Antwortlabels beschränken. [tweet-2100388704644919662](../sources/tweet-2100388704644919662.md)
5. Labels auf Antwortwerte zurückabbilden und aus den Logits per Softmax Optionsscores bilden. [tweet-2100388704644919662](../sources/tweet-2100388704644919662.md)

Der Autor erwartet Skalierungsvorteile mit der Zahl paralleler Fragen bis zur Rechensättigung und nennt Training kleiner Modelle für diese Inferenzform als zusätzliche Kosten-/Qualitätsverbesserung. Er liefert weder Engine-Code noch einen kontrollierten Benchmark; Softmax-Scores sind hier kein Nachweis kalibrierter Richtigkeit. [Jev](../entities/Jev.md) ist der Bezug, während [OpenJev NLI](../entities/OpenJev%20NLI.md) einen getrennten, trainierten Cross-Encoder beschreibt. [tweet-2100388704644919662](../sources/tweet-2100388704644919662.md)

## Qwen-Erklärdiagramm für JSON-Feldklassifikation (Stand 2026-09)

Niels Rogge erklärt anhand eines Qwen2.5-RLCD-Modells: Kontext und Schema einmal vorverarbeiten, KV-Cache speichern, pro Feld den Feldsuffix mit diesem Cache auswerten, den letzten Hidden State durch den LM-Head schicken, nur Logits der erlaubten Antworttokens auswählen, Softmax bilden und das höchste Ergebnis auf den Feldwert abbilden. [tweet-2100239244501430438](../sources/tweet-2100239244501430438.md)

Das Originaldiagramm zeigt risk_level mit vier Enum-Werten, requires_review als Boolean und action_tier mit drei Stufen. Der Host setzt die gewählten Werte zum JSON zusammen; fehlende Klammern oder unzulässige Enum-Werte werden damit vermieden, richtige Sachentscheidungen oder kalibrierte Wahrscheinlichkeiten folgen daraus nicht. [tweet-2100239244501430438](../sources/tweet-2100239244501430438.md)

*Bildhinweis: Qwen-Diagramm: gemeinsamer Prefill, KV-Cache, Feldsuffix und begrenzte Logits (Bild nicht mitgeliefert).* [tweet-2100239244501430438](../sources/tweet-2100239244501430438.md)

Die Visualisierung ist eine zusätzliche Erklärung zum bereits beschriebenen parallelen Optionsscoring. Ihr Titel How Jev works ist kein Beleg, dass TypeSafes private Engine genau so implementiert ist; der Post nennt ein offenes Qwen-Modell als Grundlage und liefert keinen kontrollierten Laufzeitvergleich. [tweet-2100239244501430438](../sources/tweet-2100239244501430438.md)
