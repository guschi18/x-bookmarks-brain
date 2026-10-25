---
tags: [agents, tools]
sources: [tweet-2076626834561925183.md]
created: 2026-10-01
updated: 2026-10-01
---

# Verifier Setup

## Zweck (Stand 2026-07)

[Verifier Setup](https://github.com/AI-Builder-Club/skills/blob/main/skills/verifier-setup/SKILL.md) richtet laut gespeicherter Skill-Datei ein Repository für spätere Ergebnisprüfung ein. Es erzeugt oder ergänzt eine /verify-SOP, einen Dev-Launcher mit Skill und einen passenden Bedien-Driver; das Setup selbst führt noch keinen einzelnen Verifikationslauf aus. [tweet-2076626834561925183](../sources/tweet-2076626834561925183.md)

## Ablauf (Stand 2026-07)

Zuerst vorhandenen App-Start, Prüf-SOP, Driver, Tests, Sandbox und Belegablage inventarisieren und funktionierende Teile behalten. Danach tatsächlichen Stack, Ports, Authentifizierung, Regressionbefehle und Belegupload ermitteln; fehlende Voraussetzungen bereitstellen, Ausführung lokal oder in Crabbox und den Driver bestätigen, schließlich eine kurze repospezifische SOP generieren. [tweet-2076626834561925183](../sources/tweet-2076626834561925183.md)

Für Weboberflächen nennt der Skill playwright-cli, für API/CLI passende konkrete Werkzeuge. Die spätere /verify-SOP sieht einen getrennten Prüfer, reale Bedienung und Screenshot-/Videobelege im PR vor; andere App-Typen erhalten passende Ausgaben-/Assertionsprüfungen. [tweet-2076626834561925183](../sources/tweet-2076626834561925183.md)

## Einsatzgrenze (Stand 2026-07)

Im [Loopany](Loopany.md)-Walkthrough ist diese Infrastruktur Voraussetzung für risikoreiche [Loop Engineering](../concepts/Loop%20Engineering.md)-Aufgaben. Wiederverwendung statt Überschreiben bestehender Teamregeln ist ausdrücklich vorgesehen. Die gespeicherte Datei belegt den Setup-Vertrag, keine erfolgreiche Einrichtung oder universelle Wirksamkeit. [tweet-2076626834561925183](../sources/tweet-2076626834561925183.md)
