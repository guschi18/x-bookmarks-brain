---
tags: [agents, tools]
sources: [tweet-2101355584305943031.md, tweet-2104688418659987802.md]
created: 2026-10-03
updated: 2026-10-06
---

# Jev Model Router

## Rolle und Artefakt (Stand 2026-09)

Der Mod für [Claude Code](Claude%20Code.md) nutzt [Jev](Jev.md) über TypeSafe oder Vercel AI Gateway; das gespeicherte README liegt unter https://github.com/davila7/claude-code-templates/tree/main/cli-tool/components/mods/productivity/jev-model-router. Der Hauptpost bedankt sich für einen Gateway-Fix, dessen Screenshot einen fehlenden Protokollversionsparameter beschreibt. [tweet-2101355584305943031](../sources/tweet-2101355584305943031.md)

## Routing-Policy (Stand 2026-09)

Ein Request fragt parallel tier (mechanisch / gewöhnliches Engineering / schwierig), effort auf vier Stufen und risky ab. Standardmäßig werden Subagentenmodell und Main-Effort geroutet, das Hauptmodell bleibt unverändert. Die Klassifikation erfolgt bei prompt.submit, wird auf den ersten Modellrequest angewendet und für den Turn wiederverwendet. [tweet-2101355584305943031](../sources/tweet-2101355584305943031.md)

Die README nennt minUpgradeConfidence 0,3 und minDowngradeConfidence 0,6; risky über 0,7 erzwingt die tiefe Stufe. Ohne Konfidenz darf die Policy nur hochstufen. Fehler, Timeout (Standard 800 ms) oder unlesbare Antwort lassen den ursprünglichen Request bestehen; reine Slash-Befehle ohne Zusatztext werden nicht klassifiziert. [tweet-2101355584305943031](../sources/tweet-2101355584305943031.md)

TypeSafe hat bei zwei gesetzten Keys Vorrang. Gateway-Konfidenz wird aus dem Maximum einer optionalen Wahrscheinlichkeitsverteilung abgeleitet; ohne Verteilung fehlt sie. Ohne Keys nutzt der Mod den eingebauten Classifier. Subagent-Effort setzt er nicht, da das Agent-Tool dafür keinen Parameter anbietet. [tweet-2101355584305943031](../sources/tweet-2101355584305943031.md)

## Installation und Diagnose (Stand 2026-09)

Die README nennt npx claude-code-templates@latest --mod productivity/jev-model-router, Claude Code 2.1.259+ und CLAUDE_CODE_ENABLE_FUNCTION_HOOKS=1. Projektinstallation braucht Projektvertrauen; pluginConfigs verwendet je nach Ladepfad jev-model-router@skills-dir oder jev-model-router. Entscheidungslogs zeigen die wirklichen Requeständerungen, während Statusleiste und Effortbox unverändert bleiben können. [tweet-2101355584305943031](../sources/tweet-2101355584305943031.md)

## Abweichung und Grenzen (Stand 2026-09)

Der zitierte Launch-Post spricht von Hauptmodellwahl nur beim Sitzungsstart; die gespeicherte README beschreibt optionales turn.step-Routing, standardmäßig aus. Das sind unterschiedliche gespeicherte Beschreibungen, kein einheitlich getestetes Verhalten. Modellwechsel können laut README [Prompt Caching](../concepts/Prompt%20Caching.md) invalidieren; mit API-Key verlassen Prompt beziehungsweise Subagentenauftrag die Maschine. Die experimentellen Hook- und Gateway-Schnittstellen sowie Einsparungen wurden hier nicht getestet. [tweet-2101355584305943031](../sources/tweet-2101355584305943031.md)

## Kopierbare Host-Policy (Stand 2026-09)

Der vollständige Sechs-Punkte-Prompt lässt [Jev](Jev.md) vor Workerstart ein zugelassenes Profil mit einem oder zwei Sessions wählen, einschließlich Modell und Effort. Ohne Auswahl gilt der Hostdefault; der Host prüft die Auswahl, setzt feste Sessionwerte und behält Rechte und Freigaben. [tweet-2104688418659987802](../sources/tweet-2104688418659987802.md)

Für klare Coding-Aufträge empfiehlt Avid Sonnet 5.5 mit medium, mehr Effort für komplexe Reasoning-/JSON-Aufgaben. Eine zweite Claude-Session ist auf unabhängige Recherche oder ausdrücklich gewünschtes Review begrenzt; ihre Übergabe enthält Aufgabe, Dateien, Grenzen und Done-Kriterien. [tweet-2104688418659987802](../sources/tweet-2104688418659987802.md)

Die letzten Regeln verlangen Auftragsabschluss ohne ungefragte Zusatzfeatures oder Reviewrunden und mindestens einen passenden Test, Build, Typecheck oder anderen Codecheck; fehlt ein Check, soll das benannt werden. Der vollständige Wortlaut steht in der Source; vierfache Beschleunigung ist unbelegt. [tweet-2104688418659987802](../sources/tweet-2104688418659987802.md)
