---
tags: [agents, product-building]
sources: [tweet-2054568935274549597.md, tweet-2079610838143623371.md, tweet-2105290458541011269.md, tweet-2046098017984344065.md, tweet-2111497336723583165.md]
created: 2026-10-01
updated: 2026-10-23
---

# Personalized LLM Workflows

## Profil und dauerhafte Instruktionen (Stand 2026-05)

Der gespeicherte Claude-Leitfaden empfiehlt einen Project-Workspace statt ständig neu erklärter Einzelchats. Sein Profiltemplate fragt Name, Beruf, zwei bis drei Hauptaufgaben, ein bis drei aktuelle Ziele, Anwendungsfälle, Vorwissen, bevorzugte Informationsform, unerwünschte Antwortmuster und Interessengebiete ab. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)

Aus diesem Profil soll Claude Project Instructions unter 400 Wörtern in der zweiten Person erzeugen: Rolle und Arbeit des Nutzers, Standardformat, Ton, verbotene Antwortmuster und wiederkehrende Verhaltenswünsche. Das ist ein wiederverwendbares Briefingverfahren, keine Garantie vollständiger automatischer Erinnerung in allen Chats. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)

## Klärung, Stil und Gegenprüfung (Stand 2026-05)

- Vor einer wichtigen Aufgabe soll Claude die fünf wichtigsten Fragen stellen und erst nach den Antworten beginnen; das Cold-Email-Beispiel fragt nach den konkreten Voraussetzungen einer passenden Nachricht. Damit werden wie bei [Agent Unknowns](Agent%20Unknowns.md) fehlende Angaben sichtbar. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)
- Drei bis fünf eigene Textbeispiele dienen als Stilreferenz. Der Analyseprompt nennt Satzlänge, Rhythmus, Wortwahl, Absatzanfänge/-enden, Auslassungen und Formalität; erst danach soll ein neuer Text diesen Mustern folgen. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)
- Für eine Entscheidung fordert ein Prompt zuerst Angriff auf Annahmen und mögliche Fehler, dann den stärksten Fall zugunsten des Plans und zuletzt ein Urteil. Das Geschäftsideen-Template konkretisiert Zielkunde, Erlösmodell, Wettbewerber, Zahlungsbereitschaft, notwendige Voraussetzungen und das größte Einzelproblem. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)
- Ein Metaprompt lässt für die tatsächliche Aufgabe Rolle, Kontext, Format und Grenzen entwerfen und anschließend anwenden; Ausgabegrenzen wie drei Sätze, fünf Punkte oder unter 150 Wörter sowie Regeln gegen Vorrede und Wiederholung begrenzen die Antwortform. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)

## Vollständig gespeicherte Anwendungsvorlagen (Stand 2026-05)

- Analogielernen: Alltagssprache statt Fachjargon, nach jeder Analogie eine Verständnisfrage, Anpassung an die Antwort und Fortsetzung bis zur eigenen Erklärung. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)
- Reiseplanung: Ziel, Tage, Tagesbudget inklusive Unterkunft, Reisetempo, Interessen und Ausschlüsse angeben; Tagesplan mit Unterkunft, Aktivitäten, Essen, Logistik und Reservierungsbedarf verlangen. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)
- Ausgabenanalyse: tatsächliche Monatsdaten und eigene Ziele bereitstellen; größte Kategorien, auffällige Abweichungen, mögliche Einsparungen, relevante Unterausgaben und eine konkrete Änderung abfragen. Das Template ist kein Beleg für die Richtigkeit daraus erzeugter Finanzurteile. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)
- Selbstreflexion: zuerst Situation, Gefühle, bisherige Versuche und gewünschtes Ergebnis klären, anschließend Wahrgenommenes zurückspiegeln und erst dann eine Perspektive geben. Der Artikel grenzt dies ausdrücklich von Therapie ab. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)

## Sprachbriefing als weitere Methode (Stand 2026-07)

Karpathy empfiehlt aus eigener Erfahrung ungefähr zehn Minuten ungeordnete Spracheingabe über /voice, wenn das Modell mehr Kontext braucht und Tippen zu aufwendig ist. Optional kündigt er Erkennungsfehler an oder führt ein kurzes Interview; das Modell soll die Gedanken anschließend klarer rekonstruieren. Welcher Client /voice bereitstellt, sagt der Note-Tweet nicht. [tweet-2079610838143623371](../sources/tweet-2079610838143623371.md)

