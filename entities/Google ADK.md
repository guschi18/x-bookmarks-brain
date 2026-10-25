---
tags: [agents, tools]
sources: [tweet-2050939998115930192.md, tweet-2079234800766816633.md]
created: 2026-10-15
updated: 2026-10-20
---

# Google ADK

## Quelle und Zuordnung (Poststand 2026-05)

Das gespeicherte rund 29-minütige Video wird von Ivan Nardini als Google-Cloud-Workshop vorgestellt. Es behandelt das Agent Development Kit, Claude auf Vertex AI, [Model Context Protocol](../concepts/Model%20Context%20Protocol.md), Agent Engine und A2A. Der französische Begleitpost vom 03.05.2026 nennt dagegen einen offiziellen Anthropic-Bauplan für ein autonomes Unternehmen; der Vortrag belegt diese Zuschreibung nicht. Sein ursprüngliches Veranstaltungsdatum ist im Datensatz nicht gesichert. [tweet-2050939998115930192](../sources/tweet-2050939998115930192.md)

## Lokaler Agent und Sitzungen (Poststand 2026-05)

Der Vortrag baut einen Geburtstagsplaner mit LLM-Agent, Namen, Modell, Anweisungen und Tools. Er nennt agent.py, eine Umgebungsvariablendatei und eine Python-Initialisierungsdatei als minimale Projektbestandteile; ein Runner koordiniert Ausführung und Gesprächssitzung. ADK run startet die Terminalinteraktion, ADK web bietet eine Debug-Oberfläche für den Agentenablauf. Die Aufrufnamen sind aus dem gesprochenen Transkript übernommen und hier nicht gegen eine aktuelle CLI geprüft. [tweet-2050939998115930192](../sources/tweet-2050939998115930192.md)

Claude wird im Beispiel über Vertex AI beziehungsweise eine Modellintegration eingebunden; LiteLLM wird als weitere Möglichkeit genannt. Das Transkript wechselt zwischen älteren Claude-Versionen und einer angekündigten Integration von Claude 4. Diese Aussagen dokumentieren den Vortrag und belegen keine heutige Modellverfügbarkeit. [tweet-2050939998115930192](../sources/tweet-2050939998115930192.md)

## MCP und mehrere Agenten (Poststand 2026-05)

Ein zusätzlicher Kalender-Agent nutzt einen MCP-Server zur Terminplanung; ein Orchestrator wählt zwischen Geburtstags- und Kalenderaufgaben. Die Erklärung unterscheidet die Nutzung bestehender MCP-Tools im ADK und die Bereitstellung eigener Werkzeuge über MCP. Das Beispiel zeigt einen konkreten Orchestrierungsansatz, keinen Beweis unbeaufsichtigten Unternehmensbetriebs. [tweet-2050939998115930192](../sources/tweet-2050939998115930192.md)

## Bereitstellung und A2A (Poststand 2026-05)

Für Agent Engine beschreibt der Sprecher die Übergabe eines Agenten mit seinen Anforderungen und Paketen an einen verwalteten Endpunkt sowie Monitoring für Anfragen, Latenz, CPU, Speicher und Sitzungen. Er stellt diese Dienste als Entlastung gegenüber selbst gebautem API-, Container- und Betriebsaufwand dar. Eine Bereitstellung wurde hier nicht durchgeführt. [tweet-2050939998115930192](../sources/tweet-2050939998115930192.md)

A2A wird als Protokoll zur Zusammenarbeit zwischen Agenten unterschiedlicher Frameworks mit Agent Card, Skills und Executor vorgestellt. Der geplante praktische A2A-Teil wird aus Zeitgründen nicht gezeigt, sondern auf ein Webinar verschoben. Das Transkript nennt QR-Codes für Beispielcode, enthält jedoch keine aufgelösten Original-Repository-Links. [tweet-2050939998115930192](../sources/tweet-2050939998115930192.md)

[Google Agents CLI](Google%20Agents%20CLI.md) ist ein verwandter, separat belegter späterer Workflow zum Erstellen, Evaluieren und Bereitstellen von ADK-Agenten; diese Videoquelle dokumentiert den direkten Workshop-Ablauf. [tweet-2050939998115930192](../sources/tweet-2050939998115930192.md)

## Wissensgraph-Kurs (Poststand 2026-07)

Ein separat gespeicherter DeepLearning.AI-Kurs in Partnerschaft mit Neo4j verwendet Google ADK für einen Multi-Agenten-Entwurf: Aus CSV- und Markdown-Daten sollen Graphschema und Extraktionsplan abgeleitet werden. Die Einführung behandelt Tools, Sub-Agenten und Session-State; [Agentic Knowledge Graph Construction](../concepts/Agentic%20Knowledge%20Graph%20Construction.md) beschreibt den Ablauf und die Anbindung über LiteLLM. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)

Das rund 66-minütige Transkript enthält nicht die angekündigten Detaillektionen zur Konstruktion oder das im Post genannte Kapitel „Why Graphs are the future“. Der Kursbeleg dokumentiert deshalb den Entwurf und die ADK-Grundlagen, keine hier ausgeführte vollständige Graphbau-Pipeline. [tweet-2079234800766816633](../sources/tweet-2079234800766816633.md)
