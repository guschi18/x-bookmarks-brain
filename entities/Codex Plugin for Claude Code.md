---
tags: [agents, tools]
sources: [tweet-2050565218049376471.md]
created: 2026-10-16
updated: 2026-10-16
---

# Codex Plugin for Claude Code

## Zweck und Laufzeit (Stand 2026-05)

Das offizielle [Repository openai/codex-plugin-cc](https://github.com/openai/codex-plugin-cc) stellt [Codex](Codex.md) innerhalb von [Claude Code](Claude%20Code.md) für Reviews und delegierte Aufgaben bereit. Laut gespeicherter README nutzt es den lokalen Codex CLI und App Server mit derselben Anmeldung, Konfiguration und demselben Repository. Es ist kein separat gehosteter Codex-Lauf. [tweet-2050565218049376471](../sources/tweet-2050565218049376471.md)

## Gespeicherter Installationsweg (Stand 2026-05)

Die README verlangt Node.js 18.18 oder neuer und eine Codex-Anmeldung über ChatGPT beziehungsweise einen API-Key; Nutzung zählt zum jeweiligen Codex-Kontingent. Der gespeicherte Einstieg lautet: [tweet-2050565218049376471](../sources/tweet-2050565218049376471.md)

```text
/plugin marketplace add openai/codex-plugin-cc
/plugin install codex@openai-codex
/codex:setup
```

Fehlt Codex, kann Setup laut README eine Installation anbieten; als manueller Weg steht dort `npm install -g @openai/codex`. Modell und Reasoning-Effort werden aus der Codex-Konfiguration übernommen; Projektwerte setzen ein vertrauenswürdiges Projekt voraus. Diese Anleitung wurde hier nicht ausgeführt. [tweet-2050565218049376471](../sources/tweet-2050565218049376471.md)

## Befehle und Auswahl (Stand 2026-05)

`/codex:review` prüft uncommittete Änderungen oder mit `--base main` einen Branch und ist ausschließlich lesend. Eigener Fokus-Text gehört laut README zu `/codex:adversarial-review`, das Entscheidungen, Trade-offs, Ausfallfälle und Alternativen hinterfragt, ebenfalls ohne Code zu ändern. Beide unterstützen `--background` und `--wait`. [tweet-2050565218049376471](../sources/tweet-2050565218049376471.md)

`/codex:rescue` delegiert Untersuchung oder Änderungen; `--resume` setzt einen bisherigen Lauf fort, `--fresh` startet neu. `/codex:status`, `/codex:result` und `/codex:cancel` verwalten Hintergrundjobs. Anders als die Review-Befehle darf ein Rescue-Auftrag Änderungen ausführen. [tweet-2050565218049376471](../sources/tweet-2050565218049376471.md)

`/codex:transfer` importiert den Gesprächskontext in einen persistenten Codex-Thread und liefert einen Resume-Befehl. Laut README muss eine manuell gewählte Quelle unter `~/.claude/projects` liegen; ältere Codex-Versionen ohne Session-Import müssen aktualisiert werden. [tweet-2050565218049376471](../sources/tweet-2050565218049376471.md)

## Optionales Review-Gate und Grenzen (Stand 2026-05)

`/codex:setup --enable-review-gate` aktiviert einen Stop-Hook, der einen gezielten Codex-Review auslöst und bei Findings den Abschluss blockiert; `--disable-review-gate` deaktiviert ihn. Das Gate ist optional, entgegen dem verkürzten Eindruck eines immer automatischen Reviews im Begleitpost. Die README warnt vor langen Claude-/Codex-Schleifen und schnellem Kontingentverbrauch. [tweet-2050565218049376471](../sources/tweet-2050565218049376471.md)

Die README dokumentiert Verhalten und Voraussetzungen, liefert aber keinen unabhängigen Qualitätsvergleich. Das gespeicherte Video hat kein auswertbares Transkript; Installation, Authentifizierung und Reviews wurden hier nicht getestet. [tweet-2050565218049376471](../sources/tweet-2050565218049376471.md)
