---
tags: [tools, security]
sources: [tweet-2053841305030324735.md]
created: 2026-10-13
updated: 2026-10-13
---

# Ladder

## Werkzeug und Ablauf (Stand 2026-05; gespeicherte README)

[everywall/ladder](https://github.com/everywall/ladder) ist ein selbst gehosteter HTTP-Proxy zur Untersuchung von Website-Auslieferung. Er modifiziert Anfragen vor dem Abruf und Antworten vor der Ausgabe, etwa User-Agent, Header, HTML, CSS und JavaScript. Domainbezogene YAML-Regeln bestimmen diese Änderungen. [tweet-2053841305030324735](../sources/tweet-2053841305030324735.md)

Die README nennt Browseroberfläche, API, Roh-HTML-Ausgabe, Docker und Binärdateien. Eine Ziel-URL lässt sich direkt an die Proxy-URL anhängen; `http://localhost:8080/raw/https://www.example.com` liefert die Rohansicht. [tweet-2053841305030324735](../sources/tweet-2053841305030324735.md)

## Einrichtung und Regeln

Die gespeicherte Docker-Anleitung verwendet `ghcr.io/everywall/ladder:latest` mit Port 8080 und `RULESET=https://raw.githubusercontent.com/everywall/ladder-rules/main/ruleset.yaml`. `USERPASS` aktiviert Basic Auth; `ALLOWED_DOMAINS` begrenzt die Zielseiten. Die README warnt vor einer öffentlich zugänglichen Instanz ohne Authentifizierung. [tweet-2053841305030324735](../sources/tweet-2053841305030324735.md)

Regeln können Request-Header überschreiben, URL-Domain/Pfad/Query verändern, Text per Regex ersetzen und Code in DOM-Positionen einfügen. Das ist dokumentierte Konfigurierbarkeit, kein hier getesteter Nachweis für eine konkrete Website. [tweet-2053841305030324735](../sources/tweet-2053841305030324735.md)

## Grenzen

Die README erklärt zunächst, dass Ladder fortgeschrittene Anti-Bot-Schutzmaßnahmen nicht umgeht; später beschreibt sie optionales FlareSolverr für Cloudflare- und JavaScript-Challenges. Diese unterschiedlichen Aussagen werden als Quellenstand erhalten, ohne universelle Funktion zu behaupten. Der Screenshot zeigt nur die Proxy-Startseite; die Post-Zahl von 16.000 Downloads ist nicht unabhängig verifiziert. [tweet-2053841305030324735](../sources/tweet-2053841305030324735.md)
