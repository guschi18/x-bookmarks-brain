---
tags: [security, agents, tools]
sources: [tweet-2112110254024757276.md]
created: 2026-10-23
updated: 2026-10-23
---

# OpenShell

## Überblick (Stand 2026-10)

NVIDIA/OpenShell ist laut README eine sichere, private Laufzeit für Flotten autonomer KI-Agents. Man legt in einer Policy fest, worauf jeder Agent zugreifen darf; OpenShell setzt sie durch, sodass Agents Dateien lesen, Pakete installieren und APIs aufrufen können, ohne uneingeschränkten Zugriff auf Daten, Geheimnisse oder Netz. [tweet-2112110254024757276](../sources/tweet-2112110254024757276.md)

## Mechanismus laut README

- Kernel-Durchsetzung: Jeder Agent läuft in einer isolierten Sandbox; Kernel-Kontrollen begrenzen Dateizugriff und Systemaufrufe, jede Netzverbindung durchläuft vorher eine Policy-Prüfung. [tweet-2112110254024757276](../sources/tweet-2112110254024757276.md)
- Agents sehen keine echten Zugangsdaten; OpenShell fügt sie nur Anfragen an freigegebene Ziele hinzu. [tweet-2112110254024757276](../sources/tweet-2112110254024757276.md)
- Formal verifizierte Policy-Änderungen: Vor der Freigabe markiert OpenShell riskante neue Zugriffe, etwa neue Hosts mit Zugangsdaten, damit sie auf menschliche Prüfung warten. [tweet-2112110254024757276](../sources/tweet-2112110254024757276.md)

## Einstieg

Voraussetzung sind Linux, macOS auf Apple Silicon oder Windows mit WSL 2 (experimentell) sowie Docker, Podman oder Host-Virtualisierung. Installation: curl -LsSf https://raw.githubusercontent.com/NVIDIA/OpenShell/main/install.sh | sh, dann openshell sandbox create --name demo. Lizenz: Apache 2.0. [tweet-2112110254024757276](../sources/tweet-2112110254024757276.md)

Der Post nennt 16,6K Sterne; die Zahl stammt nicht aus der README. Die Schutzwirkung ist Herstellerangabe und wurde hier nicht geprüft. Verwandt: [Claude Code Security Hardening](../concepts/Claude%20Code%20Security%20Hardening.md). [tweet-2112110254024757276](../sources/tweet-2112110254024757276.md)
