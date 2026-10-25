---
tags: [agents, product-building]
sources: [tweet-2071509401224261823.md, tweet-2067842298667225185.md, tweet-2067721938894500036.md, tweet-2064663221718425660.md, tweet-2063698758517366884.md, tweet-2074060484047712521.md, tweet-2073741417143300099.md, tweet-2062139630955184170.md, tweet-2061545633560010826.md, tweet-2057924890330644925.md, tweet-2056418157305454805.md, tweet-2074049148765016255.md, tweet-2078148918173368411.md, tweet-2077826623320023303.md, tweet-2055307509267587534.md, tweet-2080257779395154409.md, tweet-2079569829120377139.md, tweet-2094425039554629829.md, tweet-2094138777178403057.md, tweet-2093335809097109630.md, tweet-2092988408050360798.md, tweet-2107939129736700335.md, tweet-2088742864310481025.md, tweet-2049506712801935611.md, tweet-2046223609870582020.md, tweet-2043620640792379812.md, tweet-2040705762406895940.md, tweet-2041505133025194343.md, tweet-2041299378967621889.md, tweet-2112219173288120531.md, tweet-2112047997987213449.md]
created: 2026-09-29
updated: 2026-10-23
---

# Agentic Engineering

## Begriff und Beispiel

Der Post schreibt Andrej Karpathy eine Abgrenzung von „Agentic Engineering“ zu Vibe Coding zu und nennt Spezifikation, Eval-Schleifen und Sicherheitsaufsicht als Kernfähigkeiten. Die Zuschreibung wird in der gespeicherten Quelle nicht unabhängig verifiziert. [tweet-2071509401224261823](../sources/tweet-2071509401224261823.md)

Der begleitende Artikel zeigt als Beispiel mit [Google Agents CLI](../entities/Google%20Agents%20CLI.md) einen RAG-Agenten, der vor Bereitstellung gegen 20 synthetische Fälle geprüft wird. Ein Eval-Hinweis auf eine zu freizügige Agentenanweisung führte laut Autor zur Korrektur. [tweet-2071509401224261823](../sources/tweet-2071509401224261823.md)

## Grenze

Der Artikel ist eine Kooperation mit Google Cloud und belegt weder allgemeine Produktreife noch Übertragbarkeit des Einzelfalls. Das Video-Transkript fehlt. [tweet-2071509401224261823](../sources/tweet-2071509401224261823.md)

## Arbeitsweise im Gespräch mit Matt Pocock

Pocock beschreibt Klärungsfragen, Spezifikation und zerlegte Aufgaben vor Agentenläufen sowie menschliche Priorisierung bei vielen parallel möglichen Arbeiten. Er betont, dass Git, Debugging, Tests und ein gut änderbarer Codebestand den Nutzen eines Agents beeinflussen. Diese Punkte stammen aus einem Gespräch, nicht aus einer Vergleichsstudie. [tweet-2067842298667225185](../sources/tweet-2067842298667225185.md)

## Issue-Workflow und Lernprompt (Stand 2026-06)

Ein gespeicherter Pull Request zeigt mehrere konkrete Implementierungsschritte samt Tests hinter Pococks Kurzformel „Issue labeln, Implementierung erhalten“. Der PR belegt Artefakte, aber die Gesamtabfolge mit GitHub Actions, Sandcastle und [Claude Code](../entities/Claude%20Code.md) ist aus dem Raw nur teilweise rekonstruierbar. [tweet-2067721938894500036](../sources/tweet-2067721938894500036.md)

Pococks teach-Prompt verschiebt den Blick von reinem Codieren auf Planung, QA und Codebase-Design; Screenshot und Post zeigen den vorgeschlagenen Lernstart, nicht die Wirksamkeit des Trainings. [tweet-2064663221718425660](../sources/tweet-2064663221718425660.md)

## Benchmarks und Arbeitskontext (Stand 2026-06 bis 2026-07)

Der Post zur [Meta-Agent Challenge](Meta-Agent%20Challenge.md) behauptet, autonome Agentenentwicklung scheitere häufig an Budgetsteuerung, Fehlerbehebung und Designwechseln; ohne gespeicherten Paper-Volltext ist das eine Zusammenfassung des Postautors. [tweet-2063698758517366884](../sources/tweet-2063698758517366884.md)

