---
tags: [agents, product-building, tools]
sources: [tweet-2064826394589442448.md, tweet-2063935703189262622.md, tweet-2055166454404661614.md, tweet-2082060635936805111.md, tweet-2103801891528573089.md, tweet-2103929525746938284.md, tweet-2098941338297458746.md, tweet-2097949495749390762.md, tweet-2093762643639115999.md, tweet-2093640804359180592.md, tweet-2093344589788643702.md, tweet-2106891315371737480.md, tweet-2085905362260312379.md, tweet-2112180280110776797.md, tweet-2112166940081004693.md, tweet-2111306174259691669.md, tweet-2110389810258968965.md]
created: 2026-09-29
updated: 2026-10-23
---

# Agentic Video Production

## Ablauf im Beispiel

[Agentic Video Production](Agentic%20Video%20Production.md) meint hier den berichteten Einsatz eines Coding-Agenten für einen reproduzierbaren Schnittablauf: 17 Takes werden transkribiert, Szenen und Zeitmarken in einer Edit-JSON festgehalten, über FFmpeg zusammengesetzt und farblich bearbeitet. [tweet-2064826394589442448](../sources/tweet-2064826394589442448.md)

Remotion-Komponenten legen UI-Einblendungen entlang des Transkripts fest; eine Designgruppe bearbeitet Figma-Entwürfe, die der Agent laut Autor wieder in den Film übernimmt. Die beschriebenen Schritte beziehen sich auf ein [Fable](../entities/Fable.md)-Beispiel. [tweet-2064826394589442448](../sources/tweet-2064826394589442448.md)

## Voraussetzung und Grenze

Der Autor hatte ein Filmteam, 25 GB Rohmaterial und menschliche Designer; er sagt zudem, dass das gezeigte spätere Beispiel nicht genau der veröffentlichte Launchfilm sei. Die Quelle belegt seinen Workflow-Bericht, nicht autonome Filmqualität oder eine generelle Zeitersparnis. [tweet-2064826394589442448](../sources/tweet-2064826394589442448.md)

## Wiederverwendbares Toolkit (Stand 2026-06)

Die README von [Claude Code Video Toolkit](../entities/Claude%20Code%20Video%20Toolkit.md) beschreibt einen wiederverwendbaren Ablauf von Skript und Assets über Szenenreview, Design, Audio und Vorschau zum MP4-Render und optionaler Veröffentlichung. Menschen bleiben laut Autor Regisseur, Editor und Designer; der Agent bedient die Werkzeuge. [tweet-2063935703189262622](../sources/tweet-2063935703189262622.md)

Ein project.json hält Szenen, Audio, Sitzungsverlauf und Phase fest; der Dateibestand wird laut Dokumentation mit dem geplanten Zustand abgeglichen. Markenprofile, Templates und gespeicherter Projektkontext sollen Wiederaufnahme über mehrere Sitzungen ermöglichen. Das erweitert den Einzelfall um ein dokumentiertes Werkzeugangebot, belegt aber keine generelle autonome Qualität oder Kostenersparnis. [tweet-2063935703189262622](../sources/tweet-2063935703189262622.md)

## Benachbartes Schnittwerkzeug (Stand 2026-05)

[OpenCut](../entities/OpenCut.md) wird in einem Post als offener Mehrspur-Videoeditor ohne Wasserzeichen beworben. Das Videotranskript fehlt; der auf OpenCut dokumentierte Nutzer-Nachtrag ergänzt eine README (Stand 2026-10-08) mit weiterhin nur angekündigtem MCP/Headless-Modus, aber keine geprüfte Integration in diesen Produktionsablauf. Der Werkzeughinweis wird deshalb von nachgewiesenen Agenten-Workflows getrennt. [tweet-2055166454404661614](../sources/tweet-2055166454404661614.md)

## Vollautomatische Kurzvideos (Stand 2026-07)

