---
tags: [agents, tools, research]
sources: [tweet-2043264109076947222.md, tweet-2040705762406895940.md]
created: 2026-10-21
updated: 2026-10-21
---

# Claude Code Best Practice

## Ressource und Herkunft

[shanraisshan/claude-code-best-practice](https://github.com/shanraisshan/claude-code-best-practice/blob/d681c9642495b161648d01b41170a6a1b0d99894/README.md) ist eine separat auf Nutzerwunsch untersuchte Lern- und Referenzsammlung zu [Claude Code](Claude%20Code.md). Die README empfiehlt, das Repository als Kurs zu lesen und Bausteine für den eigenen Ablauf auszuwählen. Der April-Post nennt 84 Tipps; im geprüften Commit vom 21.10.2026 stehen 83. Diese unterschiedlichen Stände werden nicht vereinheitlicht. [tweet-2043264109076947222](../sources/tweet-2043264109076947222.md)

Die Zuordnung zum Bookmark ist begrenzt: Sein Kurzlink führt zu X-Post 2043199144429531433 von sukh_saroy; dessen Inhalt war nicht auslesbar. Inhaltliche Übereinstimmung macht das untersuchte Repo plausibel, ersetzt aber keinen direkten Linknachweis. Seine Dokumentation wird deshalb als datierter Nachtrag geführt. [tweet-2043264109076947222](../sources/tweet-2043264109076947222.md)

## Was sich gezielt lesen lässt (Nachrecherche 2026-10-21)

Die README verknüpft Grundlagen, konkrete Implementierungen, quellverlinkte Praxistipps, Vergleiche von Entwicklungsabläufen und Themenreports. Für den Einstieg eignen sich der [Agents-/Commands-/Skills-Vergleich](https://github.com/shanraisshan/claude-code-best-practice/blob/d681c9642495b161648d01b41170a6a1b0d99894/reports/claude-agent-command-skill.md), der [Memory-Leitfaden](https://github.com/shanraisshan/claude-code-best-practice/blob/d681c9642495b161648d01b41170a6a1b0d99894/best-practice/claude-memory.md), der [Settings-Report](https://github.com/shanraisshan/claude-code-best-practice/blob/d681c9642495b161648d01b41170a6a1b0d99894/reports/claude-global-vs-project-settings.md) und das vollständige [Wetterbeispiel](https://github.com/shanraisshan/claude-code-best-practice/blob/d681c9642495b161648d01b41170a6a1b0d99894/orchestration-workflow/orchestration-workflow.md). [tweet-2043264109076947222](../sources/tweet-2043264109076947222.md)

Der Vergleich ordnet Commands einem expliziten Einstieg im Hauptkontext zu, Agents eigenem Kontext und begrenzten Werkzeugen, Skills wiederverwendbarem Wissen beziehungsweise aufrufbaren Verfahren. Die README empfiehlt bei Skills Trigger-Beschreibungen, zusätzliche Referenzen und Skripte sowie eine mit echten Fehlerfällen wachsende Gotchas-Sektion. Das sind Gestaltungsempfehlungen des Repos, keine bewiesenen universellen Regeln. [tweet-2043264109076947222](../sources/tweet-2043264109076947222.md)

Der Memory-Leitfaden unterscheidet beim Start geladene Anweisungen oberhalb des Arbeitsordners von erst bei Dateizugriff geladenen Anweisungen unterhalb. Der Settings-Report trennt persönliche Zustände von gemeinsam nutzbarer Projektkonfiguration. Beide helfen beim Strukturieren von [Context Engineering](../concepts/Context%20Engineering.md); Vorrangregeln sollten vor Konfigurationsänderungen an der aktuellen Herstellerdokumentation geprüft werden. [tweet-2043264109076947222](../sources/tweet-2043264109076947222.md)

## Konkretes Command-Agent-Skill-Beispiel

Der [weather-orchestrator](https://github.com/shanraisshan/claude-code-best-practice/blob/d681c9642495b161648d01b41170a6a1b0d99894/.claude/commands/weather-orchestrator.md) fragt Celsius oder Fahrenheit ab, delegiert den Temperaturabruf und ruft danach einen SVG-Skill auf. Der Fetcher benutzt Open-Meteo für Dubai; als Ergebnisse nennt das Repo weather.svg und output.md. Der Command verlangt eine numerische Temperatur samt Einheit, bevor der Render-Schritt starten darf. Das ist ein nachvollziehbares Datenübergabe- und Fehlerabbruchmuster. [tweet-2043264109076947222](../sources/tweet-2043264109076947222.md)

Eine wichtige Inkonsistenz bleibt: Die Workflow-Erklärung beschreibt weather-fetcher als vorgeladenes Wissen ohne dynamischen Skill-Aufruf; die aktuelle [Agent-Datei](https://github.com/shanraisshan/claude-code-best-practice/blob/d681c9642495b161648d01b41170a6a1b0d99894/.claude/agents/weather-agent.md) verlangt ausdrücklich Skill(weather-fetcher) und verbietet direkten Netzwerkzugriff. Der Agent enthält außerdem Hooks und Projekt-Memory. Die Dokumentation wurde gelesen, das Verhalten nicht ausgeführt oder bestätigt. [tweet-2043264109076947222](../sources/tweet-2043264109076947222.md)

## Praktische Auswahl und Evidenzgrenzen

Für eigene [Agentic Engineering](../concepts/Agentic%20Engineering.md)-Abläufe lässt sich das Wetterbeispiel als kleine Vorlage für Eingangsdaten, Delegation, Rückgabeprüfung und Artefakt-Erzeugung lesen; anschließend sollten nur passende Tipps und Settings übernommen werden. Der README-Stand mischt zeitabhängige CLI-Funktionen, Erfahrungswerte und widersprechende Kontextschwellen. Eine belegte Verbesserung um den im Tweet behaupteten Faktor 100 fehlt. [tweet-2043264109076947222](../sources/tweet-2043264109076947222.md)

## Ergänzung: ECC als installierbarer Workflow (Nachrecherche 2026-10-21)

[Everything Claude Code](Everything%20Claude%20Code.md) ergänzt die Lernsammlung um dokumentierte Installationswege, selektive Skills und Regeln, Hooks, Review-Schritte und einen gemeinsamen Memory Vault. Sein separat geprüfter Stand 2.2.3 ist von historischen Tweet-Zahlen zu trennen; insbesondere natives Windows hat laut README Einschränkungen. Die Verbindung ist eine Auswahlhilfe, keine Aufforderung zur Vollinstallation beider Repos. [tweet-2040705762406895940](../sources/tweet-2040705762406895940.md)