Matt Pocock empfiehlt, Dev-Server-Ausgaben in eine lokale Datei zu schreiben und sie in AGENTS.md zu nennen, damit Agenten Laufzeitfehler lesen können; der Post misst den Nutzen nicht. [tweet-2074060484047712521](../sources/tweet-2074060484047712521.md)

David Ondrej kündigt öffentliche Agenten-Skills an; gespeichert ist ein Screenshot mit Ordnernamen, kein Skill-Text. Das online identifizierte Repository https://github.com/davidondrej/skills führt passende Ordnergruppen und Skill-Dateien; seine README liegt inzwischen im Raw-Beleg (siehe unten), beweist aber nicht das Ziel des alten Kurzlinks. [tweet-2073741417143300099](../sources/tweet-2073741417143300099.md)

## Ergänzungen (Stand 2026-06)

[Prefactoring](Prefactoring.md) ergänzt Pococks Arbeitsweise um einen vorbereitenden Blick auf Codeänderbarkeit: vor der Implementierung nach Umbauten suchen, welche den eigentlichen Schritt einfacher machen. Der kurze Post belegt den Prompt, keinen Zeit- oder Qualitätsgewinn. [tweet-2062139630955184170](../sources/tweet-2062139630955184170.md)

Suzannes im Bild gelesener Lehrprompt verlangt inkrementelle Verständnisprüfungen und eine laufende Markdown-Checkliste für Problemursache, Lösungsentscheidung, Randfälle und Auswirkungen. Erst eigene Wiedergabe abfragen, dann Lücken schließen; Warum-Fragen, offene oder Multiple-Choice-Quizzes und bei Bedarf Code/Debugger sollen die Erklärung prüfen. [tweet-2061545633560010826](../sources/tweet-2061545633560010826.md)

Die /goal-Endbedingung im Bild ist nachgewiesenes Verständnis aller Checklistenpunkte. Der Prompt enthält die Verifikationsabsicht, aber keine Lernergebnisse oder Vergleichsdaten. [tweet-2061545633560010826](../sources/tweet-2061545633560010826.md)

## Karpathys direkte Abgrenzung und laufende Notizen (Stand 2026-05)

Im gespeicherten Interview unterscheidet Karpathy Vibe Coding als niedrigere Einstiegsschwelle von professioneller Agentenarbeit, die schneller werden soll, ohne Qualität und Sicherheitsverantwortung abzugeben. Das ist ein direkter Gesprächsbeleg für die grobe Abgrenzung; die speziellen Eval- und Werkzeugzuschreibungen älterer Posts werden dadurch nicht automatisch bestätigt. [tweet-2057924890330644925](../sources/tweet-2057924890330644925.md)

Er erklärt ungleichmäßige Modellfähigkeiten durch Trainingsdaten und verifizierbare RL-Aufgaben. Als verbleibende menschliche Arbeit nennt er Spezifikation, Urteil, Design und Verständnis; sein Beispiel falsch über E-Mail zugeordneter Zahlungen illustriert einen berichteten Designfehler. [Software 3.0](Software%203.0.md) beschreibt den dazugehörigen Wechsel zu Prompt und Kontext als Programmiermittel. [tweet-2057924890330644925](../sources/tweet-2057924890330644925.md)

[Implementation Notes](Implementation%20Notes.md) ergänzt die Aufsicht um eine laufende Datei für Entscheidungen, Abweichungen, Alternativen und offene Fragen. Thariqs präzisierter Prompt liefert eine wiederverwendbare Anweisung, aber keinen gemessenen Effekt auf Qualität oder Geschwindigkeit. [tweet-2056418157305454805](../sources/tweet-2056418157305454805.md)

## Gespeicherte Skills-Sammlung und Rollenvertrag (Stand 2026-07)

Die neue README von [David Ondrej Skills](../entities/David%20Ondrej%20Skills.md) liegt nun im Raw-Beleg und erklärt fünf Kategorien wiederverwendbarer Agenten-Workflows. Das schließt die frühere Kataloglücke für dieses Repository, bestätigt aber weiterhin nicht den alten Kurzlink oder den Inhalt einzelner Skills. [tweet-2074049148765016255](../sources/tweet-2074049148765016255.md)

[Kimi First](../entities/Kimi%20First.md) beschreibt einen expliziten Vertrag: Claude plant und prüft, Kimi führt feste Work Orders aus, Tests und vollständiger Diff werden unabhängig kontrolliert und nach zwei erfolglosen Runden übernimmt Claude. Die README ist ein Workflow-Artefakt, kein Qualitäts-/Kostenvergleich der Modelle. [tweet-2077826623320023303](../sources/tweet-2077826623320023303.md)

