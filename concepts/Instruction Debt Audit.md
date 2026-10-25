---
tags: [agents, tools]
sources: [tweet-2096668098422272007.md, tweet-2097369738968195513.md, tweet-2098480213244117065.md]
created: 2026-10-03
updated: 2026-10-08
---

# Instruction Debt Audit

## Anti-Muster nach Anthropic

Der Artikel nennt für frische Modelle: Verifikationsrituale ("prüfe zweimal"), Gründlichkeits- und Betonungsverstärker ("CRITICAL: YOU MUST ALWAYS"), starre Prozeduren und Scratchpad-Gerüste, veraltete Few-Shot-Beispiele, widersprüchliche Regeln und veraltete Konfiguration wie manuelle Thinking-Budgets. Frontier-Modelle befolgten Anweisungen wörtlicher, was Kosten und Fehler erhöhe. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

Der berichtete Test: Von einem sauberen Support-Prompt wurden sechs Altversionen mit je einem eingebauten Anti-Muster erzeugt und auf Opus 4.8, Opus 5 mit nur geändertem Modell sowie Opus 5 nach `prompt-audit` laufen gelassen. Nach dem Audit sanken die Kosten im Mittel um 14,6 Prozent und die Genauigkeit stieg um 5,3 Prozent; Ursachen waren unter anderem verworfene Anfragen durch die abgeschaltete Thinking-Einstellung, zurückgehaltene Erstattungen durch widersprüchliche Regeln und ein Scratchpad, das einen Tool-Aufruf in den Reasoning-Text schrieb statt ihn auszuführen. Es ist ein Herstellertest mit konstruierten Prompts. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

## Werkzeuge

- `/claude-api prompt-audit` markiert Anweisungen, die das neue Modell nicht mehr braucht, und schlägt einen Diff vor ([Claude API Skill](../entities/Claude%20API%20Skill.md)). [tweet-2096668098422272007](../sources/tweet-2096668098422272007.md) [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

## Abgrenzung

[Skill Cleaner](../entities/Skill%20Cleaner.md) prüft das sichtbare Skill-Inventar und Beschreibungsbudget, [Jev Workspace Audit](Jev%20Workspace%20Audit.md) sucht Aufgaben für ein Modell, [Context Engineering](Context%20Engineering.md) behandelt die Auswahl von Kontext insgesamt. Bei diesen Quellen ist der Nutzen bisher nicht an eigenen Setups gemessen. [tweet-2097369738968195513](../sources/tweet-2097369738968195513.md)

## OpenAI-Perspektive auf Instruktionspflege (Stand 2026-09)

Der Astra-Leitfaden erweitert die Pflegefrage um spezifische Skill-Trigger, progressive Offenlegung und taskbezogene Referenzen. Instruktionen für ältere Modelle können laut OpenAI neue Modelle überbeschränken oder unnötige Prüfungsschleifen auslösen. [tweet-2098480213244117065](../sources/tweet-2098480213244117065.md)

Als Auditfrage schlägt der Artikel vor zu prüfen, welche AGENTS.md-Regeln noch nötig sind, wo Entscheidungsgrenzen gewünschte Arbeit stoppen und wie die tatsächliche Fertigbedingung beschrieben ist. Die Quelle ergänzt [Context Engineering](Context%20Engineering.md), ohne die Anthropic-Testwerte als Astra-Messung zu verwenden. [tweet-2098480213244117065](../sources/tweet-2098480213244117065.md)
