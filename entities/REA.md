---
tags: [agents, tools]
sources: [tweet-2108245653843509415.md, tweet-2112308732872819104.md, tweet-2114160336114954401.md]
created: 2026-10-12
updated: 2026-10-26
---

# REA

## Tool und Originalbild (Stand 2026-10)

Das am 12.10.2026 betrachtete gespeicherte Originalbild bezeichnet REA als „Reverse Engineer Anything“ und beschreibt einen MCP für Reverse Engineering von Binärdateien, Apps und Laufzeitverhalten. Sichtbarer Einstieg ist npx rea-agents setup; der Screenshot nennt npm v6.0.0, Node.js 22.19+ und MIT. [tweet-2108245653843509415](../sources/tweet-2108245653843509415.md)

Der Screenshot zeigt zugleich einen failing-CI-Badge. Trending-Platzierung und der Post „Software is done“ belegen weder stabile Analyse noch automatische vollständige Rekonstruktion. [tweet-2108245653843509415](../sources/tweet-2108245653843509415.md)

## Ergänzendes Repository (Recherche 2026-10-12)

Das beim Review gefundene [Opiuz/REA-Repository](https://github.com/Opiuz/REA) beschreibt CLI und [MCP](../concepts/Model%20Context%20Protocol.md) für native Binärdateien, JavaScript-/Electron-Apps, .NET-Assemblies und Websites. Analyse soll lokal erfolgen und Befunde samt Grenzen zurückgeben; dies sind ergänzende README-Angaben, nicht der gespeicherte Raw-Artikel. [tweet-2108245653843509415](../sources/tweet-2108245653843509415.md)

Die aktuelle README nennt macOS und Linux; Windows-Ghidra-Unterstützung ist als derzeit nicht verfügbar bezeichnet. Tiefe Binäranalyse braucht Hopper oder eine vorhandene Ghidra-Installation; Hopper hat eine eigene Lizenz. Setup zeigt Änderungen vor Freigabe und sichert vorhandene Konfiguration. Keine Installation oder Analyse wurde hier ausgeführt. [tweet-2108245653843509415](../sources/tweet-2108245653843509415.md)

## REA-Prompts-Sammlung (Stand 2026-10)

Das Repository JoasASantos/REA-Prompts (REAP) sammelt einfügbare Prompts für REA in 16 Kapiteln: Installation, Einstieg, Feature-Tracing, Binäranalyse, Software- und Feature-Nachbau, Spiele, WASM-Portierung, Firmware, Android, Kernel, Schwachstellenforschung, Electron und JavaScript, Schutzmechanismen, Versionsvergleich und lange Untersuchungen. Die README verweist auf rea.tools, die offizielle Prompt-Galerie madewithrea.com/prompts und einen Einführungs-Thread. [tweet-2112308732872819104](../sources/tweet-2112308732872819104.md)

Die README warnt, nur eigene oder ausdrücklich autorisierte Software zu analysieren; Kapitel zu Anti-Cheat, DMA, DRM, Kernel und Schwachstellen seien für Sicherheitsforschung, Interoperabilität, CTFs, Bug-Bounties und den Test eigener Software gedacht. Platzhalter stehen in spitzen Klammern; jede Anfrage soll ein Feature fokussieren. [tweet-2112308732872819104](../sources/tweet-2112308732872819104.md)

### Beispiel-Prompts (wörtlich aus der README)

Erste Übung, CSV-Export nachverfolgen:

> Download https://rea.tools/examples/notes-example.zip into a new folder and extract the contents. Use REA to investigate what happens when I click "Export notes". Trace the flow from the button to the file write. Show where notes.csv is created, which fields it contains, and the files and functions that prove each step. [tweet-2112308732872819104](../sources/tweet-2112308732872819104.md)

Ein Feature erklären, ohne die Anwendung auszuführen:

> Use REA to investigate how <FEATURE> works in <PATH TO APPLICATION>. Identify the entry point, the functions involved, the data flow, the dependencies and the observable effects. For every conclusion, present evidence: file, function, address or relevant snippet. Separate confirmed facts, inferences and points that remain unknown. Do not execute the application in this step. [tweet-2112308732872819104](../sources/tweet-2112308732872819104.md)

Clean-Room-Spezifikation statt Codekopie:

> Use REA to study <application> as a black box for a clean-room clone. Produce CLONE_SPEC.md covering: every user-visible feature, screen and state machine; inputs, outputs and edge cases; file formats and network protocols it uses; settings and persistence layout; error behaviors. For each requirement, cite the evidence (function, address, string, captured request). Mark anything unconfirmed as UNKNOWN. Do not copy code or assets - I will implement from the spec only. [tweet-2112308732872819104](../sources/tweet-2112308732872819104.md)

Nachbau prüfen:

> Compare <MY IMPLEMENTATION> with the observed behavior of <ORIGINAL APPLICATION>. Use verify_reconstruction, if available. Check results, errors, limits and state transitions. Present passing cases, divergences and behaviors not yet tested. Do not consider equivalence demonstrated just because a few examples passed. [tweet-2112308732872819104](../sources/tweet-2112308732872819104.md)

Evidenzgrenze: Die Prompts wurden hier nicht ausgeführt; ihre Wirksamkeit ist nicht belegt. Es handelt sich um die Sammlung eines Drittautors, nicht um offizielle REA-Dokumentation. [tweet-2112308732872819104](../sources/tweet-2112308732872819104.md)

## Alternative: leanrea (Stand 2026-10)

leanrea (github.com/aicodeking/leanrea) ist ein 8-KB-Skill, der dem Agenten sagt, welche CLI-Tools er je Zieltyp nutzt (asar, otool, nm, go version -m, jadx, apktool, tshark, sqlite3), statt eine MCP-Schicht mit 207 Tools zu laden. Die README berichtet im eigenen Benchmark (Sonnet 5.5, 4 Aufgaben x 3 Läufe) gegenüber REA 38 % weniger Laufzeit, 35 % geringere Kosten und 60 % weniger Tokens bei 74/75 gegen 75/75 Punkten. Die Autoren nennen nur 3 Läufe pro Zelle, ein Modell und einen Rechner; REA ist als Referenz im Bestfall mit Tool-Suche getestet. Vergleichszahlen eines Konkurrenzprojekts, nicht nachgemessen. [tweet-2114160336114954401](../sources/tweet-2114160336114954401.md)