## Demo versus belastbares Produkt (Stand 2026-07)

Im Karpathy-Transkript wird eine promptbare Bildungsdemo von zuverlässig adaptiver [AI Tutoring](AI%20Tutoring.md)-Produktfunktion unterschieden. Die Aussagen des weiterverbreitenden Posts über Agenten-Müll, tote Diversität und 90 Prozent Demo-Unternehmen sind darin nicht belegt und werden nicht als Karpathy-Zitate übernommen. [tweet-2078148918173368411](../sources/tweet-2078148918173368411.md)

## Lokales Geschäftsbeispiel und Wettbewerbsthese (Stand 2026-05)

David Ondrej behauptet, Menschen mit Agentic-Engineering-Kompetenz würden ihre Geschäftskonkurrenten deutlich übertreffen. Die gespeicherte Bildbeschreibung zeigt einen von Greg Brockman geteilten Post über einen [Codex](../entities/Codex.md)-Skill zum Finden lokaler Unternehmen mit Website-Bedarf und den Beispielprompt „Find local businesses within 20km of Casoria“. Das belegt eine konkrete Aufgabenidee im Screenshot, aber weder den vollständigen Skill noch tatsächlich gewonnene Kunden oder einen Wettbewerbsvorteil. [tweet-2055307509267587534](../sources/tweet-2055307509267587534.md)

## Prüfgauntlet statt Codelektüre (Stand 2026-07)

Robert C. Martin liest den Code seiner Agenten nach eigener Aussage nicht mehr und setzt stattdessen auf strenge Vorgaben: Unit- und Gherkin-Tests, QA-Prozeduren, Qualitätsmetriken, Mutation Testing und Testabdeckung. Sein Vertrauen stützt er darauf, dass der Code alle diese Prüfungen bestehen muss; Projektdaten oder Fehlerraten nennt der Post nicht. [tweet-2080257779395154409](../sources/tweet-2080257779395154409.md)

Dazu passend hebt er bei [Squeaky Clean](../entities/Squeaky%20Clean.md) die Arbeitsteilung hervor: große Modelle für Architektur, viele kleine Modelle parallel für die Implementierung. Er schreibt ausdrücklich, das Werkzeug nicht ausprobiert zu haben. [tweet-2079569829120377139](../sources/tweet-2079569829120377139.md)

## Ondrejs persönliches Setup (Stand 2026-08, Q3 2026)

Der vollständige Artikel ergänzt den Katalog [David Ondrej Skills](../entities/David%20Ondrej%20Skills.md) um persönliche Arbeitsverfahren. Die Oberfläche bb bündelt laut Autor mehrere Harnesses und Abos; [Cmux](../entities/Cmux.md) bietet geteilte Terminal-Panes und Browser, wird von ihm bei vielen parallelen Workspaces aber als unübersichtlich beschrieben. Ghostty und Herdr dienen seinem Terminalbetrieb; Herdr zeigt Zustände wie running, idle, blocked und done. Sein noch nicht veröffentlichtes Corral priorisiert fertig gewordene Agenten nach P1 bis P4, statt sie allein nach Abschlusszeit zu beantworten. Das sind unterschiedliche Werkzeuge und berichtete Erfahrungen, keine unabhängig geprüfte Produktbewertung. [tweet-2094425039554629829](../sources/tweet-2094425039554629829.md)

### Persistente Ausführung und wiederverwendbare Bedienung

Für länger laufende Agenten beschreibt Ondrej einen eigenen VPS mit Herdr und SSH-Zugriff von Laptop oder Telefon. Sein Einrichtungsauftrag lautet: "learn everything about that server, and set up the dev environment. Herdr, Node.js, Python 3, Git". Im berichteten Ablauf hatte er die SSH-Sitzung selbst geöffnet und ließ den Agenten über einen zweiten Cmux-Pane installieren. Die Behauptung, damit in zehn Minuten den Großteil gehosteter Cloud-Agenten abzudecken, ist eine Einzelfallerzählung; Betrieb, Wiederaufnahme und Sicherheit wurden hier nicht getestet. [tweet-2094425039554629829](../sources/tweet-2094425039554629829.md)

