---
tags: [agents, tools]
sources: [tweet-2115424619460997188.md]
created: 2026-11-01
updated: 2026-11-01
---

# FFmpeg Skill

## Überblick (Stand 2026-10)

kajisho5/ffmpeg-skill gibt Coding-Agents (Claude Code, Cursor, Codex, jeden MCP-Client) einen lokalen Videoeditor auf FFmpeg-Basis: ohne Cloud, ohne API-Schlüssel, nur Python-Standardbibliothek. Der Skill lehrt einen festen Ablauf (prüfen, möglichst verlustfrei schneiden, kontrollieren, verifizieren) und bringt 42 Werkzeuge mit: Schnitt, Zusammenfügen, Stille entfernen, Seitenverhältnis, Untertitel, Overlays, HDR-zu-SDR, Audiobereinigung, Sync, Multicam, Lautheit und Lieferprüfungen. [tweet-2115424619460997188](../sources/tweet-2115424619460997188.md)

## Kleiner MCP-Einstieg

Alle Werkzeuge sind als MCP-Tools aufrufbar, aber `tools/list` meldet standardmäßig nur einen Kern von 12, um den Kontext des Clients klein zu halten. Mit `FFMPEG_SKILL_MCP_FULL=1` erscheinen alle 42; per Namen sind alle immer über `tools/call` erreichbar. Der Tweet leitet daraus ab: je mehr Werkzeuge, desto schlanker der Einstieg. [tweet-2115424619460997188](../sources/tweet-2115424619460997188.md)

## Vertrag und Rolle

Das Eingabeschema jedes Tools wird zur Laufzeit aus demselben argparse-Parser abgeleitet wie die CLI; CI schlägt bei Abweichung fehl (laut README "SPEC"). Der Skill entscheidet nicht, was geschnitten wird; das übernimmt ein vorgeschaltetes "Gehirn" wie die verwandten Repositories video-production-agent und AI-video-production-OS desselben Autors. [tweet-2115424619460997188](../sources/tweet-2115424619460997188.md)

## Evidenzgrenze

Nur README und Tweet gelesen, nichts ausgeführt; die Demos sind laut README aus synthetischem Material erzeugt. Einordnung: [Agentic Video Production](../concepts/Agentic%20Video%20Production.md). [tweet-2115424619460997188](../sources/tweet-2115424619460997188.md)
