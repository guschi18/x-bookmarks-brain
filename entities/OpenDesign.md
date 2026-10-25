---
tags: [tools, product-building, agents]
sources: [tweet-2049145798768668746.md]
created: 2026-10-16
updated: 2026-10-16
---

# OpenDesign

## Historischer Start (Stand 2026-04)

Tom Huang beschreibt [nexu-io/open-design](https://github.com/nexu-io/open-design) als offene Alternative zu [Claude Design](Claude%20Design.md) und kündigt Bild-, Video- und Audio/Musik-Unterstützung an. Die zitierten über 30 Skills, über 71 Designsysteme und mehr als 95 Prozent Nachbildungsnähe sind damalige Anbieterangaben ohne unabhängige Messung. [tweet-2049145798768668746](../sources/tweet-2049145798768668746.md)

## Arbeitsablauf (separater gespeicherter README-Stand)

Die spätere README beschreibt eine lokale Desktop-/Weboberfläche: Briefing und Gestaltungsrichtung festlegen, DESIGN.md als Markenvertrag wählen, einen Skill oder eine Vorlage mit dem Agenten kombinieren, echte Projektdateien erzeugen und im Studio prüfen. Unterstützte Artefakte umfassen Prototypen, Decks, Dokumente, Bilder und [HyperFrames](HyperFrames.md)-Videos. Dieser spätere Umfang belegt nicht die vollständige Verfügbarkeit im April. [tweet-2049145798768668746](../sources/tweet-2049145798768668746.md)

Das System verbindet vorhandene Coding-Agenten per CLI-Adaptern oder BYOK-Endpunkte. Dateisystemfähige Agenten schreiben kanonische Projektdateien; einfache API-Pfade liefern einen Artefaktblock. MCP stellt Projektdateien, Tokens und Komponenten zur weiteren Bearbeitung bereit, statt bei jeder Änderung ZIP-Dateien neu anzuhängen. [tweet-2049145798768668746](../sources/tweet-2049145798768668746.md)

## Wiederverwendung und Übergabe

Die README trennt funktionale Skills, Rendering-Vorlagen, DESIGN.md-Designsysteme und Plugins. Bestehende Repositories können mit einem Designsystem überarbeitet werden; HTML, PDF, PPTX, ZIP und MP4 sind dokumentierte Ausgabewege. Die verschiedenen Katalogzähler und Roadmapstände werden nicht zu einem einheitlichen historischen Release zusammengezogen. [tweet-2049145798768668746](../sources/tweet-2049145798768668746.md)

## Voraussetzungen und Grenzen

Der gespeicherte Stand nennt Desktop-Pakete für macOS/Windows, Quellbetrieb und Docker sowie modellabhängige Zugangsdaten. Lokal gespeicherte Dateien bedeuten keine vollständig lokale Modellverarbeitung: BYOK-Modelle können externe Dienste nutzen. Die README beschreibt außerdem stets aktive bereinigte Sicherheits-/Zuverlässigkeitstelemetrie neben zustimmungsabhängigen Produktanalysen. [tweet-2049145798768668746](../sources/tweet-2049145798768668746.md)

Standardmäßig bindet der Daemon laut README an Loopback; öffentliche oder gemeinsame Bereitstellung verlangt gesonderte Authentifizierungs-/Origin-Konfiguration. Die Demo wurde visuell stichprobenartig geprüft, nicht installiert oder auf Exportqualität getestet; die erneute Transkription lieferte keinen gesprochenen Text. Das Projekt ergänzt [Design Skills for Coding Agents](../concepts/Design%20Skills%20for%20Coding%20Agents.md) um eine zusammenhängende Oberfläche. [tweet-2049145798768668746](../sources/tweet-2049145798768668746.md)