Häufige Einzelanweisungen legt er als Textkürzel ab, mehrstufige Abläufe als Skills aus [David Ondrej Skills](../entities/David%20Ondrej%20Skills.md). Vor der Implementierung lässt er wichtige Designentscheidungen einzeln mit Optionen klären. Kurze globale Aliase reduzieren wiederholte CLI-Eingaben; Diktiersoftware ersetzt in seinem Setup das Tippen. Seine Aliase cc und cx umgehen nach eigener Beschreibung die Rechteabfragen von [Claude Code](../entities/Claude%20Code.md) beziehungsweise [Codex](../entities/Codex.md); dies ist die dokumentierte Autorenpraxis, keine allgemeine Sicherheitsvorgabe. [tweet-2094425039554629829](../sources/tweet-2094425039554629829.md)

### Parallelität und Auslieferung

Worktrees empfiehlt er für mittelgroße bis große Projekte mit vielen parallelen Agenten, für kleine Projekte dagegen einen einfachen einzelnen Branch. Die Entscheidung folgt der erwarteten Kollisionsgefahr, nicht einer Pflicht zur maximalen Parallelisierung. Agentenzustände, Aufgabenprioritäten und bewusst gewählte Subagent-Modelle sollen gemeinsam mit Regeln, Rechten und Auslösebedingungen gesteuert werden. [tweet-2094425039554629829](../sources/tweet-2094425039554629829.md)

Sein Guardrail-Hook soll destruktive Befehle und Zugriffe auf sensible Systeme abfangen. Für Auslieferungen mit vielen Agenten beschreibt er einen Betriebssystem-Lock über die gesamte Folge Merge, Prüfung, Push, CI, Deploy und Healthcheck, statt nur über den letzten Push. Vollständige Hook-Implementierungen enthält der Artikel nicht. [tweet-2094425039554629829](../sources/tweet-2094425039554629829.md)

### Review, Entscheidungen und Produktionsdaten

Für mittlere bis große Änderungen empfiehlt er zwei unterschiedliche Modelle zur Prüfung und anschließend eine deduplizierte Liste wichtiger Findings; kleine Frontend-Änderungen behandelt er leichter. Er warnt vor rekursiven Reviews und festen Fehlerquoten wie "find the 5 biggest issues", weil diese aus seiner Sicht erfundene Probleme begünstigen. Eine gemessene Fehlerrate nennt der Artikel nicht. [tweet-2094425039554629829](../sources/tweet-2094425039554629829.md)

Wesentliche Architekturentscheidungen dokumentiert er unter /docs/adr mit Entscheidung, Begründung und damaligem Projektzustand. Ein ausschließlich lesender Postgres-Zugang soll Agenten erlauben, vermuteten Feature-Bedarf mit echten Nutzungsdaten zu prüfen. Tests will er nach Bedarf begrenzen; seine provokative Anweisung, keine Tests zu verlangen, ist ein persönliches Prompt-Rezept und ersetzt keine risikobezogene Prüfung. [tweet-2094425039554629829](../sources/tweet-2094425039554629829.md)

Voraussehbare Folgeschritte reiht er vorab ein, etwa Plan umsetzen, durch ein anderes Modell prüfen und Findings beheben. Für die eigene Entwicklung betrachtet er Commits, Agentensitzungen und Nutzerprompts gemeinsam über längere Zeit; keine Einzelmetrik sei allein aussagekräftig. Das dazu erwähnte Vectal-Labs-Repo ist in der gespeicherten Extraktion nicht benannt und wird daher nicht erfunden. [tweet-2094425039554629829](../sources/tweet-2094425039554629829.md)

### Zeitgebundene Auswahl und Evidenzgrenze

Die Empfehlungen zu Harnesses, Modellrollen und Abos bilden Q3 2026 ab: minimaler Pi-Harness, Cursor CLI, als selbstverbessernd bezeichnete Hermes/Prime-Harnesses sowie Claude Code/Codex; die Budgetleiter und die pauschale Ablehnung von API-Preisen sind Autorenmeinungen. Sie überschreiben keine neueren Modell- oder Produktangaben der verlinkten Seiten. Er empfiehlt eigene Versuche bei Modellwechsel statt Rangfolgen aus sozialen Medien; die ergänzende Seite [Model Selection Evals](Model%20Selection%20Evals.md) behandelt systematische Prüfung. [tweet-2094425039554629829](../sources/tweet-2094425039554629829.md)

