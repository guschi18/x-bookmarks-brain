---
tags: [product-building, tools]
sources: [tweet-2068064010600108267.md, tweet-2075929554594500772.md, tweet-2075545587093807111.md, tweet-2030433563770855683.md, tweet-2083898950755471520.md, tweet-2097134648270766520.md, tweet-2098224649762984168.md, tweet-2093580756564189238.md, tweet-2093397349309509899.md, tweet-2093377750707142698.md, tweet-2093304387430944807.md, tweet-2092994294282060147.md, tweet-2092979876718379436.md, tweet-2092979873476215219.md, tweet-2092979866836648104.md, tweet-2092609257338200469.md, tweet-2091703453940891839.md, tweet-2091265597237608664.md, tweet-2087873421094896122.md, tweet-2086241047575961750.md, tweet-2085905362260312379.md, tweet-2085633290095202422.md, tweet-2084981497220456650.md, tweet-2049145798768668746.md, tweet-2048446552591740936.md, tweet-2048684838979342618.md, tweet-2047557417718988964.md, tweet-2046624729403142320.md, tweet-2001356829939634313.md, tweet-2113506956933476634.md, tweet-2028878637014057196.md, tweet-2029146101715259900.md, tweet-2021689840253968598.md, tweet-2019727896500400457.md, tweet-2019546289369936090.md, tweet-2003097964865102224.md]
created: 2026-09-29
updated: 2026-10-24
---

# Design Skills for Coding Agents

## Ansatz

Der gespeicherte Artikel sammelt 45 Skills für agentengestützte Gestaltung und gruppiert sie nach Frontend, Bild/3D/Video und weiteren Produktdesign-Schichten. SKILL.md-Dateien sollen Stilregeln und Arbeitsabläufe vor der Codeerzeugung verfügbar machen. [tweet-2068064010600108267](../sources/tweet-2068064010600108267.md)

## Empfohlene Kombination und Grenze

Der Autor empfiehlt wenige sich ergänzende Skills, ein konsistentes Themensystem und Playwright als visuelle Rückkopplung. Die behauptete Qualitätsverbesserung und Installationszahlen sind nicht unabhängig gemessen; die vielen Listenpunkte ersetzen keine Produktentscheidung über Ziele und Nutzer. [tweet-2068064010600108267](../sources/tweet-2068064010600108267.md)

## Animationen und Referenzdesign (Stand 2026-07)

Emil Kowalski kündigt /improve-animations an: ein starkes Modell soll Animationen auditieren, günstigere Modelle sollen die Änderungen ausführen. Das gespeicherte Demo-Video hat trotz erneuter Anreicherung null Transkriptzeichen; konkrete Prüfschritte sind hier nicht belegt. [tweet-2075929554594500772](../sources/tweet-2075929554594500772.md)

Ein anderes Tutorial zeigt einen konkreten Website-Ablauf: Referenzbilder auswählen, Bild und Bewegung getrennt gestalten, Schrift und Farben vorgeben, mit [Codex](../entities/Codex.md) zunächst eine Hero-Sektion erzeugen und das Ergebnis im Browser iterativ anpassen. Die Qualitätsurteile und Geräteprüfung stammen vom Sprecher; ein unabhängiger Vergleich fehlt. [tweet-2075545587093807111](../sources/tweet-2075545587093807111.md)

## Taste Skill aus erster Hand (Stand 2026-03)

Die README von [Taste Skill](../entities/Taste%20Skill.md) liegt vollständig im Raw-Beleg: Der Haupt-Skill design-taste-frontend ist als experimentelle v2 umgeschrieben, steuert Layoutvarianz, Motion und Dichte über drei Regler und ergänzt Stilvarianten, ein Redesign-Audit sowie Bildgenerierungs-Skills für Referenzboards. Die Sammlung ist MIT-lizenziert; Wirkung auf die Designqualität ist nicht gemessen. [tweet-2030433563770855683](../sources/tweet-2030433563770855683.md)