Seine Beobachtung weniger späterer Korrekturen ist ein Erfahrungsbericht ohne Messreihe oder Beispieltranskript. Der gesamte Note-Tweet ist als Quelle gespeichert, nicht nur das abgeschnittene full_text. [tweet-2079610838143623371](../sources/tweet-2079610838143623371.md)

## Grenzen der Produkt- und Sparbehauptungen (Stand 2026-05)

Der Leitfaden empfiehlt frische Chats für neue Themen, behaltenes Projektprofil und Thinking für schwierige Fragen. Sein behaupteter Nullkontext in jedem neuen Chat, pauschale 10-Prozent-Nutzung, 80-Prozent-Nutzenverlust und 40–60 Prozent Tokenersparnis sind nicht durch Messdaten oder einen aktuellen Herstellerabgleich belegt; die Prozentzahlen werden nicht als Leistungswerte übernommen. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)

Der vollständige Artikel enthält die konkreten Profil- und Anwendungsprompts; die gespeicherte Oberfläche und das Thinking-Verhalten sind kein aktuell geprüfter Funktionsvertrag. [tweet-2054568935274549597](../sources/tweet-2054568935274549597.md)

## Geschäftskontext durch ein adaptives Interview (Stand 2026-09)

EXM7777 teilt eine komplette Bildvorlage: jeweils eine kurze Frage stellen, die nächste aus der Antwort ableiten, konkrete Beispiele fordern und bei Geld, Zeit, Risiko, Wiederholung oder Reibung vertiefen. Der Interviewinhalt ergänzt das Profilbriefing und [Context Engineering](Context%20Engineering.md) um Rollen, Arbeitsabläufe und Delegation. [tweet-2105290458541011269](../sources/tweet-2105290458541011269.md)

Vollständige Transkription des gespeicherten Prompts (Zeilenumbrüche normalisiert): [tweet-2105290458541011269](../sources/tweet-2105290458541011269.md)

```text
<goal>
Learn enough about me and my business to become a high-value operator, strategist, and assistant.
Understand my goals, business model, team, workflows, decisions, constraints, tools, recurring tasks,
weak spots, and bottlenecks.
</goal>

<method>
Ask one short, high-value question at a time. Use each answer to decide what to ask next. Go deeper
where there is money, time, risk, repetition, friction, or unclear thinking. Ask for concrete examples.
Challenge vague answers and assumptions. Look for patterns, inefficiencies, missing systems,
unnecessary manual work, and things I am doing that should be delegated or automated.
</method>

<focus>
Understand:
- what the business does and how it makes money
- my role and what I spend time on
- my current goals and priorities
- key customers, products, channels, and operations
- how decisions are made
- what slows growth
- where mistakes happen repeatedly
- what depends too much on me
- what tasks repeat every day or week
- what could be automated, delegated, standardized, or removed
- what information I regularly need
- what tools, software, and workflows I use
- where communication breaks down
- what I avoid, delay, or overthink
- what creates the most leverage
- where you should challenge me vs. just execute
</focus>

<weak_spots>
Actively look for bottlenecks, wasted time, manual processes, unclear ownership, poor follow-up,
repeated decisions, missing dashboards or information, inefficient communication, unnecessary
meetings...
</weak_spots>

<finish>
When you have enough context, stop interviewing me. Save everything into your memory, include:
how I work, how the business works, priorities, bottlenecks, automation opportunities, delegation
opportunities, useful systems, important context to remember, how you should work with me, open
questions. Do not invent anything. Mark uncertainty clearly.
</finish>
```

Der Abschluss fordert eine Zusammenfassung von Arbeitsweise, Geschäft, Prioritäten, Engpässen, Automatisierungs-/Delegationschancen und offenen Fragen; nichts erfinden und Unsicherheit markieren. Die Aufforderung zur Speicherung garantiert keine produktübergreifende oder vollständige Erinnerung. Die Werbeaussagen 200 IQ und perfect memory sind nicht gemessen. [tweet-2105290458541011269](../sources/tweet-2105290458541011269.md)

## Sieben Gesprächsanweisungen für Claude (Stand 2026-04)