Behauptete Sprachtempo-, Kosten- und Produktivitätsgewinne sowie Cursor-PR-Anteile und Zukunftsprognosen wurden hier nicht unabhängig verifiziert. Die Quelle belegt ein persönliches Setup und wiederverwendbare Verfahren, keinen universellen optimalen Stack. [tweet-2094425039554629829](../sources/tweet-2094425039554629829.md)

## Vier Stufen vor und während der Implementierung (Stand 2026-08)

Im vom Nutzer ergänzten [Gespräch von David Ondrej und Dex Horthy](https://www.youtube.com/watch?v=xgkjtF89-44) vom 07.08.2026 beschreibt Dex einen Ablauf, der menschliche Designentscheidungen vor große Codeänderungen legt. Das vollständige Autotranskript (internes Zusatzmaterial; nicht Teil dieser Ausgabe) wurde am 09.10.2026 gesichert; der Video-Link ist ein datierter Nutzer-Nachtrag zum Bookmark. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)

1. **Produkt:** Nutzerproblem und messbares Erfolgskriterium klären; eine Erklärung des späteren Features und einfache HTML-Prototypen schreiben, bevor technische Entscheidungen getroffen werden. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)
2. **Systemarchitektur:** Dienste, Datenfluss, Endpunkte, Tabellen und relevante Abfragen mit dem späteren Reviewer abstimmen. Der Aufwand richtet sich nach Reife und Risiko des Produkts; die Suche nach Product-Market Fit kann schnellere Experimente rechtfertigen. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)
3. **Programmdesign:** Vorab die Entscheidungen klären, die der Agent sonst still treffen würde: Dateiplatzierung, Typen, Methodensignaturen, Call Stack und Tests. Kleine Codeblöcke machen die geplante Struktur prüfbar, bevor umfangreiche Implementierung den Richtungswechsel verteuert. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)
4. **Vertikale Schritte:** Erst einen dünnen Pfad vom API-Stummel bis zum Frontend verbinden und prüfen, dann Migrationen, Geschäftslogik und Fehlerfälle ergänzen. Jede Stufe mit curl, Browser oder Tests beobachten; nicht erst alle Datenbank-, Service- und Frontendschichten vollständig bauen. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)

### Verständnis, Regression und widersprechende Praxis (Stand 2026-08)

Dex berichtet, dass sein früherer Factory-Ansatz ohne regelmäßige Codelektüre zu einem hartnäckigen Fehler und aufwendiger Einarbeitung in schlecht verstandenen Code geführt habe. Er empfiehlt, Verständnis aktiv zu halten, etwa durch Agentenerklärungen, Fragen, Diagramme und bewusstes Verlangsamen bei Kontrollverlust. Ondrej beschreibt dagegen, kleine Änderungen teils ohne vollständiges Review auszuliefern; das Gespräch dokumentiert verschiedene Risikotoleranzen. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)

Der Gegensatz zur zuvor dokumentierten Praxis Robert C. Martins ist ausdrücklich zeitlich und personell zu trennen: Martin setzt am 23.07.2026 laut [Post](../sources/tweet-2080257779395154409.md) auf Prüfgauntlets ohne Codelektüre; Dex begründet im August-Gespräch, weshalb er sich darauf nicht generell verlassen will. Beide Quellen berichten Praxis und Positionen, keine kontrollierten Zuverlässigkeitsdaten. Siehe den Abschnitt „Prüfgauntlet statt Codelektüre“ oben. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)

Zur Testqualität nennt das Gespräch eine konkrete Gegenprobe: Modellpatch entfernen, neue Tests gegen den ursprünglichen Code laufen lassen und prüfen, ob sie dort scheitern. Tests, die vor und nach dem Fix bestehen, belegen den Fehler nicht. Tests, Linters und Modellreviews ergänzen sich; bestandene Einzelschritt-Benchmarks belegen laut Dex keine langfristige Änderbarkeit. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)

### Den Auslieferungsengpass bearbeiten (Stand 2026-08)

Dex unterscheidet ineffiziente Teilprozesse vom tatsächlichen Engpass: Wenn Review oder Produktklärung limitiert, erhöht mehr Agenten-Code allein den beim Nutzer ankommenden Wert nicht. Verbrauchte Tokens oder ausgeschöpfte Abos sind damit keine Erfolgsmetrik. Die Sprecher diskutieren Betriebsalarme und Featureanfragen als mögliche Eingänge einer Factory, aber ohne vollständige Produktionsimplementierung. [tweet-2094138777178403057](../sources/tweet-2094138777178403057.md)

