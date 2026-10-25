---
tags: [agents, tools, marketing]
sources: [tweet-2111229504874246441.md]
created: 2026-10-23
updated: 2026-10-23
---

# Earshot

## Rolle und Zeitstand (Stand 2026-10)

[earshot](https://github.com/Leonxlnx/earshot) ist laut gespeicherter README ein CPU-basiertes Werkzeug, das Klang für Coding-Agenten beschreibbar, vergleichbar und bearbeitbar macht. Es bietet CLI, Python-API und MCP-Server. [tweet-2111229504874246441](../sources/tweet-2111229504874246441.md)

Der Post vom 16. Oktober kündigt v0.2 an; die später gespeicherte README beschreibt bereits 0.3 samt Soundbank und Film-Kits. Der Post belegt daher keine aktuelle neueste Version. Der auf [Cinetic](Cinetic.md) dokumentierte neuere Integrationsstand bleibt maßgeblich für dessen Versionsvoraussetzungen. [tweet-2111229504874246441](../sources/tweet-2111229504874246441.md)

## Hören und prüfen (Stand 2026-10)

Die Kommandos describe, match, rank und find beschreiben Einzelklänge, bewerten Beschreibungen, vergleichen Kandidaten und finden passende Zeitabschnitte. timeline und sheet verbinden Ereignisse, Lautheit und Timing mit einer Timeline beziehungsweise einer beschrifteten Grafik. critique vergleicht einen Film mit einem Referenzprofil; measure liefert Messwerte ohne Modelle. [tweet-2111229504874246441](../sources/tweet-2111229504874246441.md)

Für wiederholte Aufrufe empfiehlt die README MCP oder eine Python-Sitzung, damit Modelle geladen bleiben; einzelne CLI-Prozesse laden sie jeweils neu. LLM-Kritik mit Gemini ist optional und verlangt einen eigenen Schlüssel sowie ausdrückliche Upload-Freigabe. [tweet-2111229504874246441](../sources/tweet-2111229504874246441.md)

## Klang erzeugen und als Code rekonstruieren (Stand 2026-10)

forge rendert parametrisierte Syntheserezepte, bewertet Kandidaten und variiert sie. fit passt ein Synthesemodell an eine Aufnahme an und schreibt ein ausführbares Rezept, dessen Parameter weitere Takes oder Morphs ermöglichen. Ein Fit ist laut README ein Derivat seiner Aufnahme; deren Lizenz bleibt zu beachten. [tweet-2111229504874246441](../sources/tweet-2111229504874246441.md)

Die README beschreibt eine Bank von 201 in Code gespeicherten Effekten. sfx rendert einzelne Effekte mit Dauer, Ziel-Peak oder geeigneten Tonhöhenparametern; kit ordnet Rollen konkrete Klänge zu und speichert vermessene Synchronpunkte. Diese Zahlen und Genauigkeitsangaben stammen aus der Projektdokumentation. [tweet-2111229504874246441](../sources/tweet-2111229504874246441.md)

## Voraussetzungen und Grenzen (Stand 2026-10)

Die Installation benötigt Python 3.10+, ffmpeg/ffprobe und beim ersten Modellaufruf laut README ungefähr 1,1 GB für CLAP und AST. Nach dem Download werden die angepinnten Modelle lokal geladen; Offline-Variablen verhindern Nachladen und lassen fehlenden Cache als Fehler sichtbar werden. Code und Modellgewichte haben getrennte Lizenzen. [tweet-2111229504874246441](../sources/tweet-2111229504874246441.md)

Die eigene Suche optimiert die eigenen Kritiker und kann deren Bewertungen ausnutzen. Die README warnt ausdrücklich vor diesem Goodhart-Effekt, kleinen Blindtests und begrenzten Referenzprofilen. Geschmack, Emotion, Sprachinhalt, Herkunft und Lizenzen werden nicht zuverlässig beurteilt; Autorenbenchmarks sind keine unabhängige Qualitätsprüfung. Das Demo-Transkript ist leer; hier wurde kein Klang angehört oder erzeugt. [tweet-2111229504874246441](../sources/tweet-2111229504874246441.md)
