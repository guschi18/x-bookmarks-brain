---
tags: [tools]
sources: [tweet-2095878511164547237.md]
created: 2026-10-08
updated: 2026-10-08
---

# Learnomarchy

## Lernen im echten Desktop (Stand 2026-09)

[MaximilianHansen/learnomarchy](https://github.com/MaximilianHansen/learnomarchy) ist laut README ein Tastenkürzel-Trainer als Arcade-Spiel. Er erzeugt echte Fenster und prüft Missionen über Hyprlands IPC mit Zeitmessung auf Zehntelsekunden. Die HUD bleibt über Workspaces hinweg sichtbar; `q` bricht ab, `r` startet neu. [tweet-2095878511164547237](../sources/tweet-2095878511164547237.md)

Neun Levels und die Ränge CADET, PILOT und ACE verwenden Sterne zum Freischalten; drei Sterne öffnen den nächsten Level, fünf markieren die Sollzeit. Tastenkürzel erscheinen zunächst als Hinweis, danach zählt Erinnern; bei Stocken werden Hinweise wieder eingeblendet. Der Trainer zeigt eine Recall-Rate und erstellt optional Ergebnis-Share-Cards. [tweet-2095878511164547237](../sources/tweet-2095878511164547237.md)

## Installation und Wartung (Stand 2026-09)

Die README setzt Omarchy 4 voraus und nennt ein Bash-Skript mit vorhandenen Werkzeugen wie hyprctl, jq und wl-copy. Installation: [Repository](https://github.com/MaximilianHansen/learnomarchy) klonen, `./install.sh` lesen und ausführen; als Schnellweg dokumentiert sie das Herunterladen des install.sh und direkte Ausführen mit Bash. [tweet-2095878511164547237](../sources/tweet-2095878511164547237.md)

`learnomarchy` öffnet die Levelauswahl, `--level 7` wählt einen Level, `--reset` löscht Fortschritt, `--update` aktualisiert und `--uninstall` entfernt die Installation. Der Fortschritt liegt laut README in `~/.local/state/learnomarchy/save`; Darstellung verwendet die 16 Terminalfarben. [tweet-2095878511164547237](../sources/tweet-2095878511164547237.md)

## Abgrenzung und Evidenzgrenze (Stand 2026-09)

Dies ist das Repository von Maximilian Hansen, getrennt vom anderen bereits erfassten [Learn Omarchy](Learn%20Omarchy.md)-Kurs. Die README nennt stock Hyprland mit Omarchy-Tastenkürzeln als mögliche, ungetestete Umgebung; hier wurden Installation, Missionserkennung und Lernwirkung ebenfalls nicht geprüft. [tweet-2095878511164547237](../sources/tweet-2095878511164547237.md)
