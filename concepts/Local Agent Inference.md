---
tags: [llm-training, agents, tools]
sources: [tweet-2095906342154424750.md, tweet-2097976305354518968.md, tweet-2093095040281379187.md, tweet-2092962838822150508.md, tweet-2092962836934705501.md, tweet-2090856982383300898.md, tweet-2053386368160514542.md, tweet-2052352848059404408.md, tweet-2047837426010509796.md]
created: 2026-10-03
updated: 2026-10-18
---

# Local Agent Inference

## Definition (Stand 2026-09)

Gemeint ist der Betrieb von Coding-Agenten-Harnesses auf lokal gehosteten Modellen, privat und offline, ohne Tokenkosten und API-Schlüssel. Der gespeicherte Praxisartikel betont, dass das etwas anderes ist als Chat mit einem lokalen Modell. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)

## Warum Agenten anders belasten (Stand 2026-09)

- Der Verlauf wächst: Jede Runde liest Gesprächsverlauf, Befehle, Tool-Aufrufe und Ergebnisse erneut; nach zwanzig bis dreißig Runden belegt der Kontext oft mehr RAM als die Gewichte. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)
- Tool-Aufrufe sind exakt: Quantisierung kostet etwas Qualität, was im Chat genügt, bei strukturell exakten Aufrufen aber ohne Teilpunkte scheitert. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)
- Langsamkeit summiert sich: 20 Token/s wirken im Chat annehmbar, über eine Schleife von zwanzig Schritten nicht mehr; zusätzlich drücken Speicher und Hitze. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)

## Warum lokal (Stand 2026-09)

Genannte Gründe: Kundendaten unter Verträgen mit zugelassenen Verarbeitern, regulierte Bereiche wie Gesundheit, Recht und Finanzen, abgeschottete Umgebungen sowie hochvolumige, mechanische Arbeit, bei der der Preis pro Token dominiert. Meist gilt das nur teilweise, etwa für ein Repository oder einen Batch-Job. Zur Einordnung siehe [AI Sovereignty](AI%20Sovereignty.md). [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)

## Vier Stellschrauben und Speicherbandbreite (Stand 2026-09)

Wahl von Modell, Kompression, Laufzeit-Tuning und Kontextlänge hängen zusammen. Beispiel: Qwen3.6 35B-A3B hat 35 Milliarden Parameter, davon etwa 3 Milliarden aktiv, alle müssen aber resident sein; bei 8 Bit etwa 38 GB, in BF16 etwa 70 GB, bei 4 Bit noch etwa 20 GB, sodass eine 16-GB-Maschine es nie lädt. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)

Gleiche Bittiefe heißt nicht gleichen Qualitätsverlust: Quantisierungsbewusst trainierte Modelle (genannt: Gemma 4 E2B) halten bei 4 Bit mehr Genauigkeit als nachträglich komprimierte wie Liquid LFM2.5 2.6B. Die Erzeugungsgeschwindigkeit liegt grob bei Speicherbandbreite geteilt durch Gewichtsgröße; ein großer Unified-Memory-Pool kann trotz niedrigerer Bandbreite schneller sein als eine Karte, deren Modell überläuft. Konfigurationen aus Foren passen deshalb selten zur eigenen Maschine. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)

Werkzeug dafür: [Magnitude](../entities/Magnitude.md) profiliert die Hardware und wählt Modell und Einstellungen. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)

## Grenzen (Stand 2026-09)

Die Argumente stammen aus einem Praxisartikel eines Werkzeug-Werbenden; Messungen fehlen. [tweet-2095906342154424750](../sources/tweet-2095906342154424750.md)

## Konkretes NVIDIA-Serving-Kit (Stand 2026-09)

[Qwen NVIDIA Serving Kit](../entities/Qwen%20NVIDIA%20Serving%20Kit.md) dokumentiert Qwen3.8-27B mit EXL3-Quantisierung auf einer NVIDIA-Karte unter Windows/Linux, hardwarebasierte Kontextprofile, passende vorkompilierte Engine-Wheels und einen OpenAI-kompatiblen Endpunkt mit separat gestarteter Harness-Oberfläche. Die Anleitung verbindet damit Modellbetrieb mit Agententools, deren Ausführung weiterhin der Client übernehmen muss. [tweet-2097976305354518968](../sources/tweet-2097976305354518968.md)

Kontext, Vision und Quantisierung konkurrieren um VRAM; Tweet-Maximalangaben und unterschiedliche README-Profile sind keine universellen Hardwaregarantien. Die API bindet im gespeicherten Default an 0.0.0.0 ohne wirksamen API-Key, das Harness nur an Loopback. Optionale Cherry-Websuche nutzt externe Dienste, weshalb lokales Modellserving nicht allein einen vollständig offline arbeitenden Agenten beweist. Autorwerte und Installation wurden hier nicht reproduziert. [tweet-2097976305354518968](../sources/tweet-2097976305354518968.md)

