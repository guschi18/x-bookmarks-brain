---
tags: [agents, research, tools]
sources: [tweet-2102727405198876753.md]
created: 2026-10-25
updated: 2026-10-25
---

# Qwen Intelligence

## Ankündigung und Quellenstand (Stand 2026-09)

[Qwen Intelligence](https://www.qwenintelligence.com/) kündigt Mobile Planner Agent, Mobile-Use Agent und Mobile Creative Agent als Kombination für persönliche mobile Aufgaben an. Die Source enthält den vollständigen Post, sieben Primärtexte und 73 strukturierte Links. Das Launch-Bild liefert keine technischen Messdaten. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)

## Planung, Zustand und GUI

[Qwen-Planner-Agent](https://github.com/Tongyi-MAI/Qwen-Planner-Agent) verbindet laut Bericht einen trainierten Planner mit einem zustandsbehafteten Harness: relevante Erinnerungen abrufen, Skills auswählen, bestätigte Artefakte an Subagenten übergeben und auf Toolfehler reagieren. Datenkurierung, Training und Harness-Anpassung sollen über Ausführungsfeedback zusammenwirken. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)

Das Repo ist ausdrücklich nur die Website und der technische Bericht mit aufgezeichneten Beispielen; Modellgewichte, Trainingscode und Agentenimplementierung werden dort nicht veröffentlicht. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)

Die gespeicherte Planner-Tabelle nennt 77,05 Prozent Overall auf MobilePA-Bench und 2,41 USD pro 1.000 Aufgaben als geschätzte Outputtoken-Kosten. Das ist kein Gesamtpreis: Eingaben, Tools, Geräteausführung und zusätzlicher Harness-Aufwand fehlen. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)

Der [Qwen-UI-Agent-Bericht](https://tongyi-mai.github.io/Qwen-UI-Agent/) beschreibt GUI-Nutzung auf Mobilgeräten sowie weitere Oberflächen. Seine Evaluation weist darauf hin, dass Harness, Judge, Simulator, Laufzeit und Aufgabenmengen von anderen Evaluierungen abweichen können. Die Zahlen sind nicht ohne Weiteres zwischen Tabellen vergleichbar. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)

## MobilePA-Bench

[MobilePA-Bench](https://tongyi-mai.github.io/MobilePA-Bench/) umfasst laut Projekttext 1.705 Aufgaben, 212 realistische Tools und 13 Domänen. Geprüft werden Toolnutzung, Memory, Skills und Subagenten-Zusammenarbeit in einem persistenten Zustand. Overall gewichtet diese vier Bereiche mit 50/20/20/10 Prozent. Verdeckte Aufgaben und Ground Truth bleiben privat; die Website bietet eine gehostete Evaluation an. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)

## MobileWorld: ausführbarer Benchmark

[MobileWorld](https://github.com/Tongyi-MAI/MobileWorld) dokumentiert 201 Aufgaben in 20 Apps mit längeren und appübergreifenden Abläufen. Neben GUI-Aufgaben gibt es simulierte Nutzerinteraktion und Aufgaben mit [Model Context Protocol](../concepts/Model%20Context%20Protocol.md)-Tools. Docker-/Android-Umgebung, selbst gehostete Backends und Snapshots sollen vergleichbare Startzustände ermöglichen. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)

Erfolg wird je Aufgabe über Textvergleich, Backend-Datenbank, lokalen Speicher oder App-Callbacks geprüft. Das [Projektportal](https://tongyi-mai.github.io/MobileWorld/) ergänzt Trajektorien und einen Vergleich einzelner Agentenläufe. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)

Die gespeicherte README verlangt privilegiertes Docker, KVM und Python ab 3.12; Linux oder Windows mit WSL2/KVM, macOS noch in Arbeit. Dies ist der gespeicherte Dokumentstand, keine eigene Plattformprüfung. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)

Der dokumentierte Ablauf lautet Repository klonen, uv sync, API-Zugänge konfigurieren, mw env check, mw env run und mw eval. --enable_mcp und --enable_user_interaction erweitern die Aufgabenklassen; mw logs view öffnet die Trajektorienansicht. Physische Android-Geräte werden separat per ADB beschrieben. Diese Befehle wurden hier nicht ausgeführt. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)

## Creative-Link und Evidenzgrenzen

Der als Creative-Agent-Link gespeicherte [arXiv-Eintrag 2608.16887](https://arxiv.org/abs/2608.16887) behandelt Pixel-Space-Diffusion: Vortraining im latenten Raum und Übergang beim Posttraining. Der Abstract nennt 3,18- bis 4,75-fache Inferenzbeschleunigung in seinen Experimenten; dies belegt weder die gesamte mobile Creative-Agent-Funktion noch die 3-Sekunden-Aussage des Tweets. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)

Die Launch-Angaben 82,1 auf MobileWorld, 92,2 auf MobileWorld-Real, 97,2 auf AndroidDaily und 90 Prozent Ende-zu-Ende-Erfolg sind Anbieterwerte für unterschiedliche Tests. Sie sind keine hier replizierte Leistung im persönlichen Alltag. Die gespeicherte AI-Bildbeschreibung nennt den dritten Agenten abweichend; maßgeblich für die Ankündigung ist Mobile Creative Agent im Originaltext. [tweet-2102727405198876753](../sources/tweet-2102727405198876753.md)