[MoneyPrinterTurbo](../entities/MoneyPrinterTurbo.md) steht für das Gegenstück zum menschlich geführten Schnitt: Aus Thema oder Stichwort entstehen laut README Skript, Material, Sprachausgabe, Untertitel, Musik und Kurzvideo in einem Durchlauf, optional mit automatischer Veröffentlichung. Die README nennt dafür auch einen Agent-Skill. Über Qualität, Reichweite oder Einnahmen sagt sie nichts aus. [tweet-2082060635936805111](../sources/tweet-2082060635936805111.md)

## Prozess-Skills für Launchfilme (Stand 2026-09)

Zwei Skills verlagern Produktfilme in einen freigabegesteuerten Agentenprozess: [Product Film Skill](../entities/Product%20Film%20Skill.md) baut aus Designsystem, Interview, BRAND.md und Beat-Grid eine Remotion-Komposition mit geprüftem 240-fps-Render. [tweet-2103801891528573089](../sources/tweet-2103801891528573089.md) [No Slop Motion](../entities/No%20Slop%20Motion.md) setzt auf HyperFrames und zehn Gates von Pain Research bis QA, mit Bannliste und Linter gegen typische KI-Videomuster. [tweet-2103929525746938284](../sources/tweet-2103929525746938284.md)

## HTML-Rendering als weiterer Werkzeugpfad (Stand 2026-09)

[HyperFrames](../entities/HyperFrames.md) dokumentiert HTML-/CSS-Kompositionen, seekbare Animationen und Frame-Erfassung in Chrome mit FFmpeg-Ausgabe. Das ist ein weiterer Rendering-Pfad neben dem bereits gespeicherten Produktionsprozess; eine fertige, qualitativ geprüfte Videoausgabe folgt aus der README allein nicht. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## MCP-Schnitt mit menschlicher Regie (Stand 2026-09)

Ein Editor beschreibt [DaVinci Resolve](../entities/DaVinci%20Resolve.md) mit Astra über MCP: Material synchronisieren, Rohschnitt erstellen, Dialog-Cleanup und anschließend live durchsehen und Korrekturen diktieren. Zwei-Frame-Audio-Crossfades sowie Punch-ins sind konkrete wiederkehrende Arbeitsschritte. [tweet-2097949495749390762](../sources/tweet-2097949495749390762.md)

Der Autor berichtet weniger Handarbeit, aber ähnliche gesamte Schnitt-/Regiezeit. Zu knapp abgeschnittene Wörter, zu viel Leerraum und gelegentliche Antworten ohne Ausführung erfordern Nachprüfung; fehlende MCP-Funktionen werden teilweise über Computersteuerung bedient. Der Bericht erweitert die vorhandenen Rendering-Workflows um direkte Timeline-Arbeit, belegt aber keine vollständig autonome Ausgabe. [tweet-2097949495749390762](../sources/tweet-2097949495749390762.md)

## Videostreams während der Aufnahme bearbeiten (Stand 2026-08)

[JoyAI-Video-Edit](../entities/JoyAI-Video-Edit.md) ergänzt die dokumentierten Schnitt- und Renderabläufe um einen anderen Pfad: Bilder eines Live- oder hochgeladenen Videostreams werden laut README bei ihrem Eintreffen anhand von Textanweisungen bearbeitet, ohne die ganze Sequenz abzuwarten. Das Originaldiagramm zeigt wechselnde Szenen-, Subjekt- und Stilvorgaben während desselben Streams. Das ist ein Modell-/Deployment-Beleg, kein Nachweis eines vollständigen autonomen Produktionsprozesses. [tweet-2093762643639115999](../sources/tweet-2093762643639115999.md)

## Austauschbare Kurzvideo-Bausteine (Stand 2026-08; README nachgeladen 2026-10-09)

[Pixelle-Video](../entities/Pixelle-Video.md) dokumentiert eine themengesteuerte Kurzvideo-Pipeline aus Skript, generierten Bildern oder Clips, TTS und Musik. Der wiederverwendbare Mechanismus sind austauschbare ComfyUI-/RunningHub-Workflows und direkte Medien-APIs sowie getrennte HTML-Templates für Text, Bild und Video; vor der Gesamtausgabe lassen sich Stimme, Bildstil und Template einzeln vorprüfen. Das am 09.10.2026 nachgeladene README ist ein späterer Dokumentationsstand zum August-Post. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)