## Referenzen vor dem Prompt (Stand 2026-08)

Leon Lin führt generisch wirkende vibecodete Websites nicht auf schwache Modelle zurück, sondern auf schlechte Referenzen: Vor „make something modern“ solle man Inspiration sammeln, Screenshots, Flows und Komponenten als visuelles Material an den Agenten geben und ein Komponentensystem wählen, statt alles neu generieren zu lassen. Sein Artikel ist eine Ressourcenbibliothek mit 160 Links in neun Rubriken – UI-Inspiration (etwa Godly, Refero, Mobbin), React-Komponenten (React Bits, Magic UI, 21st.dev, shadcn/ui), Shader/WebGL, Verläufe und Hintergründe, Texturen/3D, Bilder und Illustrationen, Icons, Schriften und React Native. Für React Native nennt er Expo, React Native Reusables, gluestack und Reanimated als Struktur, ergänzt um eigene Motion- und Detailarbeit. Die vollständige Liste steht im Raw-Beleg der Quelle; der Mobbin-Link ist ein Affiliate-Link, und die Auswahl ist eine persönliche Sammlung ohne Vergleich. [tweet-2083898950755471520](../sources/tweet-2083898950755471520.md)

## Designkontext extrahieren (Stand 2026-09)

[Dembrandt](../entities/Dembrandt.md) rendert Websites und extrahiert berechnete Stile als DTCG-Tokens, DESIGN.md und Tailwind-Theme; dokumentierte Baseline-Vergleiche prüfen Design-Drift in CI. Canvas/WebGL und dynamische Inhalte begrenzen die Abdeckung. [tweet-2097134648270766520](../sources/tweet-2097134648270766520.md)

[SkillUI](../entities/SkillUI.md) ergänzt einen anderen Ablauf: URL, lokale Dateien oder Repository scannen und Design-Tokens, Kontextdateien und Referenzen als Skill-Paket ausgeben. Ultra-Modus dokumentiert Screenshots und Interaktionsanalyse; die behauptete exakte UI-Reproduktion und automatische Einbindung sind ungeprüft. [tweet-2098224649762984168](../sources/tweet-2098224649762984168.md)

## Unterschiedliche UI-Ressourcen (Stand 2026-08; Online-Nachtrag 2026-10)

[SceneAI](../entities/SceneAI.md) sammelt im gespeicherten Seitenstand Prompts für Hero-Sektionen und Landingpages sowie animierte Hintergründe. Die Extraktion enthält Katalognamen und Zugangswerbung, keine vollständigen Einzelprompts oder gemessene Zeitersparnis. [tweet-2093580756564189238](../sources/tweet-2093580756564189238.md)

[21st.dev](../entities/21st.dev.md) ergänzt den bereits enthaltenen Ressourcenlink um einen konkreten Übernahmeweg: Komponenten als KI-Prompt kopieren oder per shadcn CLI übernehmen; der Code landet im eigenen Projekt statt als einheitliches Komponentenpaket importiert zu werden. Die gespeicherten Kopierlimits bleiben historische Anbieterangaben. [tweet-2093397349309509899](../sources/tweet-2093397349309509899.md)

[VibeUI](../entities/VibeUI.md) ist eine andere Sammlung: Die am 2026-10-09 zusätzlich geprüfte Website bietet Layout-Prompts nach UI-Baustein. Raw selbst enthält lediglich die ausgeschriebene Domain; der Online-Nachtrag darf nicht als ursprünglicher Artikeltext gelten. [tweet-2093377750707142698](../sources/tweet-2093377750707142698.md)

## Visuelle Promptressource (Stand 2026-08; Online-Nachtrag 2026-10)