AYi teilt die folgenden konkret nutzbaren Formulierungen; die deutsche Fassung übersetzt den gespeicherten chinesischen Text. Es sind Prompt-Vorschläge des Autors, keine bestätigten universellen Qualitätsregeln. [tweet-2046098017984344065](../sources/tweet-2046098017984344065.md)

1. Gewünschtes Verhalten positiv beschreiben: „Schreibe in kurzen, kräftigen Sätzen“ statt nur lange Sätze zu verbieten. [tweet-2046098017984344065](../sources/tweet-2046098017984344065.md)
2. Widerspruch ausdrücklich erlauben: „Wenn du einen besseren Blickwinkel siehst, widersprich mir direkt“ oder „Sag mir, ob ich die falsche Frage stelle“. [tweet-2046098017984344065](../sources/tweet-2046098017984344065.md)
3. Mit einer klaren, respektvollen Aufgabe beginnen: „Lass uns dieses Problem gemeinsam lösen; ich traue dir hochwertige Vorschläge zu.“ [tweet-2046098017984344065](../sources/tweet-2046098017984344065.md)
4. Fehler mit Fakten korrigieren: „Hier liegt eine sachliche Abweichung vor; passe den nächsten Schritt anhand der Daten X an.“ [tweet-2046098017984344065](../sources/tweet-2046098017984344065.md)
5. Wiederholte Entschuldigungen unterbrechen: „Kein Problem, weiter; die nächste Aufgabe ist …“. [tweet-2046098017984344065](../sources/tweet-2046098017984344065.md)
6. Neben Ausführung eine eigene Einschätzung verlangen: „Wie würdest du vorgehen, wo könnte es Reibung geben und was habe ich übersehen?“ [tweet-2046098017984344065](../sources/tweet-2046098017984344065.md)
7. In langen Gesprächen die positive Rahmung gelegentlich erneuern: „Bisher läuft es gut; behalte diesen Rhythmus bei.“ Der behauptete Reset des Modellzustands ist nicht belegt. [tweet-2046098017984344065](../sources/tweet-2046098017984344065.md)

Als Zusatz nennt der Post „assume competence“, für kreative Aufgaben „be bold, take swings, even if speculative“ sowie einen neuen Chat, wenn sich viele Korrekturen im selben Verlauf angesammelt haben. Die Kreativanweisung erlaubt Spekulation, macht spekulative Antworten aber nicht zu Fakten. [tweet-2046098017984344065](../sources/tweet-2046098017984344065.md)

Der Autor führt die Tipps auf ein Amanda-Askell-Interview zurück; dessen Video liegt in diesem Bookmark nicht vor. Aussagen über Angst, Abwehr oder eine durch Lob verbesserte Modellleistung sind Zuschreibungen beziehungsweise Wirkungsbehauptungen ohne hier gespeicherte Versuchsbelege. Das Logo-Bild enthält keine zusätzlichen Regeln. [tweet-2046098017984344065](../sources/tweet-2046098017984344065.md)

## Persönliches AIOS als vier Schichten (Stand 2026-10; eingebettete Beispiele aus 2026-04)

Nate Herks im Oktober weiterverbreiteter Kurs nennt Context, Connections, Capabilities und Cadence als vier aufeinander aufbauende Schichten: persönlicher und geschäftlicher Kontext, Zugang zu Arbeitsdaten, wiederholbare Fähigkeiten und schließlich geplante Ausführung. Seine drei M heißen Mindset, Method und Machine. Der Kurs ist ein Arbeitsablauf, kein Betriebssystem im technischen Sinn. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)

### Bestand aufnehmen und Kontext aufbauen

1. Quellen nach Revenue, Customer, Calendar, Comms, Tasks, Meetings und Knowledge sammeln. Mit den wichtigsten beginnen; eine Integration wird nur gebraucht, wenn sie tatsächlich benötigte Daten oder Aktionen erschließt. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)
2. Einen Arbeitsordner mit CLAUDE.md, context/, decisions/, references/, archives/ und .claude/skills/ anlegen. Das gezeigte Onboarding fragt unter anderem nach Geschäft, unveränderten Schreibbeispielen und aktuellen Prioritäten und schreibt daraus dauerhafte Kontextdateien. Der Starter ist nur über die Community erwähnt; ein direkter Repository-Link fehlt. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)
3. audit prüft die vier Schichten; level-up fragt nach Wiederholungen, lästiger Handarbeit, delegierbaren Tätigkeiten, dem ersten Engpass bei starkem Wachstum und möglichen Wachstumshebeln. Die gezeigte Punktzahl ist eine Agentenbewertung, kein objektiver Reifegrad. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)

