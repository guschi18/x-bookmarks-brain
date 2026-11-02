---
tags: [security, llm-training]
sources: [tweet-2115215878220558547.md]
created: 2026-11-01
updated: 2026-11-01
---

# Hinoki Offensive One

## Überblick (Stand 2026-10)

Hinoki Offensive One (HO1) ist ein LLM für Pentesting und Exploit-Entwicklung der Firma Hinoki (San Francisco). Johnny Wang schreibt, das Team habe 150.000 CVE-Exploits geschrieben und das Modell darauf trainiert; es erreiche 88,4 % auf CyberGym, 2,8 Punkte über "Daybreak", mit null Verweigerungen, und sei sofort verfügbar. [tweet-2115215878220558547](../sources/tweet-2115215878220558547.md)

## Herstellerseite (Abruf 2026-11-01)

Die Seite [hinoki.security](https://hinoki.security/) nennt HO1 "the first open-access cyber model", offen für alle per Anmeldung, mit Integrationen für Claude Code, Codex, OpenCode, VS Code und Cursor. Sie behauptet, HO1 löse Aufgaben, die andere Modelle verweigern, und zeigt ein einzelnes Demo-Transkript (6 Züge gegen eine Verweigerung). Als Benchmark nennt sie ebenfalls 88,4 % auf CyberGym, aber 2,8 Punkte über GPT-5.5-Cyber; die Rangliste war im abgerufenen Text nicht lesbar (alle Werte 0,0 %). Die vollständige Recherche mit Fundstellen steht in `output/hinoki-research-2026-11-01.md`. [tweet-2115215878220558547](../sources/tweet-2115215878220558547.md)

## Widersprüche und Lücken

Der Tweet nennt "Daybreak" als Vergleichsmodell, die Website GPT-5.5-Cyber; ob das dasselbe meint, ist offen. Die Zahl 150.000 und das Training auf Exploits stehen nur im Tweet, nicht auf der Seite. Preis, Basismodell, Lizenz, Team und der Umgang mit Missbrauch sind nicht dokumentiert. [tweet-2115215878220558547](../sources/tweet-2115215878220558547.md)

## Evidenzgrenze

Alle Zahlen sind Herstellerangaben; weder CyberGym-Ergebnis noch "zero refusals" sind unabhängig bestätigt, das Modell wurde nicht getestet. Als Marktbeobachtung relevant: ein offen zugängliches Offensiv-Modell, das Verteidiger mitdenken sollten. Verwandt: [Strix](Strix.md) (KI-Pentest-Agenten) und [Cloudflare Security Audit Skill](Cloudflare%20Security%20Audit%20Skill.md). [tweet-2115215878220558547](../sources/tweet-2115215878220558547.md)