[MeiGen](../entities/MeiGen.md) ergänzt UI-Referenzen um Bild-/Video-Prompts. Die gespeicherte Extraktion ist knapp; die zusätzlich am 2026-10-09 geprüfte Galerie nennt Bild-zu-Prompt und wiederverwendbare Charaktere, ihre MCP-Seite weitere visuelle Werkzeuge. Diese aktuelle Ergänzung belegt weder historische Funktionsverfügbarkeit noch eine geprüfte Integration oder Ergebnisqualität. [tweet-2093304387430944807](../sources/tweet-2093304387430944807.md)

## Durchsuchbare Regeln und persistentes Designsystem (Stand 2026-08)

[UI UX Pro Max](../entities/UI%20UX%20Pro%20Max.md) ergänzt Extraktions- und Referenztools um BM25-Designsuche, Produkt-/Stackregeln und eine Designsystem-Ausgabe; MASTER.md und pages-Overrides speichern wiederverwendbare Vorgaben. Verschiedene Katalogstände sind datiert und als Herstellerangaben getrennt; die Designqualität wurde nicht verglichen. [tweet-2092994294282060147](../sources/tweet-2092994294282060147.md)

## Zusammenhängende Markenbild-Kampagnen (Stand 2026-08)

[Brand Campaign Prompts](Brand%20Campaign%20Prompts.md) enthält Leon Lins vollständigen Editorial-/3D-Basisauftrag, der gemeinsame Wortmarke, Typografie und Materialien mit bewusst unterschiedlichen Kompositionen verbindet. [tweet-2092979873476215219](../sources/tweet-2092979873476215219.md)

Eine separate Marken-/Themenzeile legt Name, Produkttyp, Bildanzahl und Palette fest; vier gespeicherte ARCO-/PRYNE-Motive dienen als visuelle Beispiele, ohne Modell oder reproduzierbaren Generierungsablauf zu belegen. [tweet-2092979876718379436](../sources/tweet-2092979876718379436.md) [tweet-2092979866836648104](../sources/tweet-2092979866836648104.md)

## Rollenordnung und Bildvorlagen (Stand 2026-08)

[AI Agency Tool Stack](AI%20Agency%20Tool%20Stack.md) ordnet Designwerkzeuge neben Engineering, QA, Dokumenten, Marketing und weiteren Rollen ein; es enthält zusätzliche Repositories und Originaldokumentation, aber kein getestetes Komplettsystem. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)

[GPT Image Prompt Library](../entities/GPT%20Image%20Prompt%20Library.md) ergänzt konkrete Kampagnenprompts um eine strukturierte Galerie, Vorlagenrubriken und einen Style-Library-Skill; vollständige Vorlagen sind teilweise nur verlinkt, Generierungen nicht unabhängig reproduziert. [tweet-2091703453940891839](../sources/tweet-2091703453940891839.md)

## Besucherreise und Scroll-Feedback (Stand 2026-08)

[Scrollcraft](../entities/Scrollcraft.md) ergänzt Stil-/Referenzwerkzeuge um ein Interview über Besucherreise, emotionale Richtung, Belege und Assets, danach Scroll-Szenen und Screenshot-/Keyframe-Prüfung. Das ausführliche Beispiel bewahrt konkrete menschliche Korrekturen und einen verbleibenden Reload-Bug; der Skill-Download und der Asset-Provider-Name fehlen im gespeicherten Artikel. [tweet-2091265597237608664](../sources/tweet-2091265597237608664.md)

## Diagramme und Ressourcenverzeichnis (Stand 2026-08)

[Diagram Design](../entities/Diagram%20Design.md) ergänzt die vorhandenen Gestaltungswerkzeuge um HTML/SVG-Diagramme, Brandprofile und Import/Export. Seine gespeicherte README enthält spätere 2.x-Erweiterungen; diese sind kein Beleg für den Funktionsstand des August-Tweets. [tweet-2087873421094896122](../sources/tweet-2087873421094896122.md)

