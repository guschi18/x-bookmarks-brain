---
tags: [agents, tools]
sources: [tweet-2052352848059404408.md]
created: 2026-10-14
updated: 2026-10-14
---

# Remote Agent Access

## Prinzip (Stand 2026-05)

Der von David Ondrej empfohlene zitierte Post kombiniert drei Rollen: tmux hält Terminalsitzungen beim Trennen der Verbindung offen, Termius stellt den mobilen SSH-Client, und Tailscale verbindet eigene Geräte in einem gemeinsamen Netz. Damit soll ein bereits laufender Agent von einem anderen Gerät weiter beobachtet und bedient werden. [tweet-2052352848059404408](../sources/tweet-2052352848059404408.md)

## Berichtetes Beispiel (Stand 2026-05)

Der zitierte Autor beschreibt drei Agentensitzungen mit Hermes und Qwen3.6-27B auf einem DGX Spark, die er vom Handy im Fitnessstudio verwaltet. Das ist ein konkreter Erfahrungsbericht; der dazu erwähnte Screenshot und eine vollständige Einrichtung sind nicht gespeichert. [tweet-2052352848059404408](../sources/tweet-2052352848059404408.md)

## Voraussetzungen und Grenzen (Stand 2026-05)

Aus dem beschriebenen Stack folgen als Voraussetzungen ein laufender Host mit Agent und tmux, ein erreichbarer SSH-Dienst sowie eine Verbindung beider Geräte. Eine überlebende Netzwerkunterbrechung ist keine Zusage, dass ein Prozess einen Host-Neustart oder Stromausfall überlebt. Zugangs- und Rechtekonfiguration wurden hier nicht eingerichtet oder geprüft. [tweet-2052352848059404408](../sources/tweet-2052352848059404408.md)

Der Ansatz ergänzt [Local Agent Inference](Local%20Agent%20Inference.md) um den Fernzugriff: Das Modell bleibt auf dem eigenen Rechenhost, während das Handy die Terminaloberfläche bedient. Das ist aus dem beschriebenen Beispiel abgeleitet, keine Messung der Modellleistung oder allgemeine Offline-Garantie. [tweet-2052352848059404408](../sources/tweet-2052352848059404408.md)
