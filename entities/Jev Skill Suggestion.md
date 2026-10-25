---
tags: [agents, tools]
sources: [tweet-2101888707259256903.md, tweet-2101885477158547753.md]
created: 2026-10-03
updated: 2026-10-08
---

# Jev Skill Suggestion

## Beschriebener Mechanismus (Stand 2026-09)

Daniel Avila beschreibt einen [Claude Code](Claude%20Code.md)-Mod auf Basis von TypeSafes Skill-Suggestion-Beispiel. Skills sollen nur vom Nutzer aufrufbar konfiguriert werden; [Jev](Jev.md) erhält die verfügbare Skillliste, wählt pro Anfrage einen passenden Skill und nur dessen Inhalt wird in den Hauptkontext eingefügt. [tweet-2101888707259256903](../sources/tweet-2101888707259256903.md)

Der zitierte Post nennt TypeSafe und Vercel AI Gateway sowie npx claude-code-templates@latest --mod productivity/jev-skill-suggestion. Der Hauptpost schlägt vor, Skill-, Effort- und Toolauswahl als kleine unabhängige Entscheidungsdienste außerhalb des Hauptloops zu führen; siehe [Typed Decision Layer](../concepts/Typed%20Decision%20Layer.md) und [Context Engineering](../concepts/Context%20Engineering.md). [tweet-2101888707259256903](../sources/tweet-2101888707259256903.md)

## Evidenzgrenze (Stand 2026-09)

Der gespeicherte aitmpl.com-Body enthält nur ASCII-Branding, keine Implementierungsdetails. Das Bild beschreibt Ranking und Prüfung durch getrennte TypeSafe-Fragen, belegt aber weder die konkrete Mod-Implementierung noch einen gemessenen Kontextgewinn; Installation und Auswahlqualität sind ungeprüft. [tweet-2101888707259256903](../sources/tweet-2101888707259256903.md)

## Originalankündigung (Stand 2026-09)

Daniel Avila kündigt den Mod als "Jev Skill Suggestion for Claude Code" an; der Mechanismus entspricht der Beschreibung oben (Skillliste an [Jev](Jev.md), Auswahl pro Anfrage, nur der gewählte Skill im Kontext). [tweet-2101885477158547753](../sources/tweet-2101885477158547753.md)

Genannt werden Betrieb mit der TypeSafe-API oder dem Vercel AI Gateway und die Installation per npx claude-code-templates@latest --mod productivity/jev-skill-suggestion. Die verlinkte Seite des Claude-Code-Templates-Katalogs ist nur als ASCII-Branding gespeichert; Implementierungsdetails, Kontextersparnis und Trefferquote der Skillwahl fehlen. [tweet-2101885477158547753](../sources/tweet-2101885477158547753.md)
