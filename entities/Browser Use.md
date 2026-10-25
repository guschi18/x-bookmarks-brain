---
tags: [agents, tools]
sources: [tweet-2073784353771897046.md, tweet-1997345279859962076.md]
created: 2026-09-29
updated: 2026-10-24
---

# Browser Use

## Rolle und Produkt

Im gespeicherten Interview beschreibt der Mitgründer [Browser Use](Browser%20Use.md) als Open-Source-Browserautomatisierung und Browser Harness als kleine Erweiterung, mit der Coding-Agenten einen lokalen Browser steuern und fehlende Werkzeuge selbst ergänzen können. [tweet-2073784353771897046](../sources/tweet-2073784353771897046.md)

Er nennt die Browsersteuerung per CDP, ein Telegram-Interface für dauerhaft laufende Agenten und Vorschläge, die ein Mensch vor außenwirksamen Aktionen freigibt. [tweet-2073784353771897046](../sources/tweet-2073784353771897046.md)

## Beispiele und Grenzen

Der Gast erzählt von Einkauf, Nachrichten und Produktarbeit mit seinem Agenten; es sind Selbstauskünfte und Demonstrationen im Gespräch, keine reproduzierbaren Zuverlässigkeitsmessungen. [tweet-2073784353771897046](../sources/tweet-2073784353771897046.md)

Das Interview thematisiert auch Verlust von Kontrolle und zu viele Agentenvorschläge; der Gast will Sendungen und Veröffentlichungen selbst genehmigen. [tweet-2073784353771897046](../sources/tweet-2073784353771897046.md)

Verwandte Arbeitsweisen: [Loop Engineering](../concepts/Loop%20Engineering.md) und [Agentic Engineering](../concepts/Agentic%20Engineering.md). [tweet-2073784353771897046](../sources/tweet-2073784353771897046.md)

## Skills als API-Angebot (Stand 2025-12)

Gregor Zunic stellt Browser Use Skills als Dienst vor: Automatisierungsziel beschreiben, API bauen lassen, API aufrufen. Das Bild verspricht eine Website-API aus einem Prompt. Dieser Launch-Claim ist kein Nachweis universeller Zuverlässigkeit. [tweet-1997345279859962076](../sources/tweet-1997345279859962076.md)

## Web Agents und heutiger Nachfolger (Recherche-Stand 2026-10-24)

Auf Nutzerwunsch ergänzte Website: [Browser Use Web Agents](https://browser-use.com/web-agents). Laut Hersteller erledigen gehostete Agenten Browser-Aufgaben und liefern strukturierte Daten; Ergebnisse lassen sich abrufen oder über Webhooks empfangen. Der [Quickstart](https://docs.browser-use.com/cloud/quickstart) trennt Agenten-Aufträge via POST /api/v4/runs von Cloud-Browsern, die eigener Playwright-/Browser-Use-Code über CDP steuert. Das sind aktuelle Primärquellen, keine Aussagen aus dem Tweet von 2025. [tweet-1997345279859962076](../sources/tweet-1997345279859962076.md)

Die [Legacy-Skills-Dokumentation](https://docs.browser-use.com/cloud/legacy/skills) erklärt Skills für eingestellt: skills.create, skills.refine und manuelle Aufzeichnung liefern 410 Gone. Bestehende Skills können weiter laufen; Marketplace-Skills lassen sich weiterhin klonen und ausführen. Der alte Launch ist deshalb keine aktuelle Anleitung zur Erstellung neuer Skills. [tweet-1997345279859962076](../sources/tweet-1997345279859962076.md)

Die [aktuelle Skript-Anleitung](https://docs.browser-use.com/cloud/agent/scripts) ersetzt den neuen Skill durch einen Ablauf: Cloud-Workspace anlegen, den Agenten einen wiederkehrenden Auftrag erledigen und getesteten Code speichern lassen; bei Folgeaufrufen workspace_id mitgeben und Ergebnisstruktur sowie Aktualität prüfen. Ein Workspace hält Dateien, keine laufenden Prozesse; jeder Folgeaufruf startet weiterhin einen Agenten und verbraucht Tokens. [tweet-1997345279859962076](../sources/tweet-1997345279859962076.md)

Für Live-Daten fordert die Anleitung einen neuen Abruf je Lauf, fetched_at und einen Hash der Antwort; bei Seitenänderungen soll der Agent das Skript reparieren. Das ist ein konkretes Muster für [Loop Engineering](../concepts/Loop%20Engineering.md), aber keine Garantie, dass Änderungen selbstständig korrekt behoben werden oder jeder Lauf günstiger wird. [tweet-1997345279859962076](../sources/tweet-1997345279859962076.md)

Die Primärtexte wurden am 24.10.2026 separat unter output/browser-use-research-2026-10-24/primary-sources.json gesichert. Ein API-Schlüssel wäre für eine echte Cloud-Ausführung erforderlich; hier wurden weder Aufgaben gestartet noch Anmeldedaten übertragen oder Hersteller-Benchmarks unabhängig geprüft. [tweet-1997345279859962076](../sources/tweet-1997345279859962076.md)
