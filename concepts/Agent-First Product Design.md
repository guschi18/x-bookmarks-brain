---
tags: [agents, product-building]
sources: [tweet-2064754331715346658.md, tweet-2062546475888845157.md, tweet-2057924890330644925.md, tweet-2104688418659987802.md, tweet-2089844723691479333.md, tweet-2052422567181611010.md, tweet-2110974023299699003.md]
created: 2026-09-29
updated: 2026-10-23
---

# Agent-First Product Design

## Begriff im Interview

[Agent-First Product Design](Agent-First%20Product%20Design.md) bezeichnet hier die Produktidee des MagicPath-Gründers: Ein Dienst soll für Coding-Agenten über einfache Schnittstellen und passenden Kontext erreichbar sein, während Menschen Ergebnisse prüfen und Richtung vorgeben. Er nennt [MagicPath](../entities/MagicPath.md) als Beispiel und zeigt eine Interaktion mit [Codex](../entities/Codex.md). [tweet-2064754331715346658](../sources/tweet-2064754331715346658.md)

## Schritte und Grenzen

Der Gast schlägt vor, zuerst das Nutzerproblem zu wählen, dann nötige Daten und Fachkontext bereitzustellen und schließlich einen einfachen Agentenzugang zu bauen. Er empfiehlt kurze Produktdemos und frühes Nutzerfeedback; das sind seine Erfahrungsregeln, keine nachgewiesene allgemeine Methode. [tweet-2064754331715346658](../sources/tweet-2064754331715346658.md)

Seine Vorhersagen über das Ende klassischer Softwareoberflächen und proaktive Agenten sind Spekulation. Im gespeicherten Gespräch wird weder die Übertragbarkeit auf andere Produkte noch eine Wirtschaftlichkeit gemessen. [tweet-2064754331715346658](../sources/tweet-2064754331715346658.md)

## Ergänzungen (Stand 2026-06)

Das vollständige Gespräch konkretisiert drei Fragen: Welches Problem wird gelöst, welchen Fach- und Dokumentkontext braucht das Modell und wie erhält der bestehende Agent möglichst einfach Zugang? [MagicPath](../entities/MagicPath.md) wird als Code-basierter Canvas für [Codex](../entities/Codex.md) und andere Agents vorgeführt; der Mensch soll Ergebnisse beaufsichtigen. [tweet-2062546475888845157](../sources/tweet-2062546475888845157.md)

Der Gründer empfiehlt eine klar erzählte kurze Demo, frühe Beta-Nutzer und Konzentration auf eine gut verständliche Funktion. Seine Prognose einer künftigen Codex-Schnittstelle für Browserereignisse sowie das Ende klassischer Oberflächen sind Zukunftserwartungen, keine in der Quelle nachgewiesenen Produktfunktionen. [tweet-2062546475888845157](../sources/tweet-2062546475888845157.md)

## Agentenlesbare Infrastruktur (Stand 2026-05)

Karpathy fordert im Interview Dokumentation und Infrastruktur, deren konkrete Anweisung direkt an einen Agenten übergeben werden kann. Er beschreibt Sensoren und Aktuatoren über die Welt sowie für LLMs lesbare Datenstrukturen; MenuGen-Deployment mit mehreren Diensten und DNS nennt er als bisher mühsames Gegenbeispiel. [tweet-2057924890330644925](../sources/tweet-2057924890330644925.md)

Die Idee ergänzt [Software 3.0](Software%203.0.md): Kontext soll nicht nur Codegenerierung beschleunigen, sondern einen ganzen Aufbau- und Bereitstellungsweg zugänglich machen. Agenten, die künftig für Personen oder Organisationen miteinander sprechen, sind seine Prognose, kein im Interview getestetes Gesamtsystem. [tweet-2057924890330644925](../sources/tweet-2057924890330644925.md)

## Verifizierbare Agenten-Workflows (Stand 2026-09)

Der gespeicherte AX-Artikel entwirft eine Kette aus Discovery, Kontext, Validierung, Ausführung und strukturiertem Ergebnisbeleg. Tools sollen bestehende Geschäftslogik und Rechte wiederverwenden und stabile IDs, explizite Zustände sowie prüfbare Datensätze oder Job-IDs zurückgeben. [tweet-2104688418659987802](../sources/tweet-2104688418659987802.md)

Fehler unterscheiden Mehrdeutigkeit, falsche Eingabe, verweigerten Zugriff und unterbrochene Arbeit. Idempotenzschlüssel sollen doppelte Writes bei Wiederholung vermeiden; asynchrone Jobs brauchen prüfbare Zustände. Freigabe gilt für eine konkrete Aktion und Version und wird im Backend durchgesetzt. [tweet-2104688418659987802](../sources/tweet-2104688418659987802.md)

Ein begrenzter Testworkspace prüft Discovery, Ausführung und Erholung bei festen Aufgaben, Daten, Rechten und Modellsettings. Monitoring soll Completion erst nach Ergebnisprüfung melden und erfolgreiche Aufgaben, Fehler, doppelte Writes sowie unerlaubte Änderungen unterscheiden. Viktor, PostHog und Whop sind vorgeschlagene Dienste, deren Geschäftswirkung hier nicht belegt ist. [tweet-2104688418659987802](../sources/tweet-2104688418659987802.md)

## SaaS als Agentendienst (Stand 2026-08)

Thariq schlägt vor, einen bestehenden SaaS headless zugänglich zu machen, Agenten seine Funktionen nutzen zu lassen und pro Interaktion abzurechnen, besonders für Enterprise-Kunden. Das ergänzt den Schnittstellengedanken um eine konkrete Preishypothese; Umsetzung, Nachfrage und Erlöse werden im Post nicht belegt. [tweet-2089844723691479333](../sources/tweet-2089844723691479333.md)

## CLI-Fabrik und lokale Abfragespiegel (Stand 2026-05)

[Printing Press](../entities/Printing%20Press.md) konkretisiert Agentenzugang durch generierte Go-CLIs, passende Skills und MCP-Ausgaben. Der Anbieter kombiniert lokale SQLite-Spiegel mit zusammengesetzten Abfragen, damit ein Agent etwa blockierte Linear-Issues samt alten Blockern in einem Schritt abfragen kann. Das ist ein dokumentiertes Werkzeugmuster, kein gemessener Nachweis allgemeiner Token- oder Kostenersparnis. [tweet-2052422567181611010](../sources/tweet-2052422567181611010.md)

## Headless und Agenten-Evals bei Supabase (Stand 2026-10)

Im Interview sagt der Supabase-CTO, was für Entwickler gut sei, sei auch für Agenten gut: Zuverlässigkeit, Sicherheit und Geschwindigkeit entscheiden, weil Agenten Produkte nach diesen Merkmalen auswählen. Supabase misst per Evals, ob ein Agent das Produkt nach der Wahl auch erfolgreich nutzt; einige Modellanbieter nutzten diese Evals laut dem Gast, um die Nutzung zu verbessern. [tweet-2110974023299699003](../sources/tweet-2110974023299699003.md)

Alles, was das Dashboard kann, solle auch über API, MCP-Server und CLI gehen („headless“). Für ein neues Infrastrukturprodukt würde er sogar auf ein Dashboard verzichten und die Visualisierung über die Agentenoberfläche anbieten. Das ist eine Aussage des Gasts, kein getesteter Ansatz. Für die Preisfrage nennt er eine Datenbank pro Prompt, die nach Wachstum im Hintergrund in eine dedizierte Postgres-Instanz migriert wird. Siehe [Supabase](../entities/Supabase.md). [tweet-2110974023299699003](../sources/tweet-2110974023299699003.md)
