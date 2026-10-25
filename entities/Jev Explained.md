---
tags: [agents, tools]
sources: [tweet-2101484241762603363.md]
created: 2026-10-03
updated: 2026-10-03
---

# Jev Explained

## Lernartefakt (Stand 2026-09)

https://github.com/davila7/jev-explained zeigt laut README [Jev](Jev.md) als typisierte Entscheidung statt Textgenerierung; die Live-Demo liegt auf https://jev-explained-repo.vercel.app/. Vier Beispiele sind Spamklassifikation, NVIDIA-Marktsnapshot, Tool-Call-Guardrail und Inbox-Triage. [tweet-2101484241762603363](../sources/tweet-2101484241762603363.md)

## Ablauf (Stand 2026-09)

Noul liefert eine Ja/Nein-Wahrscheinlichkeit, Choice eine Wahl mit Optionsverteilung und Konfidenz, Score einen gewichteten Wert auf einer geordneten Rubrik. Fragen gegen denselben State werden gebündelt, die decide()-Funktion wendet anschließend Policy im Code an; siehe [Typed Decision Layer](../concepts/Typed%20Decision%20Layer.md). Die Oberfläche zeigt Request, Latenz, Tokenverbrauch, Antworten und resultierende Entscheidung. [tweet-2101484241762603363](../sources/tweet-2101484241762603363.md)

Neue Beispiele werden in EXAMPLES mit State, questions, Sample-Zuständen und decide() ergänzt. Der Autor empfiehlt, das Repo in [Claude Code](Claude%20Code.md) oder [Codex](Codex.md) als Kontext zu verwenden und ein eigenes Beispiel hinzuzufügen. [tweet-2101484241762603363](../sources/tweet-2101484241762603363.md)

## Provider und Grenzen (Stand 2026-09)

Die README nennt die native TypeSafe-Schnittstelle und Vercels /typesafe/v1/systemone-Pfad. Keys liegen pro Provider im Browser-localStorage und werden über einen Serverproxy weitergeleitet, laut README ohne serverseitige Persistenz. MIT-Lizenz, etwa 100 ms und kalibrierte Antworten sind Repo-Angaben; kein Lauf und keine Finanzentscheidung wurden geprüft. Das NVIDIA-Beispiel ist eine Demo, kein Anlageergebnis. [tweet-2101484241762603363](../sources/tweet-2101484241762603363.md)
