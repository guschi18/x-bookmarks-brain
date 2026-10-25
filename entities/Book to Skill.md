---
tags: [agents, tools]
sources: [tweet-2080988734233715128.md]
created: 2026-10-02
updated: 2026-10-02
---

# Book to Skill

## Rolle (Stand 2026-07)

book-to-skill ist laut Post ein freies Open-Source-Werkzeug, das ein Buch in eine Skill für Claude umwandelt, damit nicht das ganze Buch im Kontext liegt. Das README-Bild nennt als Ziele GitHub Copilot CLI, Amp und [Claude Code](Claude%20Code.md). [tweet-2080988734233715128](../sources/tweet-2080988734233715128.md)

## Erzeugte Artefakte (Stand 2026-07)

- SKILL.md mit Hauptkonzepten und vollständigem Inhaltsverzeichnis [tweet-2080988734233715128](../sources/tweet-2080988734233715128.md)
- eine eigene Datei pro Kapitel, die nur bei Bedarf geladen wird [tweet-2080988734233715128](../sources/tweet-2080988734233715128.md)
- Glossar der Schlüsselbegriffe mit Verweisen [tweet-2080988734233715128](../sources/tweet-2080988734233715128.md)
- Dokument mit allen Techniken, Mustern und Algorithmen des Buchs [tweet-2080988734233715128](../sources/tweet-2080988734233715128.md)
- Kurzreferenz mit Regeln und Entscheidungstabellen [tweet-2080988734233715128](../sources/tweet-2080988734233715128.md)

Das README-Bild fasst den Ablauf als Point, Distill, Load on demand zusammen. [tweet-2080988734233715128](../sources/tweet-2080988734233715128.md)

## Behauptete Wirkung und Grenzen (Stand 2026-07)

Der Post rechnet mit etwa 200.000 Token für ein vollständig geladenes 400-Seiten-Buch; das README bewirbt 24- bis 51-fach weniger Tokenverbrauch und der Post weniger Halluzinationen. Beides ist unbelegte Projektangabe. Die Repo-URL fehlt im Raw; der Nutzer-Nachtrag unten ergänzt sie. Das Prinzip des bedarfsweisen Ladens gehört zu [Context Engineering](../concepts/Context%20Engineering.md). [tweet-2080988734233715128](../sources/tweet-2080988734233715128.md)

## Geprüfter Repository-Nachtrag (Stand 2026-07)

Der Nutzer hat [virgiliojr94/book-to-skill](https://github.com/virgiliojr94/book-to-skill) zu diesem Bookmark nachgereicht. Laut README wird es per `npx skills add virgiliojr94/book-to-skill` installiert und mit `/book-to-skill <path|folder|glob> [skill-name]` aufgerufen. Es arbeitet mit allen Hosts des offenen Agent-Skills-Standards, darunter GitHub Copilot CLI, [Claude Code](Claude%20Code.md), Amp, Hermes Agent, OpenCode und OpenClaw, und liest PDF, EPUB, DOCX, HTML, RTF, MOBI, Text, Markdown, reStructuredText und AsciiDoc. [tweet-2080988734233715128](../sources/tweet-2080988734233715128.md)

Die README beziffert die Bausteine auf etwa 4.000 Token für SKILL.md, je etwa 1.000 pro Kapitel und Kurzreferenz, 1.500 für das Glossar und 2.000 für patterns.md. Die MIT-Lizenz gilt für den Konverter, nicht für die verarbeiteten Bücher. Die Tokenersparnis bleibt eine Projektangabe; die Sternzahl (33,3 Tausend beim Abruf) ist ein Snapshot. [tweet-2080988734233715128](../sources/tweet-2080988734233715128.md)
