---
tags: [tools, marketing]
sources: [tweet-2082060635936805111.md, tweet-2098941338297458746.md]
created: 2026-10-02
updated: 2026-10-08
---

# MoneyPrinterTurbo

## Funktionen laut README (Stand 2026-07)

- Ablauf: Thema oder Stichwort eingeben; Skript, passende Clips, Sprachausgabe, Untertitel und Hintergrundmusik werden zu einem HD-Video zusammengesetzt. Eigene Skripte und lokale Clips sind möglich. [tweet-2082060635936805111](../sources/tweet-2082060635936805111.md)
- Formate: Hochformat 1080x1920 und Querformat 1920x1080, Stapelerzeugung mehrerer Varianten, einstellbare Clipdauer und mehrsprachige Skripte. [tweet-2082060635936805111](../sources/tweet-2082060635936805111.md)
- Bausteine: zahlreiche LLM-Anbieter und Gateways einschließlich Ollama; TTS unter anderem über kostenloses Edge TTS, Azure, Gemini und ElevenLabs; Untertitel über TTS-Zeitstempel oder lokales faster-whisper; Stockmaterial von Pexels, Pixabay und Coverr oder KI-Clips über WaveSpeed. [tweet-2082060635936805111](../sources/tweet-2082060635936805111.md)
- Zugänge: Agent-Skill, WebUI, API und CLI (cli.py --video-subject); Installation über uv mit Python 3.11 oder höher, Docker, Windows-Paket oder Colab. [tweet-2082060635936805111](../sources/tweet-2082060635936805111.md)
- Veröffentlichung: Mit Upload-Post-Schlüssel in config.toml lädt das Werkzeug fertige Videos automatisch zu TikTok, Instagram und YouTube hoch. [tweet-2082060635936805111](../sources/tweet-2082060635936805111.md)

## Grenzen (Stand 2026-07)

Die README enthält viele Sponsoren- und Affiliate-Links zu API-Anbietern; die mitgelieferte Hintergrundmusik stammt laut README aus YouTube-Videos mit Löschhinweis bei Rechteverletzung, was die Nutzungsrechte offenlässt. Der Lizenztext ist nur verlinkt. [tweet-2082060635936805111](../sources/tweet-2082060635936805111.md)

## Erweiterte CLI und Medienpfade (Stand 2026-09)

Die neu gespeicherte README ergänzt quadratische Videos, mehrere KI-Materialanbieter und ModelBest-VoxCPM-TTS. Dieser API-Pfad verarbeitet gewöhnlichen Text und Standardstimme, keine Referenzaudio-Replikation; [VoxCPM](VoxCPM.md) selbst bietet weitere Klonverfahren. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

cli.py --batch-file verarbeitet laut Anleitung bis zu 100 Aufgaben in einer UTF-8-JSON-/JSONL-Datei von höchstens 1 MiB. Lokale Pfade beziehen sich auf das Manifestverzeichnis, alle Aufgaben werden vor Start vorgeprüft; ein einzelner Fehler hält spätere Aufgaben nicht auf. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

CLI-Parameter übersteuern gespeicherte WebUI-Werte für Untertitel und Sprache; andere Einstellungen werden nicht automatisch übernommen. Eigene Audiodateien erfordern --custom-audio-file. Das ergänzt den früheren README-Stand ohne dessen historische Anbieter-/Preisangaben zu überschreiben. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)
