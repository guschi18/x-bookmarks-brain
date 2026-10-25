---
tags: [product-building, agents]
sources: [tweet-2029146101715259900.md]
created: 2026-10-24
updated: 2026-10-24
---

# Dark Portfolio Landing Page Prompt

## Definition (Stand 2026-03)

Ein langer, spezifikationsartiger Prompt für eine einseitige dunkle Portfolio-Website mit React, Vite, Tailwind CSS, TypeScript, GSAP, Framer Motion und hls.js. Viktor Oddy gibt an, Opus 4.6 habe damit die animierte Seite in einem Durchgang erzeugt (Autorangabe, anhand eines Videos ohne Transkript nicht prüfbar). Den Prompt lieferte der Nutzer; der vollständige Wortlaut steht in der Quelle. [tweet-2029146101715259900](../sources/tweet-2029146101715259900.md)

## Aufbau des Prompts

Der Prompt ist nach dem Muster Design-System, dann Abschnitt für Abschnitt gegliedert. Er legt fest: Schriften (Inter für Text, Instrument Serif kursiv für Überschriften), Farben als HSL-Variablen (Hintergrund #0a0a0a, Fläche #141414, Text #f5f5f5, Muted #888888, Linie #1f1f1f), einen Akzentverlauf von #89AACC nach #4E85BF, drei eigene Keyframe-Animationen (scroll-down, role-fade-in, gradient-shift) und ein erzwungenes Dark Theme ohne Umschalter. [tweet-2029146101715259900](../sources/tweet-2029146101715259900.md)

Sieben Abschnitte: Ladebildschirm (Zähler 000-100 in 2.700 ms, rotierende Wörter), Hero mit HLS-Hintergrundvideo und schwebender Navigationspille, Selected Works als Bento-Grid mit vier Karten, Journal mit vier Pillen-Einträgen, Explorations als Parallax-Galerie mit GSAP ScrollTrigger und Lightbox, Stats mit drei Kennzahlen und Kontakt/Footer mit gespiegeltem Video und GSAP-Marquee. [tweet-2029146101715259900](../sources/tweet-2029146101715259900.md)

Jede Komponente nennt konkrete Tailwind-Klassen, Zeiten, Easings, Rotationsformeln und Beispieltexte; nötige Assets (je vier Projekt- und sechs Explorations-Bilder) und Abhängigkeiten (gsap, framer-motion, hls.js, react-router-dom, tailwindcss-animate) stehen am Ende. Die letzten Zeilen verlangen zusätzlich sanftes Scrollen in der Navigation und Seitenübergänge. [tweet-2029146101715259900](../sources/tweet-2029146101715259900.md)

## Grenzen

Im eingefügten Prompt fehlt der JSX-Block der Seitenstruktur; nur der Rest der Ladebildschirm-Zeile ist erkennbar. Die Demo-Texte (Name, Orte, Kennzahlen wie "20+ Years Experience") sind Platzhalter. Einordnung neben Skill-basierten Ansätzen: [Design Skills for Coding Agents](Design%20Skills%20for%20Coding%20Agents.md). [tweet-2029146101715259900](../sources/tweet-2029146101715259900.md)