Die Quelle nennt [MoneyPrinterTurbo](../entities/MoneyPrinterTurbo.md) als Inspiration, beschreibt aber ein eigenständiges Repository und einen anderen Konfigurations-/Workflow-Pfad. Sie belegt eine dokumentierte Automatisierungskette, keine gemessene Zeitersparnis, autonome Qualität oder profitable Veröffentlichung. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)

## Code und Timeline synchronisieren (Stand 2026-08)

[Diffusion Studio](../entities/Diffusion%20Studio.md) dokumentiert ein bidirektionales JSX-Dokument: Agenten ändern Code, Menschen bearbeiten die resultierenden Editor-Knoten, und UI-Änderungen landen wieder im Code. Die dapi-CLI ergänzt Medienprüfung, Szenenchecks und Renderausgabe; das ist ein eigener Werkzeugpfad, keine geprüfte autonome Filmproduktion. [tweet-2093344589788643702](../sources/tweet-2093344589788643702.md)

## Regie, Technikbibliothek und gemessene QA (Stand 2026-10)

[Cinetic](../entities/Cinetic.md) verbindet drei Konzeptvarianten und einen gewählten Storymechanismus mit seedbarer Technikauswahl, gemeinsamer Bild-/Ton-Timeline und ausführbaren Render-/Synchronitätsprüfungen. Die vollständige README und vier Briefs dokumentieren einen eigenen Produktionspfad neben [Product Film Skill](../entities/Product%20Film%20Skill.md) und [No Slop Motion](../entities/No%20Slop%20Motion.md). [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)

Die interne Evaluation berichtet höher erfüllte technische Anforderungen, aber geteilte neutrale Qualitätsurteile und etwa dreifachen Zeit-/Tokenaufwand gegenüber der Baseline. Der zusätzliche QA-Prozess ist damit kein Nachweis einer generell besseren oder günstigeren Videoausgabe. [tweet-2106891315371737480](../sources/tweet-2106891315371737480.md)

## Vorbereitete Videos als interaktive Webressourcen (Stand 2026-08)

[Oil Motion](../entities/Oil%20Motion.md) bereitet generierte Bewegungen nach Keyframe-Prüfung als komprimierte MP4- oder Alpha-WebP-Ressourcen auf und steuert deren Fortschritt durch Scrollen, Maus oder Touch. Die gespeicherte README trennt Bewegungsdesign von programmatischer Translation/Skalierung und verlangt Pilot, Kontinuitätsprüfung sowie statische Fallbacks. Das ergänzt Film-/Schnittabläufe um einen Webanimationspfad, ohne autonome Qualität zu belegen. [tweet-2085905362260312379](../sources/tweet-2085905362260312379.md)

## Bewegung über sechs Regler steuern (Stand 2026-10)

beamnxw lässt [Claude Code](../entities/Claude%20Code.md) eine Bewegungsreferenz in sechs bearbeitbare Regler zerlegen und legt die Werte in eine Config: Spacing (Abstand zwischen den Posen), Typografie (Skalierung, Laufweite, Zeilenumbrüche), Motion Blur (Belichtung bei schneller Bewegung), Easing (Beschleunigen und Abbremsen), Follow-through (Ausschwingen nach dem Stopp) und Anticipation (kleiner Rückzug vor der Hauptbewegung). [tweet-2112180280110776797](../sources/tweet-2112180280110776797.md)

Dadurch wird Feedback konkret, etwa vier Frames Anticipation hinzufügen, den Schwanz um drei Frames verzögern oder den Titel eine Sekunde halten. Die Schleife lautet bauen, rendern, scrubben, justieren, wiederholen. [tweet-2112180280110776797](../sources/tweet-2112180280110776797.md)

