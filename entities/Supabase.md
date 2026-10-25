---
tags: [product-building, security]
sources: [tweet-2110974023299699003.md]
created: 2026-10-23
updated: 2026-10-23
---

# Supabase

## Überblick (Stand 2026-10)

Supabase ist ein quelloffenes Backend auf Postgres, das sich laut Gründerbericht als „open source Firebase alternative“ positioniert. Der CTO und Mitgründer („Ant“ im Transkript) sagt im Interview mit David Ondrej, der frühere Slogan „real time Postgres database“ sei nicht verstanden worden; erst der Wechsel zur Firebase-Alternative habe Entwickler überzeugt. Er rät, die eigene Botschaft zu iterieren, bis sie präzise ist. [tweet-2110974023299699003](../sources/tweet-2110974023299699003.md)

## Agenten als Nutzer (Stand 2026-10)

Der Gast beschreibt Agenten als „elite level software engineers“. Anfangs hätten Modelle Bilddaten in Postgres statt in den Storage gelegt und für schnelle Ergebnisse RLS abgeschaltet; das habe sich zuletzt deutlich gebessert. Supabase pflegt Evals, die messen, ob ein Agent das Produkt nach der Wahl erfolgreich nutzt; Modellanbieter nutzten sie laut Gast zur Verbesserung. [tweet-2110974023299699003](../sources/tweet-2110974023299699003.md)

Preislogik und Produkte ändern sich für Agenten: Statt weniger großer Gratisdatenbanken soll jeder Prompt eine eigene Datenbank bekommen können. Supabase Lite deckt den schnellen Start ab, bei Wachstum wird ohne Ausfall in eine dedizierte Postgres-Instanz migriert; für sehr große Last nennt er Multigres, eine skalierbare Postgres-Variante. Weitere Ankündigungen verweist er auf Supabase Select. [tweet-2110974023299699003](../sources/tweet-2110974023299699003.md)

Headless: Was das Dashboard kann, solle auch über API, MCP-Server und CLI laufen. Für ein neues Infrastrukturprodukt würde der Gast auf ein Dashboard verzichten. Einordnung in [Agent-First Product Design](../concepts/Agent-First%20Product%20Design.md). [tweet-2110974023299699003](../sources/tweet-2110974023299699003.md)

## Sicherheit mit Agenten (Stand 2026-10)

Offener Quellcode ist für den Gast ein Sicherheitsargument, weil Fehler früher auffallen, wenn viele den Code lesen und Agenten Systeme prüfen. Für Agentenzugriff nennt er Read Replicas und Datenbank-Branching, für Anfänger eine einfache Sicherheitsprüfung des Projekts vor dem Produktivgang, am besten als Regel bei jedem Merge nach main. Details und Grenzen: [Claude Code Security Hardening](../concepts/Claude%20Code%20Security%20Hardening.md). [tweet-2110974023299699003](../sources/tweet-2110974023299699003.md)

## Arbeitsweise und Organisation (Stand 2026-10)

Supabase ist laut Gast vollständig remote und schriftlich organisiert (Slack, Notion, Linear), mit Mitarbeitenden in 64 Ländern. Er nennt als Vorteil, dass Agenten diese Historie durchsuchen können, und stellt Mitarbeitende aus der Open-Source-Community ein, weil sie asynchron arbeiten. Er arbeitet bevorzugt in der Cloud mit [Claude Opus 5.5](Claude%20Opus%205.5.md) und wechselt bei erreichtem Limit zu [Codex](Codex.md). [tweet-2110974023299699003](../sources/tweet-2110974023299699003.md)

## Evidenzgrenzen

Alle Zahlen und Selbstbeschreibungen stammen vom Gast und sind Herstellerangaben: der Bewertungswert über 10 Milliarden Dollar kommt vom Interviewer, die Angabe, 60 Prozent der jüngsten YC-Batch seien auf Supabase gebaut, vom Gast. Das Transkript ist automatisch erzeugt und enthält einen Sponsor-Spot und Eigenwerbung des Interviewers, die hier nicht ausgewertet sind. Zum Vergleich mit einem anderen agentenorientierten Backend siehe [InsForge](InsForge.md). [tweet-2110974023299699003](../sources/tweet-2110974023299699003.md)
