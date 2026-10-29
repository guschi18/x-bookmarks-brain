---
tags: [agents, tools, security, product-building]
sources: [tweet-2098354614856744978.md, tweet-2115097056394240293.md]
created: 2026-10-08
updated: 2026-10-28
---

# OpenBot

## Rolle und Architektur (Stand 2026-09)

[CopilotKit/OpenBot](https://github.com/CopilotKit/OpenBot) beschreibt eine selbst betriebene Alpha-Vorlage für KI-Mitarbeiter über AG-UI. Jeder Bot bekommt einen Computercontainer mit eigenem Browserprofil und Workspace; Agenten können aus unterschiedlichen Frameworks oder eigener Implementierung stammen. Bun, Docker, PostgreSQL/pgvector und CopilotKit Intelligence tragen App, API und persistente Threads. [tweet-2098354614856744978](../sources/tweet-2098354614856744978.md)

Ein zentrales Gateway löst Ziele auf, prüft Policy, schreibt den Audit-Eintrag und führt dann Computer-, Datei-, MCP- oder Komponentenaktionen aus. Die README beschreibt CEL-Regeln mit Deny vor Allow und Ablehnung bei fehlender oder fehlerhafter Policy; diese Sicherheitsversprechen wurden hier nicht unabhängig geprüft. [tweet-2098354614856744978](../sources/tweet-2098354614856744978.md)

## Einrichtung und Bedienung (Stand 2026-09)

Dokumentierter Clone-Einstieg: `.env.example` nach `.env` kopieren, `bun install`, ein Intelligence-Projekt auswählen und `bun scripts/setup-learning.ts` ausführen; Modell-Key ergänzen und mit `bash scripts/start.sh` starten. Der Helper setzt Runtime-Key und Learning-Container; vollständige Schritte und Startfehler stehen in [prompt.txt](https://github.com/CopilotKit/OpenBot/blob/main/prompt.txt) und der [Dokumentation](https://github.com/CopilotKit/OpenBot/blob/main/docs/README.md). [tweet-2098354614856744978](../sources/tweet-2098354614856744978.md)

Laut README läuft die Clone-App auf Port 3010, die API auf 3001; ein Deployment-Image bedient beide auf 3001. `bash scripts/stop.sh` stoppt auch Botcomputer, während Datenbank, Dateien und Browserprofile als Volumes erhalten bleiben. Das ist gespeicherte Betriebsdokumentation, kein lokaler Deploymenttest. [tweet-2098354614856744978](../sources/tweet-2098354614856744978.md)

Bot-/Channel-Seiten zeigen Bildschirm und Aktivität. Bei Login oder 2FA kann ein Mensch übernehmen; währenddessen werden Botaktionen abgelehnt. Agenten erhalten separate MCP-, Skill- und Komponentenrechte, Admin-Seiten zeigen Credentials, Grenzen und Audit. Optionale Routinen laufen mit einem Worker; die README nennt mindestens 15 Minuten Abstand, maximal 20 aktive Routinen und Abschaltung nach zehn aufeinanderfolgenden Fehlern. [tweet-2098354614856744978](../sources/tweet-2098354614856744978.md)

## Zugriff und Grenzen (Stand 2026-09)

Die Vorlage aktiviert `OPENBOT_SINGLE_USER=true`: jede Anfrage gilt als ein Administrator. Vor Zugriff weiterer Personen verlangt die README dessen Abschaltung und konfigurierte Authentifizierung; Computer und Supervisor binden standardmäßig an Loopback. Private Agentenendpunkte benötigen eine explizite Hostliste; Schlüssel werden laut Projekt verschlüsselt gespeichert und nicht zurückgegeben. [tweet-2098354614856744978](../sources/tweet-2098354614856744978.md)

Die gespeicherte README bezeichnet OpenBot als Vorlage unter aktiver Entwicklung, keine fertig betriebene Hosted-Lösung. Die im Tweet genannten 4.500 Sterne belegen Popularität am Postdatum, keine Betriebsreife. Konfiguration, Isolation und Policy-Durchsetzung wurden hier nicht getestet. [tweet-2098354614856744978](../sources/tweet-2098354614856744978.md)

[OpenDots](OpenDots.md) verwendet verwandte OpenBot-Infrastruktur; dessen eigene Workspace-Vorlage bleibt getrennt. Diese Quelle dokumentiert OpenBots vollständigen Betrieb statt nur des Computerbausteins. [tweet-2098354614856744978](../sources/tweet-2098354614856744978.md)

## Verwandtes Produkt OpenDuet (Stand 2026-10)

Die README von [OpenDuet](OpenDuet.md) nennt, dass OpenDuet heute als OpenBot läuft, mit eigenem Namen, Bots und Skills darüber. [tweet-2115097056394240293](../sources/tweet-2115097056394240293.md) Damit ist OpenDuet eine proaktive Ausprägung derselben Plattform, nicht ein getrenntes System; das ist eine Herstellerangabe der README. [tweet-2115097056394240293](../sources/tweet-2115097056394240293.md)