[Design Engineer Tools](../entities/Design%20Engineer%20Tools.md) ist ein separates kategorisiertes Verzeichnis für Webdesign, Komponenten, Capture und Utilities. Das Originalbild zeigt konkrete Namen, während die gespeicherte Website-Extraktion nur Rubriken enthält; die Sammlung ist keine vergleichende Werkzeugbewertung. [tweet-2086241047575961750](../sources/tweet-2086241047575961750.md)

## Interaktive Ressourcen und Landingpage-Briefing (Stand 2026-08)

[Oil Motion](../entities/Oil%20Motion.md) ergänzt die Gestaltungswerkzeuge um einen Keyframe-/Videopfad für interaktive Webanimationen: bestätigte Zustände, Framebereinigung, Ressourcenbudget und Eingabezuordnung. Die gespeicherte README beschreibt zusätzliche Qualitäts- und Fallback-Prüfungen, ohne gemessene Browserqualität zu belegen. [tweet-2085905362260312379](../sources/tweet-2085905362260312379.md)

[Elaya Design Skills](../entities/Elaya%20Design%20Skills.md) dokumentiert einen separaten Landingpage-Skill mit Intake, Conversion-Texten und visuellen Vorgaben. Das Repository elayadesign/ai-design-skills ist vom bisher im Katalog genannten Owl-Listener/ai-design-skills zu unterscheiden; der aktuelle primäre Skill-Nachtrag steht datiert auf der Entity-Seite. [tweet-2085633290095202422](../sources/tweet-2085633290095202422.md)

## Animation erstellen und prüfen (Stand 2026-08)

[Emil Kowalski Skills](../entities/Emil%20Kowalski%20Skills.md) ergänzt den früheren /improve-animations-Post um /find-animation-opportunities → /animate → /review-animations und ein Repository mit direkt verlinkten Skill-Dateien. Die gespeicherte README nennt konkrete Easing-/UI-Regeln, aber keinen unabhängigen Qualitätsvergleich. [tweet-2084981497220456650](../sources/tweet-2084981497220456650.md)

## Designoberfläche und Website-Nachbau (Stand 2026-04; Repo-Nachtrag 2026-10)

[OpenDesign](../entities/OpenDesign.md) ergänzt einzelne Skills um eine gemeinsame Oberfläche für Briefing, Designsysteme, Projektdateien und Übergabe; der gespeicherte spätere README-Umfang bleibt von der April-Ankündigung getrennt. [tweet-2049145798768668746](../sources/tweet-2049145798768668746.md)

[AI Website Cloner Template](../entities/AI%20Website%20Cloner%20Template.md) ergänzt die Designextraktion um einen Nachbau- und Vergleichsablauf. Das zugeordnete Originalrepository ist ein ausdrücklicher Nutzer-Nachtrag; der zusätzlich gelesene aktuelle Skill ist als späterer Stand dokumentiert. [tweet-2048446552591740936](../sources/tweet-2048446552591740936.md)

## Komponentenreferenz (Stand 2026-04; Nutzer-Nachtrag 2026-10)

Sean Brydon beschreibt 158 UI-Komponenten in einer Sandbox, für coss ui angepasst und über die shadcn CLI hinzufügbar. Dies ist eine konkrete Komponentenressource neben den vorhandenen Design-Skills; kostenlose Nutzung und Umfang sind Angaben des April-Posts. [tweet-2048684838979342618](../sources/tweet-2048684838979342618.md)

