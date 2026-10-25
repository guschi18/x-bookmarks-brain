---
tags: [agents, tools, product-building]
sources: [tweet-2041299378967621889.md]
created: 2026-10-22
updated: 2026-10-22
---

# Pi Agent

## Minimaler Harness (Stand 2026-04)

David Ondrej beschreibt Pi Agent als erweiterbaren Coding-Harness und als Grundlage von OpenClaw. Vier eingebaute Werkzeuge bilden den Kern: Read liest Dateien, Write erzeugt sie, Edit ändert vorhandene Inhalte und Bash führt Terminalbefehle aus. Ein kleiner Systemprompt und nach Bedarf ergänzte Funktionen sind die im Tutorial vertretene Designentscheidung, kein Nachweis allgemeiner Überlegenheit. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md)

Er unterscheidet Pi-TUI für Terminaloberflächen, den Pi Coding Agent als nutzbare Anwendung, Pi Agent Core für die Werkzeug-/Agentenschleife und Pi-AI als einheitliche Modellschnittstelle. Das macht den Harness zugleich zur Anwendung und zum Baustein eigener Agentenoberflächen im [Agentic Engineering](../concepts/Agentic%20Engineering.md). [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md)

## Einrichtung und dauerhafte Vorgaben (Stand 2026-04)

Der gezeigte Einstieg führt über [pi.dev](https://pi.dev/), dessen Installationsbefehl im Video kopiert wird. Der Sprecher empfiehlt, Provider und Modell dauerhaft zu konfigurieren und den API-Schlüssel in einer Auth-Datei zu hinterlegen, statt bei jeder neuen Shell Parameter und Umgebungsvariablen erneut zu setzen. Er zeigt OpenRouter, erwähnt einen selbst gewählten Schlüssel-Creditrahmen und nutzt [Claude Code](Claude%20Code.md) zur Prüfung der Einrichtung. Der direkte Link zum erwähnten Setup-Gist und dessen vollständige JSON-Dateien fehlen in Raw. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md)

Eine globale AGENTS.md soll persönliche Regeln enthalten, projektspezifische AGENTS.md ergänzen sie. Das Transkript gibt den globalen Pfad als .py/agent/agents.md und die Auth-Datei als off.json wieder; diese unsicheren Lautschriftformen sind keine geprüften Dateipfade. Für eine tatsächliche Einrichtung müssen die aktuellen Pfade und Konfigurationsfelder separat verifiziert werden. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md)

## Themes und Erweiterungen

Das Tutorial lässt den Agenten zuerst ein Matrix-Theme, dann eine Erweiterung mit CPU-, RAM- und weiteren Systemwerten erstellen. `/reload` lädt die Änderungen innerhalb der laufenden Sitzung. Der Sprecher zeigt später die Rückkehr zur Standardoberfläche durch Deaktivieren beziehungsweise Entfernen der eigenen Anpassungen. Die Demo belegt einen Anpassungsablauf, keine unabhängige Genauigkeit der angezeigten Systemwerte. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md)

Unter [pi.dev/packages](https://pi.dev/packages) zeigt er einen Katalog für Extensions, Skills und Themes. Beispiele sind Pi Subagents für Delegation, `Task Plane` für Orchestrierung, Pi Studio sowie Pi Design Deck für die Auswahl visueller Varianten. Diese Pakete sind optionale Ergänzungen und im gespeicherten Tutorial nicht als vollständig geprüfter Gesamtstack belegt. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md)

## Sitzungen gezielt fortsetzen

| Befehl | Im Tutorial gezeigter Zweck |
| --- | --- |
| `/tree` | Zu einer früheren Nachricht wechseln und innerhalb derselben Sitzung einen Nebenpfad bearbeiten; optional mit Zusammenfassung. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md) |
| `/fork` | Von einem gewählten Gesprächsstand eine neue Sitzung ableiten. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md) |
| `pi -c` | Die zuletzt bearbeitete Sitzung fortsetzen. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md) |
| `pi -r` / `pi --resume` | Eine frühere Sitzung auswählen. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md) |
| `/reload` | Neue Themes, Erweiterungen und Einstellungen im gezeigten Ablauf laden. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md) |

Der praktische Anwendungsfall für den Sitzungsbaum ist eine Nebenaufgabe wie Debugging: vom bisherigen Verlauf abzweigen, die Nebenfrage bearbeiten und anschließend mit einer Zusammenfassung zum Hauptpfad zurückkehren. Das trennt Gesprächskontext; ein isolierter Git-Branch oder eine getrennte Laufzeitumgebung ist damit nicht belegt. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md)

## Grenzen und historischer Stand

Der Sprecher bezeichnet Pi als standardmäßig ohne Rechteabfragen und empfiehlt auch für [Claude Code](Claude%20Code.md) das Umgehen solcher Abfragen. Das ist seine Arbeitsweise, keine geprüfte Sicherheitsvorgabe. Seine pauschalen Aussagen über Schutzmechanismen anderer Agenten, Prompthöhen, Shopify-Beschleunigung und universelle Kostenvorteile sind nicht unabhängig belegt. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md)

Die Modellpräferenzen, Preise, Paketpopularität und Werbeaktionen gelten für den April-2026-Bericht und ersetzen keine aktuelle Auswahlprüfung. Das vollständige Transkript enthält praktische Bedienung, aber keinen direkt gespeicherten Setup-Gist, keine reproduzierbare Benchmark-Auswertung und keine hier durchgeführte Installation. [tweet-2041299378967621889](../sources/tweet-2041299378967621889.md)
