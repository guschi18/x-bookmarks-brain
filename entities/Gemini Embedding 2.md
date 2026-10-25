---
tags: [llm-training, research, tools]
sources: [tweet-2047003304937332860.md]
created: 2026-10-18
updated: 2026-10-18
---

# Gemini Embedding 2

## Gemeinsamer Suchraum (Stand 2026-04)

Der gespeicherte Post beschreibt einen gemeinsamen Vektorraum für Text, Bild, Video, natives Audio und PDF. Als Anwendungen nennt er Textsuche über Videos, kombinierte Produkttext-/Bildsuche und Podcast-Indexierung ohne vorgeschaltete Transkription. Der zitierte Google-AI-Developers-Post kündigt allgemeine Verfügbarkeit in Gemini API und Vertex AI an. [tweet-2047003304937332860](../sources/tweet-2047003304937332860.md)

## Dimensionen und Zahlen im Originalpost (Stand 2026-04)

Der Autor nennt 3.072 Dimensionen, Video bis zwei Minuten und Matryoshka Representation Learning zur Reduktion auf 768 Dimensionen. Daraus leitet er vierfach weniger Vektorspeicher ab; die absolute Aussage ohne Qualitätsverlust und die pauschale Ablösung ganzer Mehrmodell-Pipelines sind keine hier gemessenen Eigenschaften. [tweet-2047003304937332860](../sources/tweet-2047003304937332860.md)

68,32 MTEB English, 68,8 Video-Retrieval gegenüber 60 für Amazon Nova 2 sowie 70 Prozent weniger Latenz bei Sparkonomy sind berichtete Vergleichswerte ohne gespeicherte Testkonfiguration. Die 0,20 Dollar pro Million Token beziehungsweise 0,10 Dollar im Batch und das 50-Dollar-Beispiel für 500 Millionen Token sind historische Angaben; das Rechenbeispiel setzt den genannten Batchpreis voraus. [tweet-2047003304937332860](../sources/tweet-2047003304937332860.md)

## Separater Dokumentationsabgleich (geprüft 2026-10-18)

Die zusätzlich gelesene [Google-Dokumentation](https://ai.google.dev/gemini-api/docs/embeddings) bestätigt den gemeinsamen multimodalen Raum und konfigurierbare Ausgabedimensionen. Sie beschreibt bei kleineren Vektoren eine Speicher-/Qualitätsabwägung und empfiehlt 768, 1.536 oder 3.072 Dimensionen; daraus folgt keine universelle Verlustfreiheitsgarantie für jeden Datensatz. Das ist ein späterer Nachtrag, kein in Raw gespeicherter April-Artikel. [tweet-2047003304937332860](../sources/tweet-2047003304937332860.md)

Die Dokumentation nennt Video bis 120 Sekunden mit höchstens 32 Frames und ohne Verarbeitung der Tonspur im Videofile; Audio ist ein eigener Eingabetyp. Die eigentliche Suchanwendung muss Inhalte daher passend aufteilen und indexieren; der Post allein belegt keine fertige Suche über tausende Stunden Aufzeichnung. Leistung, Preise und konkrete RAG-Integration wurden hier nicht getestet. [tweet-2047003304937332860](../sources/tweet-2047003304937332860.md)
