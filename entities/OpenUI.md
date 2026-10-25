---
tags: [agents, tools, product-building]
sources: [tweet-2098624943218913364.md]
created: 2026-10-08
updated: 2026-10-08
---

# OpenUI

## Rolle und Ablauf (Stand 2026-09)

[thesysdev/openui](https://github.com/thesysdev/openui) beschreibt ein Generative-UI-Framework: Eine erlaubte Komponentenbibliothek erzeugt Modellinstruktionen, das Modell streamt OpenUI Lang, ein Parser/Renderer baut daraus die Oberfläche. Komponenten-Props werden mit Zod-Schemas definiert; die Beschränkung auf registrierte Komponenten ist eine dokumentierte Renderingregel, kein hier geprüfter Sicherheitsnachweis. [tweet-2098624943218913364](../sources/tweet-2098624943218913364.md)

Die gespeicherte README nennt Tabellen, Diagramme, Formulare und Layouts sowie ein frameworkunabhängiges lang-core-Paket. React hat Rendering-, Headless-Chat-, UI- und Email-Pakete; weitere Pakete betreffen Vue, Svelte, Browser-Bundle und LangChain/LangGraph über AG-UI. [tweet-2098624943218913364](../sources/tweet-2098624943218913364.md)

## Einstieg und Entwicklungs-Skill (Stand 2026-09)

Der dokumentierte Quickstart ist `npx @openuidev/cli@latest create --name genui-chat-app`, dann ins Projekt wechseln, einen Modell-Key in .env setzen und `npm run dev` ausführen. Für bestehende React-Apps nennt die README `npm install @openuidev/react-lang @openuidev/react-ui`. [Dokumentation](https://openui.com/) und [Playground](https://www.openui.com/playground) ergänzen die Beispiele. [tweet-2098624943218913364](../sources/tweet-2098624943218913364.md)

Der Entwicklungs-Skill liegt unter [thesysdev/skills](https://github.com/thesysdev/skills/tree/main/skills/openui); Installation laut README: `npx skills add thesysdev/skills --skill openui`. Er behandelt Bibliotheksdesign, Sprache, Promptgenerierung, Renderer und fehlerhafte Modellausgaben. [tweet-2098624943218913364](../sources/tweet-2098624943218913364.md)

## Messung und Grenzen (Stand 2026-09)

Der Projektbenchmark vergleicht sieben UI-Szenarien mit zwei JSON-Formaten und tiktoken/GPT-5-Encoder: maximal 67,1 Prozent weniger Token gegenüber Vercel beim Kontaktformular, insgesamt 52,8 Prozent gegenüber Vercel und 51,7 Prozent gegenüber C1. Das erklärt die Werbeaussage bis zu 67 Prozent; weder allgemeine Antwortqualität noch Produktionskosten wurden hier gemessen. [tweet-2098624943218913364](../sources/tweet-2098624943218913364.md)

Paket- und Funktionsangaben beschreiben die gespeicherte README zum September-Bookmark, keinen eingefrorenen Release oder lokal getesteten Aufbau. [tweet-2098624943218913364](../sources/tweet-2098624943218913364.md)
