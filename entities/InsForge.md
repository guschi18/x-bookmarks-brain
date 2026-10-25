---
tags: [agents, tools, product-building]
sources: [tweet-2097242863964958760.md]
created: 2026-10-03
updated: 2026-10-03
---

# InsForge

## Überblick (Stand 2026-09)

InsForge ist laut README eine quelloffene Backend-Plattform für agentisches Programmieren mit Authentifizierung, Postgres-Datenbank, S3-kompatiblem Speicher, Edge Functions, Model Gateway (OpenAI-kompatibel), Compute (private Vorschau) und Site-Deployment. Agenten nutzen sie über einen MCP-Server (selbst gehostet und Cloud) oder über CLI plus Skills (nur Cloud); selbst hosten geht mit Docker Compose. [tweet-2097242863964958760](../sources/tweet-2097242863964958760.md)

## Kontext-Architektur (Stand 2026-09)

Der Artikel beschreibt drei Schichten: Skills für statisches Wissen, die CLI für Operationen und MCP für den aktuellen Zustand. Vier schmale Skills (insforge, insforge-cli, insforge-debug, insforge-integrations) laden zunächst nur Name und Beschreibung; der volle Inhalt kommt nur bei passender Aufgabe. Die CLI liefert mit `--json` strukturierte Ausgaben und semantische Exit-Codes, sodass Agenten Auth-, Projekt- und Rechtefehler erkennen. Das MCP-Werkzeug `get_backend_metadata` liefert die gesamte Backend-Topologie samt Hinweisen in einem Aufruf von etwa 500 Tokens. [tweet-2097242863964958760](../sources/tweet-2097242863964958760.md)

Der Artikel führt für Supabase drei Ursachen für hohen Tokenverbrauch an: vollständige Doku-Metadaten bei jedem search_docs-Aufruf, fehlende Gesamtsicht auf den Backend-Zustand und rohe Fehlermeldungen, die Wiederholungsschleifen auslösen. Er verweist außerdem auf MCPMark V2, wonach der Supabase-MCP-Verbrauch von Sonnet 4.5 auf 4.6 von 11,6 auf 17,9 Mio. Tokens über 21 Datenbankaufgaben stieg, und auf einen Scalekit-Benchmark mit 10- bis 35-fach besserer Tokeneffizienz für CLI plus Skills; beides ist hier nur aus zweiter Hand gespeichert. [tweet-2097242863964958760](../sources/tweet-2097242863964958760.md)

## Selbst durchgeführter Vergleich (Stand 2026-09)

Der Autor baute die App DocuRAG (Google-OAuth, PDF-Upload, pgvector, GPT-4o) einmal mit [Claude Code](Claude%20Code.md) auf Supabase und einmal auf InsForge. Supabase: 10,4 Mio. Tokens, 9,21 Dollar, zwölf Nutzernachrichten (zehn Fehlermeldungen), 135 Tool-Aufrufe; ein 401-Fehler wurde in acht Versuchen auf Code-Ebene gesucht, bis die Ursache im verify_jwt-Prüfschritt der Plattform lag. InsForge: 3,7 Mio. Tokens, 2,81 Dollar, eine Nutzernachricht, keine Fehler. [tweet-2097242863964958760](../sources/tweet-2097242863964958760.md)

Einschränkungen: ein Lauf je Seite, die Prompts unterscheiden sich (Supabase plus OpenAI-API gegenüber InsForge als Gateway), die Supabase-OAuth-Einrichtung im Google-Dashboard geschah manuell, die Zählweise der Tokens ist nicht erklärt, die Auswertung machte eine weitere Claude-Instanz, und der Autor wirbt für das Projekt. [tweet-2097242863964958760](../sources/tweet-2097242863964958760.md)

## Einordnung (Stand 2026-09)

Das Beispiel stützt die These, dass Zustand und Fehlerrückmeldung eines Backends Teil des Agentenkontexts sind ([Context Engineering](../concepts/Context%20Engineering.md)). Zur Wahl zwischen MCP und CLI siehe [Model Context Protocol](../concepts/Model%20Context%20Protocol.md); Kostenbehauptungen im Überblick: [AI Coding Cost Claims](../concepts/AI%20Coding%20Cost%20Claims.md). [tweet-2097242863964958760](../sources/tweet-2097242863964958760.md)
