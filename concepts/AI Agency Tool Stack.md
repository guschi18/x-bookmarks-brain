---
tags: [agents, tools, product-building, marketing]
sources: [tweet-2092609257338200469.md, tweet-2034924354337714642.md]
created: 2026-10-12
updated: 2026-10-16
---

# AI Agency Tool Stack

## Rollen als Auswahlhilfe (Stand 2026-08)

Der Katalog ordnet Skills, Agenten, Anwendungen und [Model Context Protocol](Model%20Context%20Protocol.md)-Server zehn Rollen zu. Er ist eine Sammlung verlinkter Bausteine, kein getestetes zusammenhängendes Agentensystem. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)

- Engineering: Superpowers (obra/superpowers), [Addy Osmani Agent Skills](../entities/Addy%20Osmani%20Agent%20Skills.md), Karpathy Skills (multica-ai/andrej-karpathy-skills) und GStack (garrytan/gstack). [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)
- Produktdesign: [UI UX Pro Max](../entities/UI%20UX%20Pro%20Max.md), [Taste Skill](../entities/Taste%20Skill.md) und Impeccable (pbakaus/impeccable); die Rolle ergänzt [Design Skills for Coding Agents](Design%20Skills%20for%20Coding%20Agents.md). [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)
- QA: [Codex](../entities/Codex.md), microsoft/playwright-mcp und anthropics/skills. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)
- Dokumente: microsoft/markitdown, anthropics/skills und Frontend Slides; der gespeicherte LinkedIn-Zwischenschritt verweist auf https://github.com/zarazhangrui/frontend-slides. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)
- Marketing: Marketing Skills, AgriciDaniel/claude-seo, blader/humanizer und Apify. Die Beschriftung Marketing Skills wiederholt jedoch denselben Kurzlink wie MarkItDown; dafür ist kein separates Marketing-Skills-Repository belegt. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)
- Social Media: charlie947/social-media-skills, ManyChat und GPT Image. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)
- Motion/Video: Higgsfield, [HyperFrames](../entities/HyperFrames.md), calesthio/OpenMontage und [OpenCut](../entities/OpenCut.md). [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)
- Recherche: [Agent Reach](../entities/Agent%20Reach.md), mvanhorn/last30days-skill und NotebookLM. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)
- Operations: Notion MCP, github/github-mcp-server, thedotmack/claude-mem und mem0ai/mem0. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)
- Rollenübergreifende Sammlungen: msitarzewski/agency-agents, ComposioHQ/awesome-claude-skills, wshobson/agents und alirezarezvani/claude-skills. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)

## Nutzbare Verfahren aus gespeicherter Dokumentation (Stand 2026-08)

Die Karpathy-Skills-README nennt vier Arbeitsprinzipien: vor dem Code Annahmen klären, die kleinste Lösung wählen, nur nötige Stellen ändern und Ziele durch überprüfbare Erfolgskriterien ausdrücken. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)

Die Social-Media-Skills-README beschreibt einen Newsletter als Ausgangspunkt für weitere Kanäle; voice-builder erzeugt about-me.md und voice.md aus Interview und Schreibproben. Persönliche Reichweitenangaben sind Eigenangaben des Autors. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)

Die gespeicherte [OpenCut](../entities/OpenCut.md)-README trennt die angekündigte Neuentwicklung von der weiterhin nutzbaren Classic-Version; angekündigte Editor-API, Plugins, MCP und Headless-Modus dürfen daraus nicht als fertige Funktionen abgeleitet werden. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)

## Überschneidungen und Aussagegrenzen (Stand 2026-08)

Der Beleg enthält 33 externe Ziele und 1452 strukturierte Artikellinks. Codex liefert im gespeicherten Body nur eine Ladefehlermeldung, NotebookLM nur eine Google-Anmeldeseite; diese Inhalte belegen keine Produktfunktionen. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)

Mehrere Repositories sind bereits über eigenständige Quellen im Wiki vertreten; diese Sammlung bewahrt die Rollenordnung und zusätzliche Originaldokumentation. Versionsstände, Kataloggrößen und geänderte Produktnamen in den gespeicherten READMEs können später als der Tweet sein und belegen keinen einheitlichen Stand vom 26. August. Eine Installation aller Bausteine oder deren gemeinsame Funktion wurde nicht geprüft. [tweet-2092609257338200469](../sources/tweet-2092609257338200469.md)

## Zusätzliche Ressourcen aus dem März-Katalog (Stand 2026-03)

