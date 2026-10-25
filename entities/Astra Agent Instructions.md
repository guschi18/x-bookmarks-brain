---
tags: [agents, tools]
sources: [tweet-2101956340877000754.md]
created: 2026-10-03
updated: 2026-10-03
---

# Astra Agent Instructions

## Überblick (Stand 2026-09)

argofowl teilt als Bild seine aktuelle AGENTS.md, die er als Arbeitsvereinbarung für Agenten ("how to talk to me, do the work, delegate and verify") beschreibt und weiter anpasst. Persönliche Angaben und Pfade sind durch Platzhalter geschwärzt. [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md)

Ein zitierter früherer Post nennt Astra nach Überarbeitung der Datei "ziemlich solide" und etwas besser als Fable 5.1, mit dem Hinweis, das sei umstritten. Das ist eine persönliche Einschätzung ohne Messung. [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md) Siehe [Fable](Fable.md).

## Aufbau der Datei

Das Bild zeigt sieben Abschnitte. [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md)

- Vorstellung: Solo-Entwickler und Designer für macOS-, Electron- und Webprodukte; Wert auf UI, Animation, sauberen Code und offizielle Dokumentation; Projektverzeichnisse als Platzhalter. [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md)
- Ansprache: einfache, nicht-technische Sprache, knapp, keine Gedankenstriche in erzeugten Inhalten wie E-Mails oder App-Texten (Chat und Code ausgenommen). [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md)
- Prompts lesen: Eingaben werden oft diktiert, daher die gemeinte Absicht beachten statt des Wortlauts. [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md)
- Arbeitsweise: gewünschtes Ergebnis aus Anfrage und Kontext ableiten und übliche Zwischenschritte im Auftragsumfang miterledigen; Routineunsicherheit durch Inspektion lösen und nur bei wesentlicher, nicht ableitbarer Lücke fragen, währenddessen unabhängig weiterarbeiten; Zwischenartefakt oder bestandener Build zählt erst als fertig, wenn das Ergebnis erfüllt ist; bei Performance zuerst den realen Engpass messen und Vorher-/Nachher-Zahlen berichten. [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md)
- Delegation: Astra entscheidet, prüft und integriert und erledigt kleine Aufgaben selbst; größere, klar umrissene Umsetzungen gehen an Sol (gpt-5.6-sol, mittleres Reasoning, fork_turns="none") mit ausreichend Kontext zur eigenständigen Umsetzung und Prüfung. [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md)
- Verifikation: nach jeder sinnvollen Änderung das Ergebnis prüfen, das der Nutzer wirklich verwendet; bei visuellen Aufgaben die tatsächliche Ausgabe im Zielkontext ansehen, Build und Code-Review genügen nicht; gefundene Probleme beheben und erneut prüfen, Unverifiziertes samt Grund melden; vor dem Ende Ergebnis mit Originalauftrag und späteren Korrekturen vergleichen und einen offensichtlich fehlenden Schritt im erlaubten Umfang nachholen. [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md)
- Umgebung: Todo- und Notiz-App per CLI nutzen; Dev-Server zuerst in einer Port-Registry nachsehen, expliziten Port festlegen (--strictPort), gesunde Server mit passendem Projektverzeichnis wiederverwenden und nie per Namensmuster, nur eigene PIDs beenden; ein zweiter Mac über Tailscale wird nicht durch lokale Simulation ersetzt. [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md)

## Grenzen

Die Datei liegt nur als Bild vor; der Post verlinkt nichts weiter. Ob sie die Agentenqualität verbessert, ist nicht gemessen. Verwandt: [Codex Astra Luna Orchestrator](Codex%20Astra%20Luna%20Orchestrator.md). [tweet-2101956340877000754](../sources/tweet-2101956340877000754.md)
