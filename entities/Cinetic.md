---
tags: [agents, tools, marketing, product-building]
sources: [tweet-2106891315371737480.md, tweet-2111618614444892331.md, tweet-2111229504874246441.md]
created: 2026-10-12
updated: 2026-10-23
---

# Cinetic

## Rolle und Installation (Stand 2026-10)

[Cinetic](https://github.com/Leonxlnx/cinetic) ist Leon Lins Agent-Skill für Launchfilme, Produktclips, Feature-Loops und Logo-Stings aus Code. Der Agent soll eine Filmidee entwickeln und Regie führen, statt nur Animationskomponenten anzuordnen; installiert wird mit npx skills add Leonxlnx/cinetic. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)

## Dokumentierter Ablauf (Stand 2026-10)

1. Brief und drei unterschiedliche Konzepte entwickeln, prüfen und eine tragende Storyidee wählen. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)
2. Aus drei Markenadjektiven oder der vorgegebenen Marke Typografie, Farbe, Bildwelt und Logo ableiten; Style-Stills vor der Animation prüfen. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)
3. Techniken aus einer Bibliothek von laut README 273 Einträgen in 14 Kategorien ziehen; Format und Energie gewichten die Auswahl, ein Seed macht sie reproduzierbar. Nicht passende Techniken werden mit Begründung verworfen oder neu gezogen. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)
4. Bild, Musik und Effekte an einer gemeinsamen timeline.ts und einem Beat-Grid ausrichten; Kontaktframes, Auftauchzeitpunkte und Geschwindigkeitsmaxima bestimmen Ton-Cues. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)
5. Vorschau und Master rendern; Contact Sheets, Pixelprüfungen, Ton-Synchronitätsaudit und Kritikrunden führen zum dokumentierten Ship-Gate. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)

Remotion/React ist der Standard, [HyperFrames](HyperFrames.md)/HTML/GSAP der alternative Renderer. BRIEF.md, TREATMENT.md und Filmcode halten Vorgaben, Beat-Sheet, Copy und Timing nachvollziehbar; Social-Formate werden neu angeordnet statt nur beschnitten. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)

## Wiederverwendbare Briefs und Formate (Stand 2026-10)

Die vollständige Source enthält vier konkrete Briefs: Kiln als 25-Sekunden-Launchteaser, Quire als 12-Sekunden-Hochformatclip mit Markenfarben, Ledgerly als stummen 10-Sekunden-Feature-Loop und Halden als 6-Sekunden-Logo-Sting mit Transparenzvarianten. Weitere Nutzungsbeispiele decken Walkthroughs, Social-Varianten und Review bestehender Remotion-Filme ab. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)

## Voraussetzungen und Aufwand (Stand 2026-10)

Die README nennt Node 22+, FFmpeg 6+, Python 3.11 samt Medien-/Analysepaketen und Chromium. Die Skripte setzen macOS oder Linux/Bash voraus; Windows über WSL2 ist ein ungeprüfter Vorschlag. Die Remotion-Lizenz ist separat von der MIT-Lizenz des Skills zu prüfen. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)

In der eigenen letzten Evaluationsrunde meldet der Autor durchschnittlich 95 Minuten und 626k Tokens gegenüber 33 Minuten und 231k beim Baseline-Agenten. Neutrale Juroren bevorzugten zwei von vier Cinetic-Filmen; hausinterne Stiljuroren vier von vier. Die veröffentlichte 1.0.0-Fassung hatte nach weiteren Korrekturen keine eigene Runde. Das belegt weder generell bessere Filmqualität noch Einsparungen. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)

## Beziehung (Stand 2026-10)

Cinetic erweitert [Agentic Video Production](../concepts/Agentic%20Video%20Production.md) um einen eigenen Regie- und QA-Pfad. [Product Film Skill](Product%20Film%20Skill.md) und [No Slop Motion](No%20Slop%20Motion.md) verfolgen verwandte Ziele, haben aber andere Repositories und Abläufe; sie sind keine weiteren Belege für dieselbe Implementierung. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)

## Version 1.1 und gemessener Sound (Stand 2026-10)

Leon Lin nennt für Cinetic 1.1 kürzere Textelemente, ruhigeres Standardtempo und mit [earshot](https://github.com/Leonxlnx/earshot) in Code erzeugte Sounds. Die aktualisierte README dokumentiert Textfragmente mit lesbaren Haltezeiten und Bildpausen, einen ruhigen Standard und ein optionales energetischeres Profil. [tweet-2111618614444892331](../sources/tweet-2111618614444892331.md)

Der Sound-Pfad legt pro Rolle einen Klang im Film-Kit fest; earshot rendert und vermisst die Takes, danach werden Onset beziehungsweise Whoosh-Peak an die aus dem Bildcode berechneten Cue-Frames gesetzt. Für textgeführte Filme beschreibt die README einen leisen Ton je Fragment, Lesepausen und einen hervorgehobenen Reveal statt dauernder Effektlagen. [tweet-2111618614444892331](../sources/tweet-2111618614444892331.md)

Wenn earshot fehlt, nutzt der Ablauf vorhandene Kit-Takes und zuletzt synthetisierte Effekte mit Warnung. Die README nennt earshot 0.3+ als optional, empfiehlt eine eigene Python-Umgebung mit EARSHOT_PYTHON und einen angepinnten Installationsaufruf npx skills add Leonxlnx/cinetic#v1.1.0. Keine Installation oder audiovisuelle Qualitätsprüfung wurde hier ausgeführt; das beigefügte Demo-Transkript ist leer. [tweet-2111618614444892331](../sources/tweet-2111618614444892331.md)

## Eigenständiger Audiopfad (Stand 2026-10)

[Earshot](Earshot.md) dokumentiert neben Film-Kits auch lokale Klangbeschreibung, Kandidatenvergleich, Synthese mit forge und Audio-zu-Code mit fit. Diese eigenständigen Werkzeuge ergänzen die Cinetic-Integration; der earshot-v0.2-Post vom 16. Oktober ist kein Ersatz für die neuere Cinetic-Versionsvoraussetzung. Die gespeicherte earshot-README enthält bereits 0.3-Funktionen. [tweet-2111229504874246441](../sources/tweet-2111229504874246441.md)