Der Nutzer ordnete am 16.10.2026 ausdrücklich [shadcn/ui](https://ui.shadcn.com/) als Referenzseite zu. Die an diesem Tag gelesene Homepage beschreibt anpassbare Komponenten als Basis eigener Designsysteme. Die Zuordnung ist ein datierter Nutzer-Nachtrag, kein Beleg, dass die Homepage selbst die historische 158er-Sandbox ist. Das gespeicherte Video hat keinen Transkriptinhalt und ließ sich visuell nicht abrufen. [tweet-2048684838979342618](../sources/tweet-2048684838979342618.md)

## Designsystem plus Referenz und Remix (Stand 2026-04)

Das vollständige Tutorial zu [Newform](../entities/Newform.md) verbindet DESIGN.md mit Screenshots beziehungsweise HTML: Das Designsystem gibt die gemeinsamen Regeln, die konkrete Referenz steuert die gewünschte Darstellung. Iterate soll die Vorlage stärker erhalten, Remix neue Varianten erkunden; Stil-Skills und kurze Änderungsaufträge ergänzen diesen Ablauf. [tweet-2047557417718988964](../sources/tweet-2047557417718988964.md)

Die gleiche Grundlage dient anschließend für weitere Landingpage-Sektionen, mobile Ansichten, Slides und Motion-Varianten. HTML plus DESIGN.md werden an Aura oder [Claude Design](../entities/Claude%20Design.md) übergeben; der Sprecher zeigt ausdrücklich schwankende Resultate und weitere Iterationen. Historische Tarife und Promptkontingente sind keine heutigen Nutzungszusagen. [tweet-2047557417718988964](../sources/tweet-2047557417718988964.md)

## Formale Designregeln und Rückkopplung (Stand 2026-04)

[Design Markdown](../entities/Design%20Markdown.md) ergänzt die Arbeitsabläufe um einen dokumentierten DESIGN.md-Entwurf: Designbegründungen und genaue Tokens stehen zusammen; Komponenten verweisen auf benannte Farbrollen. Der offizielle Stitch-Vortrag zeigt die Schleife Datei lesen, Komponente ändern, per CLI prüfen und einen gemeldeten Kontrastfehler korrigieren. Das ist eine konkrete Validierungsdemo, kein Beleg für automatisch barrierefreie Gesamtoberflächen. [tweet-2046624729403142320](../sources/tweet-2046624729403142320.md)

## Dunkle Hintergrundfarben statt reinem Schwarz (Stand 2025-12)

Ruben Hume empfiehlt, den Hintergrund nicht auf reines Schwarz #000000 zu setzen, und nennt sechs dunkle Ersatzwerte als HEX-Palette: #0B1215, #0F171F, #0B0B0B, #020C1A, #011122 und #161616. Die Werte lassen sich als Farbtoken in ein Designsystem oder eine DESIGN.md übernehmen; der Post begründet die Empfehlung nicht und prüft keinen Kontrast. [tweet-2001356829939634313](../sources/tweet-2001356829939634313.md)

## Anti-Slop-Skill mit Reviewer (Stand 2026-10)

[Hallmark](../entities/Hallmark.md) von Together AI prüft gebaute Seiten in einem echten Browser gegen typische KI-Merkmale und lässt einen Reviewer-Agenten mit frischem Kontext entscheiden. Das ist eine Ergänzung zu Skills, die nur Stilregeln vorgeben: Die Rückkopplung ist Teil des Skills. Wirksamkeit ist Herstellerangabe. [tweet-2113506956933476634](../sources/tweet-2113506956933476634.md)

## Vokabular und Prompt-Vorlage (Stand 2026-03)

Ein Ansatz neben Skills ist das gezielte Vokabular: [Component Gallery](../entities/Component%20Gallery.md) listet UI-Komponenten mit Namen und Beispielen aus Design-Systemen, damit Entwickler Komponenten präzise benennen können; der Autor empfahl, Begriffe zu lernen, Screenshots zu sichern und umsetzen zu lassen (Autorangabe). [tweet-2028878637014057196](../sources/tweet-2028878637014057196.md)

Eine vollständige Prompt-Vorlage statt eines Skills ist der [Dark Portfolio Landing Page Prompt](Dark%20Portfolio%20Landing%20Page%20Prompt.md): Er schreibt Design-System, Abschnitte, Animationen und Abhängigkeiten einer Portfolio-Seite im Detail vor. [tweet-2029146101715259900](../sources/tweet-2029146101715259900.md)

## Komponenten und konkrete Hero-Prompts (Stand 2026-02; Nutzer-Nachtrag 2026-10-24)

[WC3UI](../entities/WC3UI.md) ergänzt die Ressourcen um Warcraft-III-Komponenten mit vier Fraktionsthemen, Formularen, Command Card und 3D-Porträts. Originalpost und Showcase widersprechen sich bei der Asset-Herkunft; die Entity hält diese Grenze fest. [tweet-2021689840253968598](../sources/tweet-2021689840253968598.md)

Der [Video Hero Section Prompt](Video%20Hero%20Section%20Prompt.md) enthält den am 2026-10-24 vom Nutzer ergänzten [DesignRocket-Link](https://designrocket.io/) und konkrete React-/Tailwind-Vorgaben für Vollbildvideo, dreizeilige Headline und SVG-CTA. Der komplette Nutzer-Prompt steht in der Source; die Video-URL enthält ein ungeprüftes Leerzeichen, der individuelle SVG-Pfad fehlt. [tweet-2019727896500400457](../sources/tweet-2019727896500400457.md)

### Porträt-Reveal als vollständiger Prompt (Stand 2026-02)

Daniel Ch beschreibt einen einzelnen Vollbild-Hero auf weißer Basis: Porträt eins als zentriertes Cover-Bild; Name links oben, Vor- und Nachname getrennt in einer Serifenschrift wie Playfair Display; F1 Records rechts oben; verlinkte, gefüllte Instagram-/X-SVG-Icons rechts unten. [tweet-2019546289369936090](../sources/tweet-2019546289369936090.md)

Ein kreisförmiger Spotlight-Cursor folgt mit leichter Verzögerung und legt Porträt zwei unter dem ersten frei. Schnelle Bewegung erzeugt weich verblassende Echos; ein subtil animiertes Grid und gegenläufige Parallax ergänzen die Tiefe. Name, Navigation und Icons sollen beim Überfahren weiß werden; etwa 300-ms-Übergänge sind vorgegeben. Die beiden Porträts müssen als Eingaben geliefert werden. [tweet-2019546289369936090](../sources/tweet-2019546289369936090.md)

Die vollständige Vorlage steht in der Source. Der Autor nennt einen Versuch mit Shipper auf Opus 4.6; dies belegt weder messbare Designqualität noch einen funktionsfähigen mobilen Ersatz für die Mausinteraktion. [tweet-2019546289369936090](../sources/tweet-2019546289369936090.md)

## Landing-Page-Skill mit Ästhetikrichtungen (Stand 2025-12)

CloudAI-X teilt ein SKILL.md namens creating-landing-pages, das Landingpages als einzelne HTML-Datei erzeugt. Vor dem Coding fragt der Skill Produkt, Zielgruppe sowie primären und sekundären CTA ab. [tweet-2003097964865102224](../sources/tweet-2003097964865102224.md) Er verlangt eine von sieben Richtungen (Ink & Paper, Neon Terminal, Brutalist Mono, Soft Luxury, Retro-Future, Swiss Precision, Organic Flow), je mit Einsatzbereich, sowie sieben Pflichtabschnitte vom Hero bis zum Footer. [tweet-2003097964865102224](../sources/tweet-2003097964865102224.md) Eine Verbotsliste schließt typische KI-Muster aus: Violett-Blau-Verläufe, Inter/Roboto/Arial, #6366F1, einheitlich 16px Radius, Schatten auf allen Karten, Lorem ipsum. [tweet-2003097964865102224](../sources/tweet-2003097964865102224.md) Eine Design-Token-Vorlage und eine Checkliste (Richtung, Schriftpaar, höchstens fünf Farben, Hero-Idee, ein interaktives Element) vervollständigen ihn. [tweet-2003097964865102224](../sources/tweet-2003097964865102224.md) Der Post belegt keine Wirkung; der Wortlaut steht in der Quelle.