## Technische Tests ersetzen keine Produktnutzung (Stand 2026-08)

Der [SnagTime](../entities/SnagTime.md)-Autor berichtet von wiederholten Agenten-Testschwärmen, aber einer erst durch menschliche Nutzung erkannten unpassenden Buchungsnavigation. Die 334 aggregierten Agentenstunden und rund 15.000 Dollar geschätzter Inferenzgegenwert belegen seinen Einzelfall; Betrieb und Wartung bleiben eigene Arbeit. Der aktuelle Repo-Nachtrag grenzt lokale Demo, Stripe-Testbetrieb und öffentliche Infrastruktur separat ab. [tweet-2093335809097109630](../sources/tweet-2093335809097109630.md)

## Belegte Bereinigung statt weiterer Abstraktionen (Stand 2026-08)

[Simplify Codebase](../entities/Simplify%20Codebase.md) ergänzt den Implementierungsablauf um explizite Verbraucherprüfung, Modul-Eigentumsgrenzen und eine vollständige Löschgrenze; Unteragenten bearbeiten Teilbereiche, ein Hauptagent integriert und prüft Tests, Typen, Lint und Build. Der vollständige Bildprompt ist auf der Werkzeugseite übersetzt, die Wirkung nicht gemessen. [tweet-2092988408050360798](../sources/tweet-2092988408050360798.md)

## Harness-Vertrag als kopierbares Muster (Stand 2026-10)

Der beigefügte Artikel trennt Harness (Dateien, Tools, Permissions, dauerhafter Zustand), Loop (Aktion und objektive Prüfung) und Graph (getrennte Agentenkontexte). Sein HARNESS.md-Muster enthält erlaubten Scope, verbotene Aktionen, Projektpfade, Linter-/Test-/Schema-Prüfung und Eskalation nach zweimaligem gleichen Fehler. Der vollständige Artikel und die zwei Draft-/Review-Prompts stehen auf der Source. [tweet-2107939129736700335](../sources/tweet-2107939129736700335.md)

Ein wiederverwendbares Prinzip ist, eine Regel sowohl als Instruktion als auch als tatsächliche mechanische Schranke zu formulieren, etwa begrenzte Tool-Rechte und ausgeführte Tests. Eine Markdown-Regel allein setzt weder Dateirechte noch einen Validator durch; die behauptete Halbierung von Halluzinationen und andere Wirksamkeitsversprechen wurden nicht reproduziert. [tweet-2107939129736700335](../sources/tweet-2107939129736700335.md)

## Abschluss gegen Belege prüfen (Stand 2026-08; gespeicherte v2-README)

[Unlazy](../entities/Unlazy.md) hält Acceptance Gates in Dateien fest und prüft sie mit CHECK-/EXPECT-Kommandos; Evidenz statt selbst behauptetem Abschluss entscheidet. Der optionale Stop-Hook gilt nur für [Claude Code](../entities/Claude%20Code.md). Der Autor empfiehlt die Kombination mit [Ponytail](../entities/Ponytail.md), ohne einen kontrollierten Vergleich dieser Kombination zu liefern. [tweet-2088742864310481025](../sources/tweet-2088742864310481025.md)

## Sandcastle-Aufbau aus dem Originaltutorial (Stand 2026-04)

Das vollständige Originaltutorial ergänzt den oben dokumentierten späteren PR-Beleg: [Sandcastle](../entities/Sandcastle.md) trennt Issue-Planung, Implementierung in eigenen Sandboxes/Branches, unabhängigen Diff-Review und Zusammenführung. Prompts und Modellwahl liegen beim aufrufenden Projekt; der erfolgreiche Demo-Lauf ist kein allgemeiner Nachweis zuverlässiger unbeaufsichtigter Auslieferung. [tweet-2049506712801935611](../sources/tweet-2049506712801935611.md)

## Vibe Coding auf prüfbare Leaf Nodes begrenzen (Stand 2026-04; ältere Aufnahme)

Im am 20.04.2026 geteilten Vortrag empfiehlt ein sich als Eric von Anthropic vorstellender Coding-Agent-Forscher, delegierten Code nach seiner Architekturrolle zu unterscheiden: Leaf Nodes sind abgegrenzte Endfunktionen, auf denen wenig anderes aufbaut; Kernarchitektur und tragende Abhängigkeiten sollen Menschen weiter verstehen und intensiv prüfen. Technische Schulden seien ohne Codeverständnis schwer zu erkennen und deshalb in Leaf Nodes eher einzudämmen. Das ist eine Risikostrategie des Sprechers, keine Sicherheitsgarantie. [tweet-2046223609870582020](../sources/tweet-2046223609870582020.md)

