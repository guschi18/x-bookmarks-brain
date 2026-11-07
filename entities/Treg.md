---
tags: [agents, tools]
sources: [tweet-2101988972977434683.md, tweet-2104526472815968694.md, tweet-2104526470760792424.md, tweet-2116122945605222637.md]
created: 2026-10-03
updated: 2026-11-02
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

## /REA-growth: Wachstums-Teardown einer Firma (Stand 2026-10)

Jason Zhou stellt /REA-growth als Open-Source-Skill auf Treg-Basis vor. Eingabe sind ein Firmenname und ein Zeitraum; Treg sammelt Traffic, Suche, KI-Antworten, Ads, Posts, Links und Stellenanzeigen, heraus kommt ein Wachstums-Blueprint, der zeigt, was wann funktionierte. Der Post nennt $0,58 für einen vollständigen Lovable-Teardown, das Treg-Angebot nennt SEO, AEO, Ads und Social als Felder. Der Name hat nichts mit [REA](REA.md) (Reverse Engineer Anything, Binär-RE) zu tun. [tweet-2116122945605222637](../sources/tweet-2116122945605222637.md)

Die gespeicherte Seite treg.to/rea-growth dokumentiert den Lauf vom 23.10.2026 (Zeitraum 09.2024 bis 10.2026, nur US-Suchdaten) mit Kostenaufstellung: Stack, News, Funding und Partner $0,160; Wachstumskurve $0,151; Suche (1.000 Keywords) $0,132; Links und Anker $0,050; Stellenanzeigen $0,040; Ads (4 Netzwerke) $0,031; Rest unter $0,01; Summe $0,58. Drei Abrufe wurden nicht berechnet (Website-History-Anbieter 404, Backlink-Datum abgelehnt, Traffic nach Kanal braucht eigenen Schlüssel). [tweet-2116122945605222637](../sources/tweet-2116122945605222637.md)

Zehn "Spielzüge" mit Aufwand, erstem Ergebnis und Prompt, abgeleitet aus Lovable (Zahlen laut Seite): [tweet-2116122945605222637](../sources/tweet-2116122945605222637.md)

1. Badge "Made with" auf alles, was Nutzer veröffentlichen: Der Linktext "Edit with" steht auf 20.132 verweisenden Domains und 255.420 Backlinks; 134.702 stammen aus Nutzer-Apps. Aufwand eine Woche, Ergebnis in 4-6 Wochen.
2. Zahlen öffentlich posten: Die meistgelikten Posts des Gründers sind Meilensteine und Nutzer-Erfolgsgeschichten. Aufwand eine Stunde pro Woche; der Prompt lässt Entwürfe vorlegen und nie selbst posten.
3. Kundenerfolge als Creator-Videos: meistgesehene YouTube-Treffer sind Verdienst-Geschichten (1,1 Mio. und 959 Tsd. Aufrufe); ob die Videos bezahlt waren, wurde nicht gesehen.
4. In Mitgliedschaften anderer Firmen bündeln (Partnerseiten wie /linkedin-premium-offer, /lenny, /students).
5. Verkäufer bezahlen: Affiliates bis $100 pro Erstabonnent, Experts 10 % je Business-Plan.
6. Vergleichsseiten schreiben, die KI liest: ChatGPT nannte Lovable bei allen drei Käuferfragen zuerst und zitierte zwei /guides-Seiten; die Sektion rankt für 517 Keywords.
7. Beiträge von Mitarbeitern als Ads an Berufsgruppen bewerben: 11 von 16 gesampelten LinkedIn-Ads mit Text sind beworbene Mitarbeiterposts.
8. Ein Land nach dem anderen öffnen: 21 von 24 Top-Meta-Ads auf Portugiesisch, Rolle "Growth Lead, Brazil" seit 29.09.2026.
9. Gratisplan als Tagesgewohnheit (5 Credits pro Tag, bis 30 im Monat); die Seite kennzeichnet dies als gesehen, die Wirkung als Schlussfolgerung.
10. Nutzern beim Wachsen helfen (/grow seit 14.10.2026); Wirkung auf Spielzug 1 ist als Schlussfolgerung gekennzeichnet.

Evidenzgrenze: Der Teardown stammt vom Treg-Anbieter selbst und ist nicht mit Lovable verbunden; Zahlen kommen aus Anbieterdaten, gemeldeter Umsatz aus Nachrichten statt Unterlagen. Raw enthält zu jedem Spielzug einen Prompt, hier nicht im Wortlaut wiedergegeben; das Demo-Video hat kein Transkript. Nicht unabhängig geprüft; Wirkung der Spielzüge ist nicht belegt. [tweet-2116122945605222637](../sources/tweet-2116122945605222637.md)
