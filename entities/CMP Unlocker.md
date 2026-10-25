---
tags: [tools, llm-training]
sources: [tweet-2093095040281379187.md, tweet-2092962836934705501.md]
created: 2026-10-10
updated: 2026-10-10
---

# CMP Unlocker

## Freischaltung und Voraussetzungen (Stand 2026-08; gespeicherte README)

[amoghmunikote/cmpunlocker](https://github.com/amoghmunikote/cmpunlocker) beschreibt Treiberpatches, die bei NVIDIA CMP 170HX mit GA100 die durch Firmware/OTP-Konfiguration beschränkte Rechenleistung und HBM2e-Speichergeometrie freischalten sollen. [tweet-2093095040281379187](../sources/tweet-2093095040281379187.md)

Die gespeicherte README verlangt x86-64-Linux, Root-Rechte, installierte nvidia-open-610.43.0x-Bibliotheken/Firmware, zum laufenden Kernel passende Header, Python 3 und beim ersten Installieren Netz für passende Modulquellen. [tweet-2093095040281379187](../sources/tweet-2093095040281379187.md)

Secure Boot soll laut README ausgeschaltet sein, weil die gepatchten Module unsigniert sind; der Post nennt ausdrücklich ausreichende Kühlung. [tweet-2093095040281379187](../sources/tweet-2093095040281379187.md)

Die gespeicherten Profilbefehle sind `sudo ./install.sh --profile=8gb` für 8GB→64GB, `--profile=10gb` für 10GB→40GB und `--profile=es` für ES→32GB; danach verlangt dieser Stand vollständiges Ausschalten und Neustart. [tweet-2093095040281379187](../sources/tweet-2093095040281379187.md)

Als erreichte Eigenschaften nennt die README volle SM-Leistung, Speichergeometrie, PCIe Gen 2, BAR1, JTAG, Profiling und Persistenz über gepatchte Module. Das sind Projektangaben, keine eigene Hardwareprüfung. [tweet-2093095040281379187](../sources/tweet-2093095040281379187.md)

## Inferenzbericht und Foto (Stand 2026-08)

bob_hw_store berichtet von 212 Token/s mit Qwen3.8-27B auf einer freigeschalteten CMP 170HX mit 64GB und nennt einen damaligen Kartenpreis von 1000 Dollar. [tweet-2092962836934705501](../sources/tweet-2092962836934705501.md)

Sein Originaltext schreibt stock llama.cpp knapp 70 Token/s und vLLM mit spekulativem Decoding beinahe das Dreifache zu; die gespeicherte AI-Bildbeschreibung verwechselt diese Zuordnung. [tweet-2092962836934705501](../sources/tweet-2092962836934705501.md)

Das tatsächlich gelesene Foto zeigt Kupferkühlkörper und einen großen Lüfter, belegt aber weder Speicherfreischaltung noch Geschwindigkeit oder Preis. [tweet-2092962836934705501](../sources/tweet-2092962836934705501.md)

Die Aussage „beste Leistung pro Dollar“ ist eine unbestätigte Autorenbewertung ohne vollständiges Vergleichsprotokoll; sie begründet keine allgemeine Kaufempfehlung. [tweet-2092962836934705501](../sources/tweet-2092962836934705501.md)

## Historische und aktuelle Anleitung trennen (Stand 2026-08; Online-Nachtrag 2026-10-10)

Der gespeicherte Stand nennt `sudo ./uninstall.sh --yes` und einen Kaltstart; die während der Triage am 2026-10-10 gelesene [aktuelle README](https://github.com/amoghmunikote/cmpunlocker) nennt dagegen `sudo ./remove.sh --yes`, Treiber 610.xx.xx+ und zusätzliche ECC-/VFIO-Funktionen. [tweet-2093095040281379187](../sources/tweet-2093095040281379187.md)

Der aktuelle Upstream führt in der gelesenen Profilübersicht 8GB→64GB und 10GB→40GB; das ES-Profil der gespeicherten Extraktion wird damit nicht als derzeit unterstützter Weg behauptet. [tweet-2093095040281379187](../sources/tweet-2093095040281379187.md)

Kein Treiberpatch, Flashen oder Inferenzlauf wurde hier ausgeführt; [Local Agent Inference](../concepts/Local%20Agent%20Inference.md) ist der passende Nutzungskontext, aber der Post allein belegt keine Agenten-Zuverlässigkeit. [tweet-2092962836934705501](../sources/tweet-2092962836934705501.md)