Der ältere Katalog ergänzt die Rollenliste um weitere Werkzeuge und Verzeichnisse. Die Kurzbeschreibungen stammen aus dem Artikel vom 20.03.2026; Funktionen, Installation und Sicherheit wurden nicht getestet. Sterne-, Installations-, Benchmark- und Geschwindigkeitsangaben werden nicht als aktuelle Fakten übernommen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)

### Schreiben, Skills und Kontext

- [Doc Co-Authoring](https://github.com/anthropics/skills/tree/main/skills/doc-coauthoring) — gemeinsames Schreiben von Dokumenten mit menschlichen und Claude-Beiträgen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [File Search](https://github.com/massgen/massgen) — als File Search verlinktes MassGen-Repository für Suchabläufe mit ripgrep und ast-grep; der Artikel nennt keinen direkten Skill-Pfad. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Context Optimization](https://github.com/muratcankoylan/agent-skills-for-context-engineering) — Skills für Kontextoptimierung und KV-Cache-bezogene Verfahren. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Marketing Skills by Corey Haines](https://github.com/coreyhaines31/marketingskills) — Marketing-Skills zu CRO, Texten, SEO und E-Mail-Sequenzen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)

### MCP und Recherche

- [Excel MCP Server](https://github.com/haris-musa/excel-mcp-server) — Excel-Dateien über einen MCP-Server bearbeiten. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Context7](https://github.com/upstash/context7) — Bibliotheksdokumentation in den Modellkontext einbinden. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Task Master AI](https://github.com/eyaltoledano/claude-task-master) — PRDs in Aufgaben mit Abhängigkeiten für Coding-Agenten zerlegen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [GPT Researcher](https://github.com/assafelovic/gpt-researcher) — Recherche autonom ausführen und zu Berichten zusammenstellen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Vanna AI](https://github.com/vanna-ai/vanna) — natürliche Sprache in SQL umsetzen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [claude-deep-research-skill](https://github.com/199-biotechnologies/claude-deep-research-skill) — achtphasiger Recherche-Skill mit automatischer Fortsetzung. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [MCP Playwright](https://github.com/executeautomation/mcp-playwright) — Browserautomatisierung über einen Playwright-MCP-Server; das konkrete executeautomation-Repository ist vom allgemeinen Playwright-Einsatz zu unterscheiden. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [stealth-browser-mcp](https://github.com/vibheksoni/stealth-browser-mcp) — Browserautomatisierung mit Tarnungsanspruch; die behauptete Nichterkennbarkeit ist nicht belegt. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [markdownify-mcp](https://github.com/zcaceres/markdownify-mcp) — PDFs, Bilder und Audio in Markdown umwandeln. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [MCPHub](https://github.com/samanhappy/mcphub) — mehrere MCP-Server über HTTP verwalten. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)

### Agenten, lokale Modelle und Orchestrierung

- [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) — Agentenplattform für länger laufende Aufgaben. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [OWL](https://github.com/camel-ai/owl) — Zusammenarbeit mehrerer Agenten. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [LlamaFile](https://github.com/Mozilla-Ocho/llamafile) — lokale Sprachmodelle als einzelne ausführbare Datei bereitstellen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Huginn](https://github.com/huginn/huginn) — selbst betriebene Web-Agenten für Monitoring und Benachrichtigungen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [cmux](https://github.com/craigsc/cmux) — mehrere Claude-Code-Agenten mit getrennten Git-Worktrees organisieren; anderes Projekt als [Cmux](../entities/Cmux.md) von manaflow-ai. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [figaro](https://github.com/byt3bl33d3r/figaro) — Claude-Agentenflotten auf dem Desktop orchestrieren. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [claude-squad](https://github.com/smtg-ai/claude-squad) — Terminal-Agenten in parallelen Sitzungen verwalten. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [SWE-AF](https://github.com/Agent-Field/SWE-AF) — ein Engineering-Agententeam über einen API-Aufruf starten. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [AIlice](https://github.com/myshell-ai/AIlice) — komplexe Aufgaben durch dynamisch erzeugte Agenten bearbeiten. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Agent Alchemy](https://github.com/sequenzia/agent-alchemy) — [Claude Code](../entities/Claude%20Code.md) mit Plugins und Aufgabenverwaltung verbinden. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [gptme](https://github.com/gptme/gptme) — persönlicher KI-Agent im Terminal. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Claude Inspector](https://github.com/kangraemin/claude-inspector) — Promptmechanik von [Claude Code](../entities/Claude%20Code.md) sichtbar machen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [TDD Guard](https://github.com/nizos/tdd-guard) — Test-first-Arbeit bei KI-Agenten erzwingen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [rendergit (Karpathy)](https://github.com/karpathy/rendergit) — Git-Repository in eine einzelne lesbare Datei umwandeln. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)

### Infrastruktur und Sicherheit

- [NVIDIA NemoClaw](https://github.com/NVIDIA/NemoClaw) — Sandbox für autonome Agenten. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Ghost OS](https://github.com/ghostwright/ghost-os) — Mac-Anwendungen durch Agenten bedienen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [e2b/desktop](https://github.com/e2b-dev/desktop) — isolierte virtuelle Desktops für Agenten bereitstellen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [container-use (Dagger)](https://github.com/dagger/container-use) — Containerumgebungen für Coding-Agenten verwenden. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Canopy](https://github.com/kwalus/Canopy) — verschlüsseltes P2P-Mesh für KI-Agenten; anderes Projekt als das CAN-Bus-Werkzeug CanoPy. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [agent-governance-toolkit (Microsoft)](https://github.com/microsoft/agent-governance-toolkit) — Sicherheits-Middleware für Agenten. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [claude-code-security-review (Anthropic)](https://github.com/anthropics/claude-code-security-review) — Pull Requests auf Sicherheitsprobleme untersuchen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [promptfoo](https://github.com/promptfoo/promptfoo) — automatisierte Sicherheitsprüfungen für KI-Modelle. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)

### Gedächtnis

- [Mem9](https://github.com/mem9-ai/mem9) — Gedächtnissystem für KI-Agenten. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Codefire](https://github.com/websitebutlers/codefire-app) — persistentes Gedächtnis für Coding-Agenten. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Memobase](https://github.com/memodb-io/memobase) — Nutzerprofil-Gedächtnis für LLMs. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)

### Suche, Daten und Modellzugang

- [CK (BeaconBay)](https://github.com/BeaconBay/ck) — Code semantisch statt nur mit Schlüsselwörtern durchsuchen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [ExtractThinker](https://github.com/enoch3712/ExtractThinker) — Dokumentenverarbeitung mit einer ORM-artigen Schnittstelle. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [OmniRoute](https://github.com/diegosouzapw/OmniRoute) — API-Proxy für unterschiedliche KI-Anbieter. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [dlt](https://github.com/dlt-hub/dlt) — Datenpipelines für verschiedene Quellen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [simonw/llm](https://github.com/simonw/llm) — CLI für lokale und entfernte Sprachmodelle. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Portkey-AI/gateway](https://github.com/Portkey-AI/gateway) — Anfragen zwischen Sprachmodellen und Anbietern routen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [lmnr](https://github.com/lmnr-ai/lmnr) — Agentenverhalten nachverfolgen und evaluieren. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)

### Video und weitere Anwendungen

- [LTX-Desktop (Lightricks)](https://github.com/Lightricks/LTX-Desktop) — Videos lokal generieren und bearbeiten. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [MetaClaw](https://github.com/aiming-lab/MetaClaw) — Agenten ohne eigenen GPU-Betrieb weiterentwickeln; der Artikel liefert keine technische Anleitung oder Messung. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Vane](https://github.com/ItzCrazyKns/Vane) — Antwortmaschine mit lokalen Sprachmodellen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)

### Projektverzeichnisse

- [Awesome Claude Skills](https://github.com/travisvn/awesome-claude-skills) — kuratiertes Claude-Skills-Verzeichnis von travisvn; eigene Sammlung neben der bereits vorhandenen Composio-Liste. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [Awesome Agents](https://github.com/kyrolabs/awesome-agents) — Sammlung von Open-Source-Agentenwerkzeugen. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [MAGI//ARCHIVE](https://tom-doerr.github.io/repo_posts/) — Feed mit neuen KI-Repositories. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)

### Weitere Skill-Verzeichnisse

- [SkillsMP](https://skillsmp.com/) — im Artikel als Community-Skills-Katalog genannt. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [AI Templates Skills](https://aitmpl.com/skills) — im Artikel als Skill- und Vorlagenverzeichnis mit Installation genannt. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
- [SkillHub](https://skillhub.club/) — im Artikel als bewertetes Skills-Verzeichnis genannt; Umfang und Bewertungen sind nicht nachgeprüft. [tweet-2034924354337714642](../sources/tweet-2034924354337714642.md)
