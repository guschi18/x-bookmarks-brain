---
tags: [agents, tools]
sources: [tweet-2101988972977434683.md, tweet-2104526472815968694.md, tweet-2104526470760792424.md]
created: 2026-10-03
updated: 2026-10-24
---

# Treg

## Registry (Stand 2026-09)

https://github.com/superdesigndev/treg beschreibt eine Registry für Agenten-Tools: Katalog-APIs, eigene Endpoints, CLIs und Skills werden über einen Organisations-Token erreichbar; https://treg.to/ ist der gehostete Dienst. Der Proxy soll Upstream-Requests mit serverseitig injizierter Auth weiterreichen. [tweet-2101988972977434683](../sources/tweet-2101988972977434683.md)

## Aufruf und Abrechnung (Stand 2026-09)

Die README nennt treg catalog search/get zur Auswahl mit Preis und Parametern, treg call für Requests und treg balance für Kosten. Eigene Team-Tools oder gespeicherte Keys haben Vorrang, danach folgen verifizierte öffentliche Routen und schließlich kostenpflichtige Treg-Keys; fehlende veröffentlichte Preise werden abgelehnt. Normale Katalogsuche wählt Anbieter nicht still automatisch, ausdrücklich geroutete treg.<capability>-Endpoints sind eine Ausnahme. [tweet-2101988972977434683](../sources/tweet-2101988972977434683.md)

Teams speichern Secrets, Tools und Skill-Bundles gemeinsam; OAuth-Verbindungen können erneuert und Credential-Health geprüft werden. treg scan ist Vorschau, treg upload registriert erkannte Keys/Skills/CLIs. treg run führt standardmäßig lokal aus, --server auf dem Registry-Server; die pauschale Aussage, Keys verließen nie den Server, gilt damit nicht ungeprüft für alle CLI-Pfade. [tweet-2101988972977434683](../sources/tweet-2101988972977434683.md)

## Integration und Betrieb (Stand 2026-09)

Die README beschreibt Claude-Code-Plugin, Workflow-Skills und [Model Context Protocol](../concepts/Model%20Context%20Protocol.md)-Oberflächen /mcp/ sowie /mcp/v2/, letztere nur für kuratierte Katalogendpoints mit getrennten Read-/Write-Signalen. Sie nennt lokale SQLite- und produktive Postgres-Konfiguration, Fernet-Verschlüsselung und eine ausdrücklich zu sichernde persistente Schlüsselkonfiguration. Ohne festen Fernet-Key können Secrets nach Neustart unlesbar sein. [tweet-2101988972977434683](../sources/tweet-2101988972977434683.md)

## Grenzen (Stand 2026-09)

Die README nennt Apache 2.0 mit Zusatzbedingungen gegen Weiterverteilung als konkurrierenden gehosteten Registry-Dienst; das ist keine hier geprüfte uneingeschränkte Apache-Lizenz. CLI-Telemetrie auf treg.to lässt sich laut README mit TREG_TELEMETRY=0 oder DO_NOT_TRACK=1 abschalten. API-Katalog, Sicherheitsgrenzen, Preise und Abrechnung sind Anbieterbeschreibungen ohne eigenen Test; Roadmap und bereits beschriebene MCP-Integration zeigen verschiedene Textstände. [tweet-2101988972977434683](../sources/tweet-2101988972977434683.md)

## Lead-Signals als Workflow (Stand 2026-09)

Die gespeicherte README beschreibt lead-signals als Workflow zum Finden kaufbereiter Interessenten aus öffentlichen Signalen: Beschwerden, Jobwechsel, Stellenanzeigen, Funding und Tool-Adoption. Monitoring kann ein Thema, einen Wettbewerber oder eine Accountliste beobachten. Artefakt: https://github.com/superdesigndev/treg/blob/main/skills/lead-signals/SKILL.md ; Oberfläche: https://treg.to/leads-signals . [tweet-2104526472815968694](../sources/tweet-2104526472815968694.md)

Für einen vorhandenen Agenten nennt sie npx skills add superdesigndev/treg --skill lead-signals; vorher die Registry einrichten, da die Workflow-Aufrufe über Treg laufen. Der Bookmark fokussiert diese Anwendung derselben bereits beschriebenen Registry; es wurde weder ein eigener Lead-Lauf noch eine Conversion-Prüfung durchgeführt. [tweet-2104526472815968694](../sources/tweet-2104526472815968694.md)

## Leads-Signals Landingpage und Preis (Stand 2026-09)

Jason Zhou veröffentlicht `/leads-signal` als Open-Source-Skill auf Treg-Basis. Er nennt $0.0002 pro Signal gegenüber Clay-Plänen für $167 pro Monat und weitere 23 Signalarten. Die Landingpage https://treg.to/leads-signals beschreibt Signalquellen (Stellenanzeigen, Funding, Tech-Stack, Jobwechsel, LinkedIn, Reddit, X) und einen Beispiellauf mit 4.710 Signalen für $0.52 vom 26.09.2026; Personen und der Jobwechsel sind laut Seite illustrativ. Preis- und Vergleichszahlen sind Autor- und Anbieterangaben ohne eigene Messung. [tweet-2104526470760792424](../sources/tweet-2104526470760792424.md)

Die README (Abschnitt Workflow-Skills, https://github.com/superdesigndev/treg#workflow-skills) listet neben lead-signals die Skills treg, web-access und recruit. [tweet-2104526470760792424](../sources/tweet-2104526470760792424.md)