## Mining-Hardware und eigener vLLM-Pfad (Stand 2026-08)

[CMP Unlocker](../entities/CMP%20Unlocker.md) ist ein separates Linux-Treiberprojekt für Rechenleistung und Speichergeometrie der CMP 170HX; Root, passende Kernel-/Treiberstände, unsignierte Module und Kühlung gehören zur gespeicherten Voraussetzung, nicht zu einem hier getesteten Setup. [tweet-2093095040281379187](../sources/tweet-2093095040281379187.md)

Der Autor berichtet 212 Token/s mit vLLM gegenüber knapp 70 mit stock llama.cpp und nennt 64GB sowie damals 1000 Dollar; Foto und Post beweisen keine allgemeine Preis-Leistungsführerschaft oder zuverlässigen Agentenbetrieb. [tweet-2092962836934705501](../sources/tweet-2092962836934705501.md)

[HyperQwen](../entities/HyperQwen.md) dokumentiert DFlash2/MTP, Requantisierung, getrennte Einzel-/Batchprofile und Kontextabwägungen; dies ist ein anderer Serving-Pfad als [Qwen NVIDIA Serving Kit](../entities/Qwen%20NVIDIA%20Serving%20Kit.md). Die historischen vLLM-0.27.1-Angaben und späteren README-Stände bleiben getrennt. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

## Edge-MoE-Laufzeit (Stand 2026-08)

[FreeToken](../entities/FreeToken.md) beschreibt eine andere Laufzeit als [Qwen NVIDIA Serving Kit](../entities/Qwen%20NVIDIA%20Serving%20Kit.md) und [HyperQwen](../entities/HyperQwen.md): CPU/GPU-Co-Ausführung, gestreamten Prefill, Expertencache und elastische Expert-/KV-Speicherverteilung. OpenAI-/Anthropic-kompatible APIs sollen Coding-Agenten anbinden; Geschwindigkeit und Hardwareeignung sind ungetestete Anbieterangaben. Das ist ein älterer, eigenständiger Ansatz und überschreibt keine neueren Konfigurationswerte anderer Laufzeiten. [tweet-2090856982383300898](../sources/tweet-2090856982383300898.md)

## Historische Idee: nur aktive MoE-Parameter auf der GPU (Stand 2026-05)

Jun Song formuliert den Wunsch, bei einem Mixture-of-Experts-Modell ausschließlich die jeweils aktiven Parameter statt aller Gewichte in den GPU-Speicher zu laden. Der Post liefert keine Implementierung und bezeichnet die Idee selbst als damals praktisch unmöglich. [tweet-2053386368160514542](../sources/tweet-2053386368160514542.md)

Die daraus abgeleiteten 100-fache Datacenter-Effizienz und ein 1T-Modell auf 32 GB VRAM sind spekulative Autorbehauptungen ohne Messung, Transferkosten oder vollständige Speicherbilanz. Sie begründen keine Hardwareempfehlung und ersetzen keine späteren Laufzeitkonfigurationen. [tweet-2053386368160514542](../sources/tweet-2053386368160514542.md)

## Mobiler Zugriff auf den Rechenhost (Stand 2026-05)

[Remote Agent Access](Remote%20Agent%20Access.md) beschreibt tmux für persistente Sitzungen, Termius als mobilen SSH-Client und Tailscale zur Geräteverbindung. Der zitierte Autor berichtet damit von Hermes-Benchmarks mit Qwen3.6-27B auf einem DGX Spark vom Handy aus. Das ergänzt die Bedienung eines laufenden Hosts; es ersetzt keine späteren Modell-/Serving-Konfigurationen und belegt weder Neustartfestigkeit noch Benchmarkwerte. [tweet-2052352848059404408](../sources/tweet-2052352848059404408.md)

## Lokale Worker unter einem Hauptagenten (Stand 2026-04)

Jun Song schlägt vor, [Codex](../entities/Codex.md) oder [Claude Code](../entities/Claude%20Code.md) einen Skill erstellen zu lassen, der den Hauptagenten auf Planung, präzise Delegation und Bewertung beschränkt und ein lokales LLM die Teilaufgaben ausführen lässt. Er begründet die detaillierten Aufträge mit geringerer Leistungsfähigkeit des lokalen Modells. Dies ist eine Rollen-Anweisung, keine mitgelieferte Tool-Anbindung oder fertige Skill-Datei. [tweet-2047837426010509796](../sources/tweet-2047837426010509796.md)

Die behauptete ausreichende Nutzung nach Wechsel vom 200-Dollar- zum 20-Dollar-Abo ist nicht gemessen. Der frühe Vorschlag ergänzt spätere konkrete Serving-Anleitungen; er ersetzt weder deren Hardwarebedingungen noch belegt er universelle Qualitäts- oder Kostenvorteile. [tweet-2047837426010509796](../sources/tweet-2047837426010509796.md)
