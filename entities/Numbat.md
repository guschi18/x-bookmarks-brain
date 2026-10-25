---
tags: [agents, security]
sources: [tweet-2082511900580196596.md]
created: 2026-10-02
updated: 2026-10-02
---

# Numbat

## Überblick (Stand 2026-07)

Numbat ist Perplexitys Open-Source-Sicherheitssuite (github.com/perplexityai/numbat), die gefährliche Aktivität von KI-Agenten auf Client-Endpunkten erkennen, untersuchen und verhindern soll. Sie integriert sich in verbreitete Client-Harnesses für Coding-Agenten und bietet dafür eine einheitliche Oberfläche, sodass Sicherheitsteams nicht für jeden Agenten eigene Schutzmaßnahmen bauen müssen. [tweet-2082511900580196596](../sources/tweet-2082511900580196596.md)

## Motivation (Stand 2026-07)

Der Artikel verschiebt den Fokus von Prompt Injection auf Vorfälle ohne Angreifer: Ein Agent, der ein übergeordnetes Ziel verfolgt, wählt einen Weg, den der Nutzer nicht beabsichtigt hätte. Solche Verhaltensweisen ließen sich nicht vollständig im Modell beheben, deshalb müsse die Abwehr im umgebenden System liegen, einschließlich des Harness. Verschärfend wirken laut Artikel stundenlange autonome Läufe und Flags wie --dangerously-skip-permissions oder --yolo. [tweet-2082511900580196596](../sources/tweet-2082511900580196596.md)

## Funktionsweise (Stand 2026-07)

Numbat erkennt installierte Harnesses, setzt Sicherheitsregeln durch, kann ausgewählte Aktionen vor der Ausführung blockieren und unterstützt Erkennung und Reaktion mit Local-first-Ansatz und agentenunabhängiger Forensik. [tweet-2082511900580196596](../sources/tweet-2082511900580196596.md)

## Einsatz und Grenzen (Stand 2026-07)

Perplexity berichtet von Erfahrungen aus Einsätzen auf tausenden eigenen Endpunkten und stellt Numbat über die Open Secure AI Alliance mit NVIDIA bereit. Wirksamkeitszahlen sind Herstellerangaben. Ein anderes Sicherheitswerkzeug im Wiki ist [Deepsec](Deepsec.md). [tweet-2082511900580196596](../sources/tweet-2082511900580196596.md)
