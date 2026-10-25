---
tags: [tools, llm-training, agents]
sources: [tweet-2092962838822150508.md]
created: 2026-10-10
updated: 2026-10-10
---

# HyperQwen

## Repository und historischer Einstieg (Stand 2026-08)

[syv-ai/qwen38-27b-rtx3090](https://github.com/syv-ai/qwen38-27b-rtx3090) und [syv-ai/HyperQwen](https://github.com/syv-ai/HyperQwen) sind die alte und die umbenannte Repository-Adresse desselben Projekts; die gespeicherten Titel und Texte nennen HyperQwen. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

Der Post vom 27.08.2026 nennt vLLM 0.27.1 plus Community-Patches für DFlash2 und Ampere-Karten. Das ist eine datierte Installationsangabe; die erwähnten exakten Localmaxxing-Run-Flags sind in diesem Bookmark nicht gespeichert. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

## Serving- und Kontextentscheidungen (Stand 2026-08; separate gespeicherte README-Stände)

Die beiden gespeicherten README-Extraktionen beschreiben Qwen3.8-27B auf einer 24GB-Karte mit Requantisierung, OpenAI-kompatibler API und Docker-Compose-Profilen single und batch. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

Die README unterscheidet Einzelgespräche und parallele API-Last: DFlash2 lohnt laut Autorenmessung bei wenigen Nutzern; bei hoher Parallelität kann einfaches Batching mehr Gesamtdurchsatz liefern. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

Die ausführlichere Auswahlhilfe verbindet Anfragezahl, Kontextlänge und Prompt-Wiederholung: normales Chatprofil mit 64k, Reproduktion mit `DFLASH_TOKENS=15`, langer Kontext über `SPEC=mtp CTX=long` und sehr langer Kontext über `CTX=huge`/KVarN. Die Ergebnisse gelten für die genannte Konfiguration, nicht pauschal für alle GPUs. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

Die zweite gespeicherte README nennt noch MTP als konservativen Default und empfiehlt für Einzelbenutzer `SPEC=dflash2` und `PREFIX_CACHE=1`; unterschiedliche Snapshots dürfen nicht zu einer einzigen historischen Default-Konfiguration vermischt werden. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

Autorwerte sind 127 Token/s für Einzelstream, etwa 1035 aggregierte Token/s bei 64 parallelen Anfragen und 381 Token/s bei Wiederholung aus dem Prompt; die README begrenzt die Kernmessungen auf eine RTX 3090 bei 250W. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

## Voraussetzungen, Messung und Grenzen (Stand 2026-08; gespeicherte README)

Der gespeicherte Docker-Einstieg lädt rund 9,5GB Image und bereitet einmalig etwa 20GB Modell vor; unter WSL2 nennt er `VLLM_WSL2_ENABLE_PIN_MEMORY=1` gegen einen UVA-Fehler. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

Die Portierung ist teilweise modell- und kartenabhängig: Attention-Geometrie, Draft-Vokabular und Drafter gehören zum Checkpoint; Tune-Tabellen stammen von sm86, sm80/CMP 170HX ist mit offenen Spekulationsfehlern beschrieben. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

Ein vergleichbarer Feldbericht soll Karte, Leistungsgrenze, Treiber, Betriebssystem/Container, Commit und Setup-Profil nennen; den ersten Benchmark nach Start soll man laut README verwerfen und den zweiten bewahren. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

Die gespeicherte zweite Extraktion überschreibt mit ihrer Schlüsselzeile `.env` statt sie zu ergänzen. Diese Zeile wird hier nicht als sichere aktuelle Installationsanweisung wiederholt. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

## Aktueller Upstream und Einordnung (Stand 2026-08; Online-Nachtrag 2026-10-10)

Die am 2026-10-10 während der Triage gelesene [README](https://github.com/syv-ai/HyperQwen) nennt einen vLLM-0.30.0-Pin und weiterhin offene sm80-Spekulationsprobleme; ältere vLLM-0.27.1-Anweisungen überschreiben diesen aktuellen Stand nicht. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

Der gespeicherte README-Stand warnt vor Bindung an 0.0.0.0 ohne Authentifizierung; die aktuelle README beschreibt Loopback als Default und bewusste Freigabe über API-Key und `BIND=0.0.0.0`. Dies sind zeitlich getrennte Angaben. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

HyperQwen ergänzt [Local Agent Inference](../concepts/Local%20Agent%20Inference.md) mit einem vLLM-Patch-/Serving-Pfad, während [Qwen NVIDIA Serving Kit](Qwen%20NVIDIA%20Serving%20Kit.md) einen separaten EXL3-Pfad beschreibt; die Quellen belegen keine getestete Austauschbarkeit. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)

Die gespeicherte README nennt Apache-2.0; Installation, Modellqualität und Leistungszahlen wurden hier nicht unabhängig reproduziert. [tweet-2092962838822150508](../sources/tweet-2092962838822150508.md)
