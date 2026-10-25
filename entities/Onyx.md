---
tags: [tools, agents, research]
sources: [tweet-2039598698548850949.md]
created: 2026-10-22
updated: 2026-10-22
---

# Onyx

## Zuordnung und Quelle

Der Post von Avi Chawla bewirbt im April 2026 eine nicht namentlich genannte Open-Source-Alternative zu Claude. Der Nutzer hat das Repository [onyx-dot-app/onyx](https://github.com/onyx-dot-app/onyx) am 2026-10-22 als gemeinte Quelle genannt; im Post steht der Name nicht. [tweet-2039598698548850949](../sources/tweet-2039598698548850949.md)

## Was das Projekt ist (Stand 2026-10)

Die README beschreibt Onyx als Wissens- und Kontextschicht für Teams und KI-Agenten: Es bindet über 50 Anwendungen an, indexiert deren Inhalte samt Metadaten und Rechten und bietet Chat, Agenten, Deep Research, Websuche, externe Aktionen über [Model Context Protocol](../concepts/Model%20Context%20Protocol.md), eine Code-Sandbox, Artefakte und Sprachmodus. [tweet-2039598698548850949](../sources/tweet-2039598698548850949.md) Es unterstützt Modelle von Anbietern wie Anthropic, OpenAI und Gemini sowie selbst gehostete über Ollama, LiteLLM oder vLLM. [tweet-2039598698548850949](../sources/tweet-2039598698548850949.md) Zugriff besteht über Web- und Desktop-App, Slack- und Discord-Bot, MCP-Server (für [Claude Code](Claude%20Code.md), Codex und andere Clients), Chrome-Erweiterung und eingebettetes Widget. [tweet-2039598698548850949](../sources/tweet-2039598698548850949.md)

Die README begründet den Index-Ansatz damit, dass ein Agent, der viele MCP-Server iterativ abfragt, mehr Token verbrauche als ein vorab aufgebauter Index mit Berechtigungen. Das ist eine Herstellerbehauptung ohne gemessenen Vergleich. [tweet-2039598698548850949](../sources/tweet-2039598698548850949.md)

## Betrieb und Lizenz

Das Repository nennt zwei Modi: Standard (Vektor- und Stichwortindex, Hintergrund-Worker für Konnektoren, Modellserver, Redis, MinIO) und Lite (unter 1 GB Speicher, nur Chat und Agenten, keine Dokumentindexierung). Als Installation nennt die README einen Ein-Befehl-Installer; Docker, Kubernetes, Helm und Terraform liegen im Verzeichnis deployment. Hier wurde nichts installiert oder ausgeführt. [tweet-2039598698548850949](../sources/tweet-2039598698548850949.md)

Die Community Edition steht laut README unter MIT. Die LICENSE-Datei schränkt das ein: Inhalte in ee-Verzeichnissen unterliegen der Onyx Enterprise License; GitHub zeigt die Lizenz deshalb als Other. Enterprise-Funktionen wie SSO per SAML/OIDC, SCIM, rollenbasierte Rechte, Analysen und Whitelabeling gehören zur Enterprise Edition. [tweet-2039598698548850949](../sources/tweet-2039598698548850949.md)

## Stand der Prüfung am 2026-10-22

GitHub-Metadaten am Prüftag: Hauptzweig-Commit a4ed03e6717c85b3d9d4e22196dbc4166e7b965e vom 2026-10-22, Release v4.9.2 vom 2026-10-15, rund 32.800 Sterne, rund 4.600 Forks, Python als Hauptsprache, Repository seit 2023-04 (Copyright-Inhaber laut LICENSE: DanswerAI, Inc.). Der Post nannte im April über 20.000 Sterne und 40+ Datenquellen; die README nennt jetzt über 50 Anwendungen. Das sind verschiedene Zeitstände, kein Widerspruch. [tweet-2039598698548850949](../sources/tweet-2039598698548850949.md)

## Evidenzgrenzen

Die Behauptungen im Post, Onyx sei besser als Claude und schlage es bei Deep Research, sind nicht belegt; die README spricht nur von bester Such- und Antwortqualität ohne Benchmark. Das gespeicherte Video hat kein Transkript. Es wurde weder ausgeführt noch getestet noch sicherheitsgeprüft. Verwandte selbst gehostete Chat-Oberfläche: [LibreChat](LibreChat.md). [tweet-2039598698548850949](../sources/tweet-2039598698548850949.md)
