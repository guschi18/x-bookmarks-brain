---
tags: [tools, agents, marketing]
sources: [tweet-2093640804359180592.md]
created: 2026-10-09
updated: 2026-10-09
---

# Pixelle-Video

## Projekt und Belegzeitraum (Stand 2026-08; README nachgeladen 2026-10-09)

Der Post vom 29.08.2026 bewirbt Pixelle-Video als automatisierte Kurzvideo-Engine: Thema eingeben, Skript, Bilder, Sprachausgabe und Musik zusammenführen. Die Quelle beschreibt eine modulare ComfyUI-Architektur; das gespeicherte, am 09.10.2026 nachgeladene README konkretisiert die Bedienung. Seine späteren Funktionen sind damit nicht rückwirkend als zum Tweetzeitpunkt verfügbar belegt. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)

Der gespeicherte [Repository-Link](https://github.com/ATH-MaaS/Pixelle-Video) lautet ATH-MaaS/Pixelle-Video; README-Befehle, Releases und Issues verwenden [AIDC-AI/Pixelle-Video](https://github.com/AIDC-AI/Pixelle-Video). Der Auszug liefert keinen Umzugszeitpunkt. Die README bezeichnet die Lizenz als Apache 2.0; der verlinkte Lizenztext wurde hier nicht gesondert geprüft. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)

## Einstieg und Konfiguration (Stand 2026-08; README nachgeladen 2026-10-09)

- Windows: laut README das integrierte Release-Paket entpacken und start.bat öffnen; Python, uv und FFmpeg seien enthalten. Quellinstallation: uv und FFmpeg installieren, das AIDC-AI-Repository klonen, dann `uv run streamlit run web/app.py`. Die WebUI läuft laut Anleitung auf http://localhost:8501/. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)
- LLM: API Key, Base URL und Modell für die Skripterstellung konfigurieren. Alternativ kann eine fertige Textvorlage die Skripterstellung überspringen. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)
- Medien: lokale ComfyUI-Instanz oder RunningHub-Schlüssel verwenden; direkte API-Workflows benötigen die Schlüssel ihrer Anbieter. Das README nennt OpenAI/GPT Image, DashScope/Wan/HappyHorse, ARK/Seedream/Seedance und Kling. Diese Anbieter-/Modellpfade sind Dokumentationsangaben vom Nachladezeitpunkt. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)

## Ablauf und Anpassung (Stand 2026-08; README nachgeladen 2026-10-09)

Die WebUI trennt Inhalt, Stimme/Visuals und Ausgabe. TTS-Workflows werden aus workflows/ geladen; genannt sind Edge-TTS und Index-TTS. Unterstützende Workflows können Referenzaudio zum Klonen aufnehmen. Vor der Erzeugung lassen sich Stimme und Bildstil vorhören beziehungsweise ansehen. Hintergrundmusik kommt aus mitgelieferten oder eigenen Dateien im bgm/-Ordner. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)

HTML-Templates trennen static_ für Textlayout, image_ für Bildhintergründe und video_ für Videohintergründe. Eigene ComfyUI-Workflows gehören nach workflows/, eigene Templates nach templates/. Die Anleitung nennt auswählbare Bildgrößen, englische Stilpräfixe und direkte Video-API-Parameter abhängig vom Modell. Das fertige Video wird mit Dauer, Dateigröße und Szenenzahl in der WebUI angezeigt und in output/ gespeichert. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)

## Grenzen und Quellenfehler (Stand 2026-08; README nachgeladen 2026-10-09)

Die README nennt lokale Ollama-/ComfyUI-Ausführung als kostenlos; das ist eine Anbieterbehauptung zu API-Kosten, keine Vollkostenrechnung für Hardware, Strom oder Einrichtung. Auch „in wenigen Minuten“ ist keine hier reproduzierte Laufzeitmessung. Der Tweet wirbt zusätzlich mit digitalen Moderatoren und Bewegungstransfer; der gespeicherte Auszug liefert dafür keinen vollständigen eigenen Bedienablauf. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)

Der lokale ComfyUI-Link im Original enthält hinter Port 8188 eine kodierte schließende Klammer und ist ungültig. Die lesbare Adresse ist http://127.0.0.1:8188; der vollständige Fehler bleibt im Quellenbeleg erhalten. Der Nutzer bestätigte am 09.10.2026 die Ausnahme für den Ingest. Installation, API-Erreichbarkeit, Stimmklonen und Videoqualität wurden nicht praktisch geprüft. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)

[Agentic Video Production](../concepts/Agentic%20Video%20Production.md) ordnet die Pipeline als automatisierten Produktionspfad ein. [MoneyPrinterTurbo](MoneyPrinterTurbo.md) wird im README als Inspiration genannt, neben Pixelle-MCP, NarratoAI, MoneyPrinterPlus und ComfyKit; verwandte Projekte sind kein Beleg für eine identische Implementierung. [tweet-2093640804359180592](../sources/tweet-2093640804359180592.md)
