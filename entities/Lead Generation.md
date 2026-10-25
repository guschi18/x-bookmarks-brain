---
tags: [tools, marketing]
sources: [tweet-2099765040807080229.md, tweet-2097920782823305690.md]
created: 2026-10-08
updated: 2026-10-09
---

# Lead Generation

## Projekt und Funktion (Stand 2026-09)

https://github.com/Madi-S/Lead-Generation ist eine Python-Sammlung zur Lead-Erfassung. Die gespeicherte README führt Google Maps, Yelp und CSV-Export als vorhandene Funktionalität auf; der Post nennt Unternehmen, Websites und E-Mail-Adressen als Ziele. [tweet-2099765040807080229](../sources/tweet-2099765040807080229.md)

## Installation und Quickstart (Stand 2026-09)

Die README empfiehlt pip install py-lead-generation und verlinkt https://pypi.org/project/py-lead-generation . Alternativ nennt sie den Repo-Checkout und run.py; die ältere Version liegt unter archived/google-maps/extractor.py. [tweet-2099765040807080229](../sources/tweet-2099765040807080229.md)

Ihr Quickstart importiert GoogleMapsEngine und YelpEngine aus py_lead_generation. GoogleMapsEngine erhält Suchbegriff, Ort und Zoom, danach await engine.run() und engine.save_to_csv(). Das Yelp-Beispiel verwendet YelpEngine('Pizza', 'Mexico, Pampanga, Philippines') und engine.save_to_csv('pizza_leads.csv'); ausgeführt wird die asynchrone Funktion über asyncio.run(main()). [tweet-2099765040807080229](../sources/tweet-2099765040807080229.md)

## Grenzen und offene Arbeit (Stand 2026-09)

Die README beschreibt die ältere Sammlung als veraltet und führt Refactoring, Tests, GUI/CLI-Ausbau, geografische Rasterung und Skalierungsarbeit als TODOs auf. Automatischer E-Mail-/SMS-Versand und weitere Quellen sind Vorhaben beziehungsweise Erwartungen, keine belegten fertigen Funktionen. Vollständigkeit der Kontaktdaten und Erfolg auf großen Datenmengen wurden hier nicht geprüft. [tweet-2099765040807080229](../sources/tweet-2099765040807080229.md)

Der CoreClaw-Link in der README ist ein Sponsor-Angebot und vom beschriebenen Python-Paket zu unterscheiden. [tweet-2099765040807080229](../sources/tweet-2099765040807080229.md)

## Verwandte Implementierung (Stand 2026-09)

[Google Maps Scrapper](Google%20Maps%20Scrapper.md) ist das separate Repository zohaibbashir/Google-Maps-Scrapper. Es dokumentiert Playwright, Firmendaten und CSV-Append per `python main.py -s <search> -t <count> -o <file> --append`; die README warnt vor Python-Abhängigkeiten und wechselnden Maps-XPaths. Dies ist eine zusätzliche Implementierung, keine neue Funktion von Lead Generation. [tweet-2097920782823305690](../sources/tweet-2097920782823305690.md)