Die offizielle Remotion-GSAP-Integration (useGsapTimeline aus @remotion/gsap, Remotion v4.0.517) baut eine pausierte GSAP-Timeline und setzt sie auf den aktuellen Frame der Remotion-Timeline; so bleibt die Animation auf Remotions Frame-Uhr. [tweet-2112180280110776797](../sources/tweet-2112180280110776797.md)

Evidenzgrenze: Der Post nennt weder gemessene Ergebnisse noch ein Beispielprojekt. Das Modell "Opus 5.5" und die Einnahmeaussagen des zitierten Artikels (Verkauf von Launchvideos, KI-Mitarbeiter Viktor) sind Angaben des Autors beziehungsweise Werbung. [tweet-2112180280110776797](../sources/tweet-2112180280110776797.md)

## Videostudio als Produktionsvertrag mit Review-Gates (Stand 2026-10)

Der von 0xwhrrari zitierte Artikel trennt Regie, Referenz, Timeline, Renderer und Kritiker. Opus schreibt eine Frame-Funktion (Zustand des Films zum Zeitpunkt t), ein Renderer erzeugt die Frames; Änderungen bleiben lokal (ein Zeitwert, eine Kurve, ein Asset), statt ein Videomodell neu zu starten. Fotorealistische Szenen und organische Bewegung nennt der Artikel ausdrücklich als Grenze. [tweet-2112166940081004693](../sources/tweet-2112166940081004693.md)

Vorgaben vor dem Rendern: ein kleines Produktionsdokument (ein Merksatz, Zielgruppe, Dauer, Formate, echte Logos und UI-Screenshots, Marken-Tokens, visuelle Regeln, nie erfundene Produktscreens oder Kennzahlen), eine Referenzanalyse mit konkreten Werten statt "premium" und ein Shot-List mit Eintritts- und Austrittszustand je Beat. Jeder Frame muss deterministisch und direkt renderbar sein (kein versteckter Takt, kein unseeded Zufall). Audio liegt auf derselben Beat-Timeline. [tweet-2112166940081004693](../sources/tweet-2112166940081004693.md)

Qualität wird über Contact Sheets (ein Standbild je Beat) und eine Checkliste geprüft (Lesbarkeit am Telefon, Safe Area, echte Assets, Schnitt-/Tonsynchronität, Hook in den ersten zwei Sekunden); die drei größten Mängel werden mit Zeitstempel lokal repariert. Sechs Gates (Referenzen, Stil und Shot-List, Stills, Rohschnitt, Reparatur, Audio und Formate) begrenzen den langen Agentenlauf; 16:9 und 9:16 sind getrennte Kompositionen. Ablage in einer Ordnerstruktur (brief, style-guide, shotlist, assets, src, reviews, out). [tweet-2112166940081004693](../sources/tweet-2112166940081004693.md)

