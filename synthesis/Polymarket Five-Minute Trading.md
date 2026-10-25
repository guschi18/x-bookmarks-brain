---
tags: [trading, crypto, agents, tools]
sources: [tweet-2046608709707600278.md, tweet-2043690015675318360.md]
created: 2026-10-20
updated: 2026-10-21
---

# Polymarket Five-Minute Trading

## Quellen und Rollen (Stand 2026-04; später gespeicherte Repository-Stände)

Lunars Artikel beschreibt einen Botentwurf für fünfminütige BTC-Märkte, ergänzt durch [Claude Code](../entities/Claude%20Code.md), einen VPS und Marktdaten. Das gespeicherte Paket enthält den vollständigen [Artikel](https://x.com/i/article/2046222969102372864), die READMEs von [Poly Data](https://github.com/warproxxx/poly_data) und [Polymarket CLI](https://github.com/Polymarket/polymarket-cli) sowie eine [Kreo-Seite](https://kreo.app/@lunar), deren Text nur Navigation und Telegram-Weiterleitung enthält. Diese Artefakte sind von den behaupteten Handelsergebnissen zu trennen. [tweet-2046608709707600278](../sources/tweet-2046608709707600278.md)

## Historischer Strategieentwurf (Stand 2026-04)

Der Autor kombiniert zwei Signale: Binance und Coinbase sollen gegenüber dem Price to Beat gleichzeitig um mehr als 50 Dollar in dieselbe Richtung abweichen; die Summe der obersten zehn Bid-/Ask-Mengen liefert als zweites Signal eine Orderbuch-Ratio über 1,8 für UP oder unter 0,55 für DOWN. Die Zahlen sind vorgeschlagene Schwellen im Artikel, keine unabhängig validierten Handelsregeln. [tweet-2046608709707600278](../sources/tweet-2046608709707600278.md)

Der Entwurf erlaubt Einstiege 60 bis 180 Sekunden nach Marktöffnung. Er zeigt Gewinnmitnahme bei einem Anteilspreis ab 0,75, Stop bei höchstens 0,35 und Halten bis zur Auflösung bei weniger als 60 verbleibenden Sekunden. Eine Schleife sammelt Daten, filtert Signale, platziert einen Auftrag und beobachtet die Position. Diese Beschreibung ist ein historischer Ablaufentwurf, keine Betriebsfreigabe. [tweet-2046608709707600278](../sources/tweet-2046608709707600278.md)

## Poly Data: Analysegrundlage (gespeicherter V2-Stand nach 2026-04-28)

Die README von warproxxx/poly_data beschreibt eine Pipeline: CLOB-Marktdaten laden, OrderFilled-Ereignisse des CTF Exchange V2 auf Polygon per Envio HyperSync lesen, mit Marktmetadaten verbinden und strukturierte Trades als CSV schreiben. Cursordateien erlauben Fortsetzung; `uv run poly-data` ist der dokumentierte Einstieg. Die README verlangt einen HyperSync-Token und nennt `PROCESS_CHUNK_SIZE=500000` als Option bei knapperem RAM. [tweet-2046608709707600278](../sources/tweet-2046608709707600278.md)

Die Quelle datiert den Vertragswechsel auf den 28.04.2026 und bewahrt den alten Retriever unter [v1-final](https://github.com/warproxxx/poly_data/tree/v1-final). Dieser Text entstand damit nach dem Tweet vom 21.04.2026 und darf nicht dessen damalige Implementierung belegen. Laut README soll die Filterung eines Nutzers über maker erfolgen; reine Offline-Tests betreffen Decoding, Handelsrichtung, Preise und Datenabbildung. Sie sind kein Profitabilitätstest. [tweet-2046608709707600278](../sources/tweet-2046608709707600278.md)

## Polymarket CLI: Lesen und Ausführen (gespeicherter README-Stand; Prüfung 2026-10-20)

Die offizielle Rust-CLI dokumentiert Marktsuche, Orderbücher und Preise ohne Wallet, darunter `polymarket markets list --limit 5` und JSON-Ausgabe mit `-o json`. Orders, eigene Handelsdaten und Onchain-Aktionen benötigen Wallet-/Signaturkonfiguration; die README nennt private Schlüssel und drei Signaturtypen. Das Projekt bezeichnet sich ausdrücklich als frühe experimentelle Software und warnt vor großen Geldbeträgen. [tweet-2046608709707600278](../sources/tweet-2046608709707600278.md)

Die README unterscheidet Limit- und Market-Order-Befehle sowie GTC, FOK, GTD und FAK. Die pauschale Artikelformulierung, es gebe keine Market Orders, reicht daher nicht als vollständige CLI-Anleitung; API-Bezeichnung und konkrete Ausführungssemantik sind getrennt zu prüfen. Die CLI ist ein Werkzeug und keine mitgelieferte Implementierung von Lunars Strategie. [tweet-2046608709707600278](../sources/tweet-2046608709707600278.md)

## Beleggrenzen und innere Widersprüche (Stand 2026-04)

Die angeblichen Anthropic-DMs, 14 Sekunden Oracle-Lag, 94 Prozent Follow-through, 71 Prozent Gewinnquote und 14.200 Dollar Monatsgewinn sind Autorenbehauptungen ohne gespeicherte Roh-Auswertung. Der Post nennt 90 Sekunden für das Follow-through, der Artikel zwei Minuten; daraus wird kein gemeinsam bestätigter Messwert. [tweet-2046608709707600278](../sources/tweet-2046608709707600278.md)

Die berichteten 1.847 Trades, 71 Prozent Gewinner, 34 Dollar mittlerer Gewinn und 19 Dollar mittlerer Verlust ergeben rechnerisch ungefähr 34.410 Dollar vor nicht ausgewiesenen Kosten, nicht die genannten 14.200 Dollar. Rundungen allein erklären diese Differenz nicht; eine Überleitung fehlt. Diese Plausibilitätsrechnung prüft keine Trades. [tweet-2046608709707600278](../sources/tweet-2046608709707600278.md)

Der Code ist nicht vollständig ausführbar: Hilfsfunktionen fehlen, `execute_trade` und `monitor_position` verlangen einen zusätzlichen Parameter, den die gezeigte Hauptschleife nicht übergibt, und pending als PnL-Wert passt nicht zur anschließenden numerischen Addition. Der Artikel verweist auf vier Repository-Rollen, speichert dort aber keine vollständigen Links; konkret erhalten sind die beiden separaten READMEs. [tweet-2046608709707600278](../sources/tweet-2046608709707600278.md)

Das 20,5-Sekunden-Video hat nur das nicht aussagekräftige Transkript Tick tock toys video. Weder die Strategie noch die beiden Werkzeuge wurden installiert, mit einer Wallet verbunden oder mit Echtgeld getestet. [Polymarket Trading Bot](../entities/Polymarket%20Trading%20Bot.md) dokumentiert ein anderes Repository und ist kein Beleg für diesen Entwurf. [tweet-2046608709707600278](../sources/tweet-2046608709707600278.md)

## Ergänzender Mehrmarkt-Botentwurf (Stand 2026-04-13)

Ein älterer Artikel desselben Accounts beschreibt einen anderen Ansatz: poly_data dient der Wallet-Auswahl, Polymarket CLI dem Scanner, Polymarket/agents der Analyse und Polymarket-Trading-Bot der Ausführung. Er filtert Wallets nach mindestens 100 Trades und mehr als 70 Prozent Gewinnquote; der Scanner verlangt mindestens 0,07 Preisdifferenz und 500 Dollar Tiefe auf beiden Seiten. Diese Grenzwerte sind Autorenparameter, keine validierte Handelsstrategie. Der spätere Fünfminuten-Entwurf vom 21.04.2026 wird dadurch nicht ersetzt. [tweet-2043690015675318360](../sources/tweet-2043690015675318360.md)

Der Analyse-Prompt verlangt Basisrate, Nachrichten, Ziel-Wallets und mögliche Fehlbewertung der Menge; drei von vier Checks sollen eine These auslösen. Drei Strategie-Agenten stimmen anschließend ab: zwei Kaufstimmen volle, eine halbe Position, keine Einigung kein Trade. Als Ausstiege nennt der Artikel 85 Prozent der erwarteten Bewegung, dreifaches Zehnminutenvolumen oder eine nach 24 Stunden unveränderte These. Der vollständige Artikel einschließlich Prompts bleibt auf der Source erhalten. [tweet-2043690015675318360](../sources/tweet-2043690015675318360.md)

Der Code ist keine ausführbare Gesamtimplementierung: Hilfsfunktionen und Platzhalter fehlen. Quarter Kelly wird falsch benannt: min(f_star, 0.25) begrenzt auf 25 Prozent des Kontos, statt f_star durch vier zu teilen. Das Beispiel mit Wahrscheinlichkeit 0,82, Preis 0,65 und 800 Dollar Konto liefert im gezeigten Code 200 Dollar statt der angegebenen 114,28. Zudem nennt der Text 4–48 Stunden bis Auflösung, der Scanner lässt bis 168 zu. Diese Textprüfung ist kein Backtest. [tweet-2043690015675318360](../sources/tweet-2043690015675318360.md)

Die im Artikel berichteten 25 Dollar Monatskosten, 74 Prozent Gewinnquote und 11.400 Dollar Gewinn nach 19 Tagen sind unbelegte Autorenangaben. Vier vollständige Repository-Links sind nicht strukturiert gespeichert; poly_data ist im Text identifizierbar. Die bereits separat dokumentierten README-Stände von Poly Data und CLI bleiben zeitlich getrennt. [tweet-2043690015675318360](../sources/tweet-2043690015675318360.md)
