---
tags: [agents, tools]
sources: [tweet-2097178140413972948.md]
created: 2026-10-03
updated: 2026-10-03
---

# Hook-Enforced Model Routing

## Muster

Der Post beschreibt ein berichtetes Spotify-Setup für [Claude Code](../entities/Claude%20Code.md): Der Großteil der Agentenarbeit sei Handarbeit statt Denken, etwa mehrere große Dateien öffnen, um eine Konfiguration zu finden, oder Dutzende ähnliche Tests nach Vorlage schreiben. Diese Arbeit werde zu den Höchstpreisen des stärksten Modells abgerechnet. [tweet-2097178140413972948](../sources/tweet-2097178140413972948.md)

Drei Mechanismen: (1) Ein Hook stoppt jede Leseanfrage über 350 Zeilen vor der Ausführung; (2) die gestoppte Datei geht an ein günstiges Modell, das strukturierte Stichpunkte statt Quellcode zurückgibt; (3) ein günstiges Modell erzeugt wiederholten Vorlagencode aus einem Beispiel, entfernt Formatierungsmarker und schreibt ihn still auf die Platte, ohne dass das teure Modell ihn sieht. [tweet-2097178140413972948](../sources/tweet-2097178140413972948.md)

## Weiche Regel gegen harte Sperre

Der zitierte Post sagt, Regeln als Anweisungen seien vom Modell ignoriert worden; erst die Sperre vor dem Öffnen habe gewirkt: "Written rules are a suggestion. A block is not." Der chinesische Post folgert, Prompts sollten nicht um Sparsamkeit bitten, sondern der Code solle sie erzwingen. [tweet-2097178140413972948](../sources/tweet-2097178140413972948.md)

## Grenzen und Evidenz

Editieren und komplexes Schließen bleiben beim teuren Modell, weil Edits die echte Datei brauchen. Im Test habe der günstige Worker einen Fehler übersehen, den das teure Modell in Sekunden fand; der chinesische Post nennt ihn einen Thread-Sicherheitsfehler. [tweet-2097178140413972948](../sources/tweet-2097178140413972948.md)

Die 90 Prozent Einsparung stehen in den Posts ohne Messmethode. Die Primärquelle, ein Spotify-Engineering-Artikel zu "Portal by Spotify" (Dimitri Mazmanov, 2026-09-03; Nutzer-Nachtrag, per Zusammenfassung abgerufen), nennt Benchmarks auf einem Java-Monorepo in vier Szenarien mit im Mittel rund 90 Prozent Ersparnis beim Massenlesen, aber keine Angaben zu Ausgangswert, Stichprobe oder Zeitraum. Die Rede von einer "vollständig öffentlichen internen Architektur" geht über den Artikel hinaus: Er beschreibt ein Werkzeug, kein Spotify-weites Setup. [tweet-2097178140413972948](../sources/tweet-2097178140413972948.md)

## Aufbau laut Spotify-Artikel (Nutzer-Nachtrag 2026-10-03)

- Drei Schichten: PreToolUse-Hooks sperren übergroße Lesezugriffe und fangen Bash-Befehle auf große Dateien ab; die Wrapper-Skripte `bulk-read` und `code-write` rufen Portal-CLI-Aktionen auf; Skills (Markdown) zeigen Claude, wann und wie. [tweet-2097178140413972948](../sources/tweet-2097178140413972948.md)
- Der Hook "check-file-size" leitet Lesezugriffe über der Schwelle (Standard 350 Zeilen, einstellbar über die Umgebungsvariable `SHUNT_MIN_LINES`) auf den Bulk-Reader um; gezielte Lesezugriffe mit Offset laufen unverändert durch. Als Worker-Modell dient in den Beispielen Gemini 2.5 Flash, austauschbar. [tweet-2097178140413972948](../sources/tweet-2097178140413972948.md)
- Der Artikel betont, Editieren und Schlussfolgern ließen sich nicht delegieren; Debugging, Architekturentscheidungen und sicherheitskritischer Code bleiben bei Claude. Der Worker habe einen subtilen Thread-Sicherheitsfehler übersehen, den Claude in Sekunden fand. [tweet-2097178140413972948](../sources/tweet-2097178140413972948.md)
- Delegierte Antworten dauern laut Artikel 10 bis 30 Sekunden; ein Aufruf ist auf 30 Sekunden begrenzt. Als Kontext nennt er Tokenkosten von 200 bis 500 Dollar je Entwickler und Monat, teils über 2.000 Dollar. [tweet-2097178140413972948](../sources/tweet-2097178140413972948.md)

Einordnung neben anderen Sparbehauptungen: [AI Coding Cost Claims](AI%20Coding%20Cost%20Claims.md). Eine Rollenteilung per Konfiguration statt Hook zeigt [Codex Astra Luna Orchestrator](../entities/Codex%20Astra%20Luna%20Orchestrator.md). [tweet-2097178140413972948](../sources/tweet-2097178140413972948.md)
