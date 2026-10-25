---
tags: [llm-training, product-building]
sources: [tweet-2101250446329364542.md]
created: 2026-10-06
updated: 2026-10-06
---

# Small Model Fine-Tuning

## Ziel und Entscheidung (Stand 2026-09)

Der Leitfaden spezialisiert ein kleines Modell auf Startup-Brief zu belegtem Funding-Pitch-Text. Fine-Tuning soll Ton, Struktur, Fachsprache und Befolgung von Vorgaben verbessern; aktuelle Marktdaten gehören laut Autor in Retrieval. Vor Training werden Prompt-only und Prompt plus Retrieval als Baselines bewertet; erst ein konkreter verbleibender Fehler begründet Training. Das ergänzt [Model Selection Evals](Model%20Selection%20Evals.md). [tweet-2101250446329364542](../sources/tweet-2101250446329364542.md)

## Datenpipeline (Stand 2026-09)

1. Erlaubte Quellen in einer Allowlist erfassen; Herkunft, Rechte, Hash und Abrufzeit dokumentieren. Private PDFs, OCR-Entwürfe und Nutzerdaten bleiben getrennt vom öffentlichen Verarbeitungscode. [tweet-2101250446329364542](../sources/tweet-2101250446329364542.md)
2. Zuerst nativen PDF-Text extrahieren, bei Bedarf Layout-OCR und Zweitprüfung. Leere oder fehlgeschlagene Seiten bleiben im Prüfprotokoll. Maschinenentwurf und menschlich geprüfter Goldtext sind getrennte Felder. [tweet-2101250446329364542](../sources/tweet-2101250446329364542.md)
3. Extraktionsrauschen bereinigen, Zahlen nicht durch ein Sprachmodell korrigieren. Zahlenfolgen separat prüfen. [tweet-2101250446329364542](../sources/tweet-2101250446329364542.md)
4. Aus Belegen kuratierte Brief-zu-Text-Paare im messages-JSONL-Format erstellen; Zieltext auf erfundene Zahlen, Kunden und Traktion prüfen. Der Autor schlägt zunächst 200-500 geprüfte Beispiele vor. [tweet-2101250446329364542](../sources/tweet-2101250446329364542.md)
5. Train/Validation/Test nach Unternehmen statt PDF-Seiten teilen, damit eine Firma nicht in mehreren Splits auftaucht. Der vorgeschlagene Split ist 80/10/10; Dataset-Hash und Splitmanifest dokumentieren. [tweet-2101250446329364542](../sources/tweet-2101250446329364542.md)

## QLoRA-Versuch (Stand 2026-09)

Das konkrete Beispiel verwendet Qwen/Qwen2.5-1.5B-Instruct, 4-Bit-NF4 mit Double Quantization, LoRA auf all-linear und SFTTrainer. BF16 wird verwendet, wenn die GPU es unterstützt, sonst FP16. Verwendete Startwerte: r=16, alpha=32, dropout=0.05, learning_rate=2e-4, zwei Epochen, Batch 2, gradient_accumulation_steps=8 und max_length=2048; Packing und Gradient Checkpointing sind aktiviert. Dies sind Artikelparameter, keine hier getesteten optimalen Werte. [tweet-2101250446329364542](../sources/tweet-2101250446329364542.md)

Der vollständige Trainingscode steht in der Source. Für Colab empfiehlt der Leitfaden Checkpoints auf Drive alle 50 Schritte, einen Resume-Pfad und dokumentierte Python-, Torch-, Transformers-, TRL- und PEFT-Versionen. Colab-Verfügbarkeit und Laufzeit sind variabel; ein kleiner VPS dient in diesem Aufbau als Gateway, nicht als GPU-Trainingsmaschine. [tweet-2101250446329364542](../sources/tweet-2101250446329364542.md)

## Evaluation und Bereitstellung (Stand 2026-09)

Die Evaluation vergleicht Nützlichkeit, unbelegte Aussagen, Zahlenfehler, Wiederholungen, Formattreue, Latenz und Kosten auf ungesehenen Firmen mit denselben Baselines. Ein sinkender Trainingsloss ersetzt diesen Vergleich nicht; ein bereits für Entscheidungen genutztes Testset ist kein unangetasteter Abschluss-Test mehr. [tweet-2101250446329364542](../sources/tweet-2101250446329364542.md)

Der Leitfaden nennt vLLM mit LoRA-Adapter für Durchsatz oder FastAPI plus Transformers für wenig Traffic. HTTPS, Auth, Rate Limits und Queueing liegen vor dem GPU-Server. Modell- und Adapterversion, Fehler, Queue-Zeit und GPU-Nutzung werden protokolliert; neue Trainingsversionen brauchen geprüfte Beispiele, Evaluation und ein Rollback-Artefakt. [tweet-2101250446329364542](../sources/tweet-2101250446329364542.md)

## Grenzen (Stand 2026-09)

Der Artikel behauptet, kleine Modelle könnten generisch gepromptete Frontier-Modelle auf engen Aufgaben übertreffen, liefert dafür aber keinen replizierten Vergleich. Seine Beispiel-Evalzahlen und Kostenrechnungen sind keine eigenen Messergebnisse. Der FastAPI-Abschnitt enthält einen Platzhalter statt vollständiger Modellinferenz; die Anleitung ist als Arbeitsablauf nützlich, aber hier weder ausgeführt noch als vollständig lauffähige Anwendung bestätigt. Der Mark-Cuban-Ausschnitt spricht allgemein über AI-Integration und belegt keine konkrete Jobgarantie für Fine-Tuning. [tweet-2101250446329364542](../sources/tweet-2101250446329364542.md)