### Verbindungen und wiederholbare Fähigkeiten

Der Sprecher zeigt für ClickUp ein eigenes Agentenkonto statt seines Hauptkontos und empfiehlt aufgabengerechte Berechtigungen. API-Schlüssel gehören in eine ausdrücklich ausgeschlossene lokale Datei beziehungsweise in die Secret-/Umgebungsverwaltung der Laufzeit; ein führender Punkt in .env verhindert Git-Tracking nicht automatisch. Im gezeigten Test wird eine gewünschte Direktnachricht fälschlich als Aufgabe angelegt: Zugriff allein garantiert keine richtige Aktion. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)

Wiederkehrende API-Recherche soll in einer lokalen Referenzdatei landen; ein konkreter Skill nennt nur seine benötigten Endpunkte und stabilen IDs. Damit entfällt die wiederholte Suche durch den gesamten Tool-Katalog. Die pauschale Behauptung, APIs seien immer tokenärmer als MCP, ist kein gemessener allgemeiner Vergleich. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)

Der Skill-Aufbau besteht aus sechs Teilen: Name/Trigger, überprüfbares Ziel, geordnete Schritte, notwendige Referenzen, Regeln und Verbesserungsschleife. Zunächst einen echten Ablauf gemeinsam ausführen, danach als Skill speichern; die ersten Läufe beobachten und Fehler an der passenden Stelle korrigieren. Name und Beschreibung dienen der Auswahl, der Haupttext dem gewählten Ablauf und Zusatzdateien werden nur bei Bedarf gelesen. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)

Das Infografik-Beispiel trennt Bildgenerierung vom deterministischen Overlay des echten Logos. Für falsche Schritte wird die Anweisung geändert, für fehlenden Stil Kontext ergänzt, für wiederkehrende Fehler eine Regel hinzugefügt und für wiederholte Tool-Recherche eine Referenz angelegt. Lokale Skills gelten im Projekt, globale im Benutzerverzeichnis. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)

### Cadence, Wiki und tägliche Pflege

Der Kurs trennt sitzungsgebundene Loops, lokale geplante Aufgaben und Cloud-Routinen. Cloud-Beispiele klonen ein Repository und brauchen gesonderte Umgebungsvariablen, Netzwerkfreigaben und gegebenenfalls Setup; lokale .env-Dateien, Browser-Cookies und außerhalb des Repositories liegende Dateien sind dort nicht automatisch vorhanden. Ein Run soll vor unbeaufsichtigter Wiederholung manuell geprüft werden. Die eingebetteten Clips nennen April 2026; Quoten, Preise, Intervall- und Laufzeitlimits sind historische Sprecherangaben und keine aktuellen Konfigurationsempfehlungen. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)

Eine ergänzende [Markdown-Wiki](LLM%20Wiki%20Pattern.md)-Schicht trennt Raw und Wiki, pflegt Index und Log und verknüpft Quellen mit Themen. Obsidian zeigt die Beziehungen, ist aber nicht die Datengrundlage. Ein kleiner Hot Cache ist für häufige persönliche Fakten optional; bei großen Dokumentbeständen nennt der Kurs weiterhin Retrieval-Systeme als sinnvolle Alternative. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)

Die tägliche Schleife lautet: morgens mit Prioritäten und Arbeitsdaten planen, abends fehlenden Kontext und nötige Korrekturen notieren, regelmäßig Skills und Verbindungen auditieren. Dashboards zuerst als kleinen Prototyp testen. Häufige, klar definierte Teilaufgaben können als deterministische Skripte laufen; ein autonomer Agent ist dafür keine Voraussetzung. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)

Grenzen: Werbeaussagen über perfekte Erinnerung, automatische Fehlerfreiheit, Produktivitätsgewinne und Zeitersparnis sind nicht belegt. Der Kurs enthält ältere eingebettete Tutorials und bewirbt eine Community sowie ein Diktierprodukt; es wurde hier weder Software installiert noch eine Verbindung eingerichtet. [tweet-2111497336723583165](../sources/tweet-2111497336723583165.md)
