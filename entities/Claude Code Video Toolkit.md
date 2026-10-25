---
tags: [agents, tools, product-building]
sources: [tweet-2063935703189262622.md]
created: 2026-09-30
updated: 2026-09-30
---

# Claude Code Video Toolkit

## Projekt und Einstieg

Das Repository [digitalsamba/claude-code-video-toolkit](https://github.com/digitalsamba/claude-code-video-toolkit) stellt laut README Skills, Befehle, Templates und Werkzeuge für [Agentic Video Production](../concepts/Agentic%20Video%20Production.md) mit [Claude Code](Claude%20Code.md) bereit. Der gespeicherte Screenshot zeigt v0.15.0 und MIT; die README beschreibt den Menschen als Regisseur, Editor und Designer. [tweet-2063935703189262622](../sources/tweet-2063935703189262622.md)

Die Anleitung beginnt mit Klonen und optionalen Python-Anforderungen, dann /setup für GPU, Speicherung und Stimme sowie /video für ein Template-Projekt. Als Anforderungen nennt sie Node.js 18+ und Claude Code, empfiehlt Python 3.9+ und bezeichnet FFmpeg als optional; ein hello-world-Beispiel soll ohne API-Keys direkt rendern. [tweet-2063935703189262622](../sources/tweet-2063935703189262622.md)

## Produktionsablauf und Zustand

Der dokumentierte Ablauf ist Skript → Assets → Szenenreview → Design → Audio → Vorschau → Render → Veröffentlichung. Remotion und MoviePy liefern Kompositionen, Playwright zeichnet Browser-Demos auf, FFmpeg übernimmt Medienbearbeitung; /scene-review und /design schaffen explizite Prüf- und Überarbeitungsschritte. [tweet-2063935703189262622](../sources/tweet-2063935703189262622.md)

Templates umfassen Sprint-Reviews, Produktdemos und vertikale Erklärvideos. Markenprofile halten Farben, Schriften, Logo und Stimme fest; project.json speichert Szenen, Audio, Sitzungen und Phase. Laut README gleicht das System geplante Assets mit vorhandenen Dateien ab und erzeugt Projektkontext zur Wiederaufnahme. [tweet-2063935703189262622](../sources/tweet-2063935703189262622.md)

## Modelle und Integrationen

Die README nennt unter anderem Qwen3-TTS, FLUX.2, Qwen-Image-Edit, ACE-Step, LTX-2 und SadTalker sowie ElevenLabs. Acht GPU-Werkzeuge werden über Modal oder RunPod angeboten; die Cent-Kosten und kostenlosen Kontingente sind Projektangaben ohne unabhängige Messung und keine Zusicherung aktueller Preise. [tweet-2063935703189262622](../sources/tweet-2063935703189262622.md)

Ein experimentelles Migrationsskript überträgt Skills und Workflows zu [Codex](Codex.md) und erzeugt einen AGENTS.md-Block aus CLAUDE.md. Die 38 gespeicherten strukturierten Links einschließlich Migrationsdokumentation bleiben auf der Source-Seite erhalten; weder Migration noch Renderqualität wurden hier ausgeführt oder geprüft. [tweet-2063935703189262622](../sources/tweet-2063935703189262622.md)
