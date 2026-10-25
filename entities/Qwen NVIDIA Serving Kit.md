---
tags: [tools, llm-training, agents]
sources: [tweet-2097976305354518968.md]
created: 2026-10-09
updated: 2026-10-09
---

# Qwen NVIDIA Serving Kit

## Projekt und Voraussetzungen (Stand 2026-09)

[MiaAI-Lab/Qwen3.8-27B-16gb-NVIDIA-GPUs-one-click-install](https://github.com/MiaAI-Lab/Qwen3.8-27B-16gb-NVIDIA-GPUs-one-click-install) ist laut README ein Windows-/Linux-Serving-Kit für Qwen3.8-27B in EXL3-Quantisierungen. Es richtet eine eigene Python-Umgebung ein, lädt passende Gewichte, startet einen OpenAI-kompatiblen Endpunkt und optional ein Harness. Der Autor nennt es experimentell mit begrenzter GPU-Testabdeckung. [tweet-2097976305354518968](../sources/tweet-2097976305354518968.md)

Die gespeicherte README verlangt NVIDIA ab Compute Capability 7.5 mit mindestens 12 GB VRAM, Treiber 570+, 64-Bit-Python 3.11+ und für das aktuelle Harness Node 22.19+. Gewichte benötigen je Quantisierung 9,7 bis 22,9 GB plus Python/PyTorch; ohne Node soll die API weiterlaufen, das Harness aber fehlen. Dateien bleiben im Kit-Verzeichnis, Administratorrechte werden nicht verlangt. [tweet-2097976305354518968](../sources/tweet-2097976305354518968.md)

## Einrichtung und Alltag (Stand 2026-09)

Windows: `windows\START-HERE.bat` installiert und startet über eine Browser-Einrichtung; `--no-start` lädt nur herunter. Danach startet `windows\start.bat` ausschließlich vorhandene Modelle. Linux: `./linux/setup.sh` installiert und stoppt danach; `./linux/start.sh` startet Server und optional Harness, `-b` läuft im Hintergrund. Downloads sind laut README resumierbar. Die Plattformabläufe sind somit ähnlich, aber nicht identisch. [tweet-2097976305354518968](../sources/tweet-2097976305354518968.md)

`windows\simplex.bat doctor` beziehungsweise `./linux/simplex doctor` prüft Umgebung, Treiber, Ports, Gewichte und freien Speicher. Die Windows-VRAM-Prüfung warnt vor stiller Auslagerung in System-RAM und starkem Tempoverlust; Linux hat diese Vorabprüfung laut README nicht. [tweet-2097976305354518968](../sources/tweet-2097976305354518968.md)

## Quantisierung, Kontext und Vision (Stand 2026-09)

Der Profilplaner ermittelt VRAM über nvidia-smi, lässt eine Reserve und bietet passende Gewichte/Kontextwerte an. 2,0 bpw stammt von [Mia-AiLab/Qwen3.8-27B-EXL3-2.0bpw](https://huggingface.co/Mia-AiLab/Qwen3.8-27B-EXL3-2.0bpw); höhere Profile aus [turboderp/Qwen3.8-27B-exl3](https://huggingface.co/turboderp/Qwen3.8-27B-exl3) werden per Revision gewählt. Die README-Tabelle nennt für 16 GB unter anderem 3,0 bpw mit rund 118k und Vision, 2,5 bpw mit rund 176k und Vision sowie 2,0 bpw mit rund 229k. Das sind Autorwerte und keine hier reproduzierten Hardwaremessungen. [tweet-2097976305354518968](../sources/tweet-2097976305354518968.md)

Die pauschale Tweet-Angabe bis 253k und die unterschiedlichen README-Baselines sind keine Garantie für dieselbe 16-GB-Konfiguration. Der Profilplaner schreibt int4-KV-Cache; die ältere .env.example-Baseline mit 2,0 bpw nennt 199936 Kontext und 8,4-Cache. Vision kostet zusätzlichen Speicher und fällt bei Platzmangel auf Text zurück. Der Abschnitt zur Default-Wahl widerspricht bei 3,0 bpw teilweise der Vision-Tabelle; konkrete Ergebnisse gehören an die jeweilige Hardware und Konfiguration. [tweet-2097976305354518968](../sources/tweet-2097976305354518968.md)

## Engine und Clients (Stand 2026-09)

Das Kit verlangt laut gespeichertem Stand ExLlamaV3 1.4.4. Es bevorzugt passende vorkompilierte Wheels nach Python, Torch und CUDA-Linie; wenn keines passt, wird kompiliert. Standard-API ist `http://127.0.0.1:8888/v1`, der Dummy-Key local wird ignoriert. Tool-Aufrufe werden aus Qwen-XML in tool_calls übersetzt; der Client muss die Funktion selbst ausführen und das Ergebnis zurückgeben. [tweet-2097976305354518968](../sources/tweet-2097976305354518968.md)

DeepSeek Harness läuft separat auf Port 3080 und wird anhand der tatsächlich geladenen Modellfähigkeiten konfiguriert. Seine Browser-Authentifizierung und Loopback-Bindung sind von der API getrennt: deren gespeicherter Default `HOST=0.0.0.0` exponiert /v1 im Netz, `HOST=127.0.0.1` begrenzt sie auf den Rechner. Cherry Studio ist optional und standardmäßig aus; dessen Websuche kann externe Dienste nutzen, daher ist der komplette optionale Agentenworkflow nicht automatisch offline. [tweet-2097976305354518968](../sources/tweet-2097976305354518968.md)

## Einordnung (Stand 2026-09)

Das Kit ist eine konkrete Ressource für [Local Agent Inference](../concepts/Local%20Agent%20Inference.md) neben [Magnitude](Magnitude.md); es beschreibt einen fest benannten Qwen-/EXL3-Pfad statt eines Belegs für beliebige Modellkompatibilität. Modellqualität, Kontextgrenzen, Werkzeugtreue und Installation wurden hier nicht geprüft. Kit-Skripte sind laut README MIT, die Modelllizenz Apache 2.0. [tweet-2097976305354518968](../sources/tweet-2097976305354518968.md)