### Anforderungen und verständliche Prüfpunkte

Der Mensch übernimmt die Produktverantwortung: Anforderungen, Grenzen, relevante Dateien und vorhandene Muster sammeln, bevor der Agent implementiert. Der Sprecher beschreibt etwa 15–20 Minuten gemeinsame Codebase-Erkundung und Planung als eigene Praxis; konkrete Implementierungsdetails nur dort vorgeben, wo sie tatsächlich wichtig sind. Das fertige Planartefakt kann vor einem neuen Kontext oder einer Kompaktierung gespeichert werden, statt die gesamte Erkundung erneut zu laden. [tweet-2046223609870582020](../sources/tweet-2046223609870582020.md)

Ein-/Ausgaben und Akzeptanztests sollen die gewünschte Produkteigenschaft für Menschen nachvollziehbar machen. Bei seinem berichteten 22.000-Zeilen-Patch an einem Reinforcement-Learning-System lagen Änderungen überwiegend in Leaf Nodes; zentrale Teile wurden intensiv geprüft, Stabilität mit langen Stresstests untersucht. In der Fragerunde grenzt er das Beispiel auf Offline-Betrieb ein; daraus folgt keine Absicherung öffentlich erreichbarer Authentifizierung, Zahlungen oder Datenbanken. [tweet-2046223609870582020](../sources/tweet-2046223609870582020.md)

Für testgetriebene Arbeit empfiehlt er wenige verständliche End-to-End-Fälle, etwa einen Erfolgsfall und zwei Fehlerfälle, statt Tests an Implementierungsdetails zu binden. Er liest häufig zuerst die Tests und prüft, ob deren Erwartungen stimmen. Ein bestandenes Testset ersetzt damit weder eine passende Testauswahl noch die gezielte Architekturprüfung. [tweet-2046223609870582020](../sources/tweet-2046223609870582020.md)

### Lernen und historischer Stand

Für unbekannte Codebereiche lässt er [Claude Code](../entities/Claude%20Code.md) zunächst relevante Dateien, Klassen und ähnliche Features erklären; neue Bibliotheken und deren Auswahl kann er während der Arbeit hinterfragen. Kompaktieren oder neu beginnen empfiehlt er an einem sinnvollen Arbeitsabschluss, beispielsweise nach der Planung. [tweet-2046223609870582020](../sources/tweet-2046223609870582020.md)

Die Aufnahme nennt Claude 4 vor Veröffentlichung und vergleicht es mit 3.7; sie ist deshalb älter als ihr April-Repost. Aussagen über exponentiellen Fortschritt, Aufgabenlängen und Produktivitätsgewinne bleiben zeitgebundene Sprecherprognosen beziehungsweise Erfahrungsberichte und überschreiben keine neueren Modellbelege. [tweet-2046223609870582020](../sources/tweet-2046223609870582020.md)

## GitLab-Issue- und PR-Schleife (Stand 2026-04)

Der gespeicherte Artikel beschreibt einen dreiteiligen Ablauf: Eine dotnet-App fragt GitLab alle 15 Minuten ab; der Agent beurteilt, ob ein Issue hinreichend geklärt ist, und entwirft sonst eine Rückfrage. Bei bearbeitbaren Issues implementiert ein Subagent auf einem neuen Branch und erstellt einen PR. Ein weiterer Durchlauf prüft neue PR-Kommentare und bearbeitet sie. Die behauptete Produktivitätswirkung ist ein Erfahrungsbericht ohne verlinkte Implementierung oder Messdaten. [tweet-2043620640792379812](../sources/tweet-2043620640792379812.md)

Der wiederverwendbare Prompt lautet: Read the entire project and create a CLAUDE.md based on: Think Before Coding, Simplicity First, Surgical Changes, Goal-Driven Execution. Adapt to the real architecture you see. Der Artikel zeigt ihn mit claude -p und --allowedTools Bash,Write,Read. Vor einer tatsächlichen Anwendung sind die zu lesenden Dateien und Schreibrechte bewusst zu wählen; hier wurde keine Konfiguration erzeugt. [tweet-2043620640792379812](../sources/tweet-2043620640792379812.md)

