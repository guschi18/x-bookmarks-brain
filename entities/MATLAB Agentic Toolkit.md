---
tags: [agents, tools]
sources: [tweet-2051612619086135802.md]
created: 2026-10-15
updated: 2026-10-15
---

# MATLAB Agentic Toolkit

## Zweck und Bausteine (Stand 2026-05)

Das [MathWorks-Repository](https://github.com/matlab/matlab-agentic-toolkit) bündelt laut gespeichertem Herstellerartikel den MATLAB MCP Core Server und Agent Skills für MATLAB-Arbeit. Der Server verbindet einen Coding-Agenten wie [Claude Code](Claude%20Code.md) mit der lokal installierten MATLAB-Instanz; die Skills geben Fachkontext und Arbeitsanweisungen. Das Toolkit vereinfacht nach Herstellerangabe Installation, Konfiguration und Updates dieser zuvor getrennten Bausteine. [tweet-2051612619086135802](../sources/tweet-2051612619086135802.md)

## Einrichtung (Stand 2026-05)

Der Artikel verlangt MATLAB R2020b oder neuer, Git und einen unterstützten Coding-Agenten. Er nennt sechs Plattformen, darunter Claude Code, GitHub Copilot, [Codex](Codex.md) und Gemini CLI; einzelne Skills wie reine Text-Live-Scripts benötigen neuere MATLAB-Versionen. [tweet-2051612619086135802](../sources/tweet-2051612619086135802.md)

Für das Claude-Code-Beispiel wird das Repository geklont, Claude im Repository-Root gestartet und mit „set up the toolkit“ zur Einrichtung aufgefordert. Der Setup-Skill soll MATLAB finden, den MCP-Server installieren, das Plugin registrieren und die Umgebung prüfen. Nach einer neuen Claude-Code-Sitzung sollen Tools und Skills auch in anderen Projektordnern verfügbar sein. [tweet-2051612619086135802](../sources/tweet-2051612619086135802.md)

```sh
git clone https://github.com/matlab/matlab-agentic-toolkit.git
cd matlab-agentic-toolkit
claude
```

Als Zugriffskontrolle schlägt der Autor vor, nach Toolkit-Zugang, MATLAB-Version und installierten Toolboxes zu fragen. Das gespeicherte Originalbild zeigt eine solche Antwort mit Tools, Skills und Ressourcen; es ist kein lokaler Funktionstest dieses Wikis. [tweet-2051612619086135802](../sources/tweet-2051612619086135802.md)

## Werkzeuge und Arbeitsablauf (Stand 2026-05)

Der Artikel nennt evaluate_matlab_code, run_matlab_file, run_matlab_test_file, check_matlab_code und detect_matlab_toolboxes für Ausführung, Tests, statische Analyse und Umgebungserkennung. MCP-Ressourcen liefern MATLAB-Coding-Guidelines und Regeln für Text-Live-Scripts. [tweet-2051612619086135802](../sources/tweet-2051612619086135802.md)

Die Skills decken Tests mit matlab.unittest, Live Scripts ab R2025a, programmatische Apps, Code-Review, Debugging und Modernisierung ab. In einem Beispiel verwendet Claude bei einer Modernisierungsaufgabe die Analyse und Guidelines automatisch; den Modernisierungs-Skill musste der Autor zusätzlich anfordern. Der Artikel behauptet daher keine verlässliche automatische Auswahl jedes passenden Skills. [tweet-2051612619086135802](../sources/tweet-2051612619086135802.md)

## Grenzen und Quellenstand (Stand 2026-05)

Der kurze Post wird durch einen vollständigen Herstellerartikel und neun strukturierte Links ergänzt. Der Autor bezeichnet die Skill-Entwicklung als laufend und die Qualität als unterschiedlich; aktuelle Kataloge und Aufrufnamen können sich ändern. Weder Installation noch Codeausführung oder behauptete Qualitätsverbesserungen wurden hier geprüft. [tweet-2051612619086135802](../sources/tweet-2051612619086135802.md)
