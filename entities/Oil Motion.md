---
tags: [tools, agents, product-building]
sources: [tweet-2085905362260312379.md]
created: 2026-10-12
updated: 2026-10-12
---

# Oil Motion

## Rolle (Stand 2026-08; gespeicherter README-Stand)

https://github.com/oil-oil/oil-motion ist ein MIT-lizenzierter Agent-Skill für interaktive Webanimationen aus AI-generierten Videos. Eingaben wie Scrollen, Maus, Drag, Touch oder Geräteorientierung steuern vorbereitete Animationsressourcen; im Browser wird bei der Interaktion kein neues Video generiert. [tweet-2085905362260312379](../sources/tweet-2085905362260312379.md)

## Wiederverwendbarer Ablauf

1. Referenzen, Ausdrucksziel, Subjekt, Hintergrund, Eingabe und Zeitsteuerung festlegen; Anfang, Zwischenzustände und Ende als Keyframes prüfen. [tweet-2085905362260312379](../sources/tweet-2085905362260312379.md)
2. Kontinuierliche Aktionen zwischen den bestätigten Frames generieren. Translation, Skalierung, Zuschnitt, Tempo und Dämpfung bleiben programmatisch steuerbar. [tweet-2085905362260312379](../sources/tweet-2085905362260312379.md)
3. Pausen, nahe Duplikate, Flackern und Strukturfehler frameweise prüfen; nach tatsächlicher Darstellungsgröße komprimieren. [tweet-2085905362260312379](../sources/tweet-2085905362260312379.md)
4. Ressourcenbudget und Zugriffsform bestimmen: gebackene Szenen als MP4, kleine transparente oder zweidimensionale Ressourcen als Alpha-WebP-Atlas, große transparente eindimensionale Zeitleisten als Green-Screen-MP4 mit WebGL-Keying. [tweet-2085905362260312379](../sources/tweet-2085905362260312379.md)
5. Einen kurzen Pilot auf der echten Seite abnehmen, dann weitere Segmente erzeugen; die gespeicherte README beschreibt Hash-/Endframe-Prüfungen vor Netzwerkaufrufen. [tweet-2085905362260312379](../sources/tweet-2085905362260312379.md)

## Qualität und Grenzen

Die README verlangt Identitäts-/Strukturkontinuität, saubere transparente Kanten, Tests bei schneller Umkehr und Rotation sowie statische Fallbacks bei Ladefehlern und reduzierter Bewegung. Falsche Anatomie oder Bewegungsrichtung muss neu generiert werden; sie lässt sich nicht durch bloße Frameaufbereitung heilen. Für zweidimensionale Blickrichtungen reicht ein einzelner horizontaler Videopfad nicht. [tweet-2085905362260312379](../sources/tweet-2085905362260312379.md)

Generierung benötigt einen API-Key; die README behauptet lokale Schlüsselspeicherung. Skripte, Integrationen, Qualität und Budgetgrenzen wurden hier nicht ausgeführt. Spätere README-Details sind kein Nachweis des vollständigen Funktionsumfangs am Tag des August-Posts. Der Ansatz ergänzt [Design Skills for Coding Agents](../concepts/Design%20Skills%20for%20Coding%20Agents.md) und [Agentic Video Production](../concepts/Agentic%20Video%20Production.md) um kontrollierte Webressourcen. [tweet-2085905362260312379](../sources/tweet-2085905362260312379.md)