Der Artikel enthält einen vollständigen Prompt für diesen Vertrag. Der Nutzer ergänzt eine PDF mit Prompts ("Prompt No After Effects Opus 5.5"): [Google Drive](https://drive.google.com/file/d/1-VZJxR-VpR1rY4FyymcMDIq742fkQYLT/view). Der PDF-Inhalt wurde nicht geprüft. Der Titel "Opus 5.5 hat After Effects ersetzt" ist eine Behauptung des Posts; belegt sind im Artikel keine Messwerte. [tweet-2112166940081004693](../sources/tweet-2112166940081004693.md)

## Motion-Director-Prompt mit messbaren Kriterien (Stand 2026-10)

Das gelesene Originalbild liefert eine vollständige Vorlage mit Rolle, Brief, vier Modi (Showreel, Product, Launch-story, Explainer), Assets, Craft, Audio, Build, Workflow, Critic loop und Quality bar. Sie ergänzt den vorhandenen Produktionsvertrag um eigene Regie- und Messvorgaben; die ausführliche Inhaltswiedergabe steht in der Source. [tweet-2111306174259691669](../sources/tweet-2111306174259691669.md)

### Konkrete Entscheidungen vor der Produktion

Der Brief fragt Gegenstand, Publikum, gewünschte Schlussaussage, Dauer/Formate, Framerate, Marke, Fakten, Material, Referenzen, Ton, Autonomie, Toolchain und CTA. Unausgefüllte Felder soll der Agent mit einer begründeten Wahl in brief.md festhalten. Produktfakten werden separat mit Originalsatz und URL in facts.json gespeichert; echte Logos, Farben und Schriften kommen aus dem Produkt. [tweet-2111306174259691669](../sources/tweet-2111306174259691669.md)

Der Prompt verlangt zwei bis drei Konzepte, dann eine Entscheidung, Storyboard und Style-Bible vor dem vollständigen Build. Ein drei- bis fünfsekündiger Testrender prüft den Weg früh. Eine gemeinsame deterministische Timeline hält Bild, Ton und Schnitt zusammen; jeder Zustand stammt aus der Framenummer statt aus laufenden Timern oder ungesetztem Zufall. [tweet-2111306174259691669](../sources/tweet-2111306174259691669.md)

### Review und ausdrücklich vorlagenabhängige Grenzwerte

Frische Kritiker beurteilen die gerenderte Arbeit nach Storyboard, jeder Szene und jedem Vollrender. Builder und Kritiker sind getrennte Rollen; Probleme erhalten Zeitstempel, eine lokale Reparatur und eine erneute Prüfung aller älteren Punkte. Zusätzlich zum Bildreview fordert die Vorlage einen Audio-only-Durchlauf, einen Faktencheck und eine Sync-Liste in timing.json. [tweet-2111306174259691669](../sources/tweet-2111306174259691669.md)

Die Vorlage nennt unter anderem 0,7 Sekunden Mindestlesezeit je Wort (0,3 bei Code/Zahlen), mindestens 4,5:1 Textkontrast, einen Frame Toleranz für Cuts/Hits, -14 LUFS und True Peak unter -1 dBTP. Für Product nennt sie Kompositionswechsel alle 1,4-3,5 Sekunden und für Explainer 125-145 Wörter pro Minute. Diese Werte beschreiben die konkrete Vorlage; sie sind keine allgemeingültigen Produktionsstandards und keine hier gemessenen Resultate. [tweet-2111306174259691669](../sources/tweet-2111306174259691669.md)

Erfundene Kennzahlen, Testimonials und reale Personen sind untersagt, generiertes Material ist zu kennzeichnen; geliefert werden MP4 und editierbare Projektquelle. Der beworbene 400-Dollar-pro-Stunde-Vergleich und die Modellbezeichnung des Posts belegen weder Kostenersparnis noch Filmqualität. [tweet-2111306174259691669](../sources/tweet-2111306174259691669.md)

## Clawd-Animation als Prompt-Vorlage (Stand 2026-10)

Leon Lin zeigt eine 60-Sekunden-Animation des Claude-Maskottchens Clawd, nach eigenen Angaben mit [Claude Opus 5.5](../entities/Claude%20Opus%205.5.md) Ultracode erstellt; das Video hat kein Transkript, der Post keinen Prompt. [tweet-2110389810258968965](../sources/tweet-2110389810258968965.md)

Den vom Nutzer ergänzten Prompt kennzeichnen diese Vorgaben: ein Ein-Minuten-Video, Assets wie SVGs online suchen und selbst nachbauen und animieren, 3D-Objekte rendern (etwa Claude-Code-Terminals oder Natur), kein Text und keine Schrift, ein echtes Video statt reiner Motion Graphics, eigene Ideen statt Kopien, und für den Ton nur freie, professionelle Sounds aus dem Netz, keine im Code erzeugten. Die Anti-Slop-Vorgabe ist eine Qualitätsanweisung, kein Nachweis der Ergebnisqualität; der vollständige Wortlaut steht in der Source. Die Zuordnung des Prompts zum gezeigten Video beruht auf der Angabe des Nutzers. [tweet-2110389810258968965](../sources/tweet-2110389810258968965.md)
