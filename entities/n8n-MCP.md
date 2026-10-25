---
tags: [tools, agents]
sources: [tweet-2037907310136484036.md, tweet-2008538584085594458.md, tweet-1997624662189122047.md]
created: 2026-10-22
updated: 2026-10-24
---

# n8n-MCP

## Überblick

[n8n-MCP](https://github.com/czlonkowski/n8n-mcp) ist ein MCP-Server, der KI-Assistenten wie [Claude Code](Claude%20Code.md), Claude Desktop, Windsurf und Cursor Zugriff auf Dokumentation, Eigenschaften und Operationen der n8n-Knoten gibt, damit sie n8n-Workflows bauen können. Der Post vom 28.03.2026 listet das Repository unter Claude-Code-Tipps. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)

## Umfang laut README (Herstellerangaben)

- 2.541 Knoten (832 Kern, 1.709 Community, davon 1.441 verifiziert); 99 % Abdeckung der Eigenschaften, 66,5 % der Operationen, 86 % der Dokumentation. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
- 2.352 Workflow-Templates, 156 gerankte Beispielkonfigurationen und 267 erkannte KI-taugliche Tool-Varianten. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)

## Betrieb und Sicherheit

- Schnellstart über ein gehostetes Dashboard mit Gratisstufe von 100 Tool-Aufrufen pro Tag; Selbst-Hosting per npx, Docker, Railway oder lokal. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)
- Die README warnt ausdrücklich: Produktions-Workflows nie direkt mit KI bearbeiten; vorher Kopie anlegen, in einer Entwicklungsumgebung testen, Backups exportieren und Änderungen validieren. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)

## Grenzen

Die Zahlen sind unabhängig nicht geprüft und stehen im Stand der gespeicherten README, nicht im Stand des Posts. [tweet-2037907310136484036](../sources/tweet-2037907310136484036.md)

## Begleitende n8n-Skills (Stand 2026-01)

Tom beschreibt, dass Claude mit dem n8n-MCP-Server zwar Knotendokumentation, Templates und Schemas abrufen kann, bei Fehlern aber ohne Erfahrungswissen im Kreis rät. [tweet-2008538584085594458](../sources/tweet-2008538584085594458.md) Abhilfe seien sieben Skills aus dem Repository von czlonkowski: Expression-Syntax, wirksame Nutzung des MCP-Servers, Workflow-Muster (Webhook, API-Integration, Datenbank, KI-Agent, geplante Aufgaben), Validierung und Debugging, Node-Konfiguration sowie JavaScript und Python für Code-Nodes. [tweet-2008538584085594458](../sources/tweet-2008538584085594458.md) Installation: nur den Skills-Ordner laden, jeden der sieben Ordner einzeln zippen und in Claude unter Einstellungen > Capabilities > Skills hochladen. [tweet-2008538584085594458](../sources/tweet-2008538584085594458.md) Als Beleg nennt der Autor einen einzelnen Mentee, dessen Workflow-Problem danach lösbar war; das ist eine Einzelanekdote ohne Messung. [tweet-2008538584085594458](../sources/tweet-2008538584085594458.md)

## Früher Skill-Post und gespeicherter README-Stand (Stand 2025-12)

Tom Dörr verlinkt [czlonkowski/n8n-skills](https://github.com/czlonkowski/n8n-skills) als Anleitung für [Claude Code](Claude%20Code.md) zum Bau von n8n-Workflows. Das damalige Bild nennt fünf Skills; die später gespeicherte README nennt 14. Die 14 sind deshalb kein belegter Funktionsstand vom 07.12.2025 und ersetzen nicht rückwirkend die oben dokumentierten sieben Skills vom Januar 2026. [tweet-1997624662189122047](../sources/tweet-1997624662189122047.md)

### Verfahren im später gespeicherten README-Stand

Die README gliedert die Anleitung in Expression-Syntax, MCP-Tools, Workflow-Muster, Validierung, Node-Konfiguration, JavaScript, Python, Code Tool, Fehlerbehandlung, Binärdaten, Sub-Workflows, KI-Agenten, mehrere Instanzen und Self-Hosting. Ein SessionStart-Router und Pre-/PostToolUse-Hooks sollen passende Hinweise automatisch einblenden; diese Hooks gelten laut README für Plugin-Installationen, nicht für einzeln hochgeladene Claude.ai-Skills. [tweet-1997624662189122047](../sources/tweet-1997624662189122047.md)

Konkrete Fehlerfallen: Webhook-Nutzdaten liegen unter $json.body; normale Code-Nodes geben eine Liste von json-Objekten zurück, der Agent-Code-Tool-Node dagegen einen String. Für Binärdateien ist $binary zuständig; ein JSON-Transformationsschritt kann die Datei verlieren. Bei mehreren Instanzen ist das Ziel vor Credential-Schreibzugriffen zu prüfen. [tweet-1997624662189122047](../sources/tweet-1997624662189122047.md)

Die Anleitung schlägt für wiederkehrende Teilabläufe typisierte Sub-Workflows und für unbeaufsichtigte Läufe Fehlerausgänge, begrenzte Wiederholungen und Error-Trigger vor. Installation laut README beispielsweise mit /plugin install czlonkowski/n8n-skills; Voraussetzung ist der n8n-MCP-Server. Dies sind dokumentierte Projektverfahren, keine hier getesteten Fehlerquoten oder Produktionsfreigaben. [tweet-1997624662189122047](../sources/tweet-1997624662189122047.md)