Der gleiche Artikel bewirbt Everything Claude Code und einen historischen Downgrade auf v2.1.98. Seine behaupteten 40-zu-3-Prozent-Verstöße, 20.196 Zusatztokens und Einkommen sind nicht unabhängig belegt; der Downgrade ist keine aktuelle Handlungsempfehlung. Das Video enthält kein auswertbares Transkript. [tweet-2043620640792379812](../sources/tweet-2043620640792379812.md)

## ECC: nachvollziehbare Prüf- und Übergabeartefakte (Nachrecherche 2026-10-21)

[Everything Claude Code](../entities/Everything%20Claude%20Code.md) dokumentiert Plan → fehlschlagenden Test → Implementierung → bestandene Tests → Review aus frischem Kontext → abschließende Verifikation. Sein Memory Vault übergibt knappe Zustände mit Belegen und offenen nächsten Schritten zwischen Harnesses, behandelt Erinnerungen aber als ungeprüften Kontext. Das sind nachvollziehbare Arbeitsvorgaben des Projekts, keine hier bestätigten Produktivitäts- oder Sicherheitsgewinne. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)

## Gedächtnis und Sitzungsverzweigung (Stand 2026-04)

Der Praxistest von [MemPalace](../entities/MemPalace.md) ergänzt Markdown-Wikis um einen anderen Weg: vorhandene Gespräche und Dateien importieren, strukturiert durchsuchen und über MCP für den Agenten verfügbar machen. Der Sprecher zeigt einen Suchtreffer, bricht aber einen langen Import ab und kritisiert die interaktive Initialisierung. Der Test belegt keine vollständige Erfassung oder überlegene Gedächtnisleistung. [tweet-2041505133025194343](../sources/tweet-2041505133025194343.md)

Das ausführliche [Pi Agent](../entities/Pi%20Agent.md)-Tutorial zeigt /tree für Nebenpfade innerhalb einer Sitzung und /fork für eine neue Sitzung. Themenfremde Debugging-Schritte können damit getrennt bearbeitet werden; pi -c setzt die letzte Sitzung fort, pi -r wählt eine frühere. Themes und Erweiterungen werden im gezeigten Ablauf mit /reload geladen. Diese April-Beispiele ergänzen den späteren allgemeinen Pi-Harness-Hinweis, ohne dessen Q3-Modell- oder Budgetempfehlungen zu ersetzen. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md)

## P0 vor Agenten-Multitasking (Stand 2026-10)

Thariq empfiehlt, bei paralleler Agentenarbeit bewusst langsamer zu werden: Welche Aufgabe ist P0, und wie sähe sie mit voller Aufmerksamkeit aus? Das ist eine Priorisierungsfrage, keine Ablehnung jeder Parallelisierung und kein gemessener Produktivitätsvorteil. [tweet-2112219173288120531](../sources/tweet-2112219173288120531.md)

## Review-Loop mit menschlicher Eskalation (Stand 2026-10; Bildnachtrag 2026-10-23)

Der vom Nutzer nachgereichte Ablauf zum zitierten Boris-Post trennt vier Stufen: Code erzeugen, Selbstprüfung des erzeugenden Agenten, Review durch einen zweiten Agenten und automatisierte Checks. Erst danach entscheidet „All clear?“ über die nächste Stufe. Der Bildnachtrag ist in der Source sichtbar und gehört nicht zum gespeicherten Raw-Text. [tweet-2112047997987213449](../sources/tweet-2112047997987213449.md)

- Alles geklärt: ausliefern (Ship). [tweet-2112047997987213449](../sources/tweet-2112047997987213449.md)
- Lösbares Problem: direkt zur Codeerzeugung zurückkehren und die Prüfstrecke erneut durchlaufen. [tweet-2112047997987213449](../sources/tweet-2112047997987213449.md)
- Neuartiges Problem: menschliches Review einschalten, danach zur Codeerzeugung zurückkehren. [tweet-2112047997987213449](../sources/tweet-2112047997987213449.md)

Die Grafik macht Selbstprüfung, unabhängiges Zweitreview und automatische Checks zu getrennten Kontrollstufen; sie nennt keine konkreten Prüfkommandos, Rundengrenze oder Kriterien für „neuartig“. Ihre Wirksamkeit ist hier nicht getestet. Der Nutzer behält den Loop ausdrücklich als nützliche Arbeitsanleitung. [tweet-2112047997987213449](../sources/tweet-2112047997987213449.md)
