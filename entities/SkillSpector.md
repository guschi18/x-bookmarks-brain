---
tags: [security, agents, tools]
sources: [tweet-2112623636905591040.md]
created: 2026-11-01
updated: 2026-11-01
---

# SkillSpector

## Überblick (Stand 2026-10)

NVIDIA/SkillSpector ist ein Sicherheitsscanner für KI-Agent-Skills (Claude Code, Codex, MCP). Er soll beantworten, ob ein Skill vor der Installation sicher ist. Der Sammelpost nennt ihn "NVIDIA Skill Inspector"; das Repository heißt SkillSpector. [tweet-2112623636905591040](../sources/tweet-2112623636905591040.md)

Laut README gehört er zur NVIDIA-Verified-Skills-Pipeline, die Skills scannt, bewertet und signiert, bevor sie im NVIDIA-Skills-Katalog erscheinen. [tweet-2112623636905591040](../sources/tweet-2112623636905591040.md)

## Funktionen laut README

- 71 Schwachstellenmuster in 17 Kategorien, darunter Prompt Injection, Datenabfluss, Rechteausweitung, Lieferkette, übermäßige Handlungsfreiheit, Memory Poisoning, MCP Least Privilege und MCP Tool Poisoning. [tweet-2112623636905591040](../sources/tweet-2112623636905591040.md)
- Zwei Stufen: schnelle statische Analyse und optionale semantische LLM-Auswertung. [tweet-2112623636905591040](../sources/tweet-2112623636905591040.md)
- Eingaben: Git-Repositories, URLs, Zip-Dateien, Verzeichnisse oder einzelne Dateien. [tweet-2112623636905591040](../sources/tweet-2112623636905591040.md)
- Live-Abfragen gegen OSV.dev mit Offline-Rückfall; Ausgabe als Terminal, JSON, Markdown oder SARIF; Risikowert 0-100. [tweet-2112623636905591040](../sources/tweet-2112623636905591040.md)
- Baseline zur Unterdrückung bekannter Funde, damit Wiederholungsläufe nur Neues zeigen. [tweet-2112623636905591040](../sources/tweet-2112623636905591040.md)

Installation: `uv tool install git+https://github.com/NVIDIA/skillspector.git`, wahlweise mit MCP-Extra, per Docker (`skillspector scan ./my-skill/ --no-llm`) oder aus dem Quellcode. [tweet-2112623636905591040](../sources/tweet-2112623636905591040.md)

## Evidenzgrenze

Die README nennt für ein Analyse-Teilset von 31.132 Skills 26,1 % mit Schwachstellen und 5,2 % mit wahrscheinlich bösartiger Absicht; das sind Angaben der Autoren zu ihrem Datensatz, hier nicht geprüft. Der Scanner wurde nicht ausgeführt. Verwandt: [Cloudflare Security Audit Skill](Cloudflare%20Security%20Audit%20Skill.md) (Code-Audit), [Strix](Strix.md) (Pentest) und [Claude Code Security Hardening](../concepts/Claude%20Code%20Security%20Hardening.md). [tweet-2112623636905591040](../sources/tweet-2112623636905591040.md)
