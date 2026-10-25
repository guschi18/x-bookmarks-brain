---
tags: [product-building, tools]
sources: [tweet-2021689840253968598.md]
created: 2026-10-24
updated: 2026-10-24
---

# WC3UI

## Zweck und Quelle (Stand 2026-02)

WC3UI ist laut dem gespeicherten banteg-Post und [Showcase](https://wc3ui.banteg.xyz/) eine thematisierbare Web-Komponentenbibliothek nach der Warcraft-III-Oberfläche. Human, Orc, Night Elf und Undead sind als vier Fraktionsthemen beschrieben. [tweet-2021689840253968598](../sources/tweet-2021689840253968598.md)

## Komponenten und Darstellung

Der zitierte Autor nennt elf Buttonvarianten, Menüs, Slider, Checkboxen, Radiobuttons, Eingabefelder, Scrollbars, Textareas und Listen. Dazu kommen Ressourcenanzeigen, ein Command-Card-Raster mit Hotkeys und Cooldowns, Tooltips mit Ressourcenkosten, Warteschlangen sowie Health-, Mana-, XP-, Fortschritts- und Ladebalken. [tweet-2021689840253968598](../sources/tweet-2021689840253968598.md)

Nach Autorangabe werden BLP-Texturen zur Laufzeit dekodiert und 9-Slice-Rahmen aus Sprite-Atlanten anhand von FDF-Maßen auf Canvas zusammengesetzt. Animierte Heldenporträts und die HUD-Uhr verwenden laut Post MDX-Modelle und WebGL. Das beschreibt den behaupteten Mechanismus, keine hier getestete Implementierung. [tweet-2021689840253968598](../sources/tweet-2021689840253968598.md)

Der Showcase nennt mehr als 60 überschreibbare Design-Tokens pro Fraktion, CSS Custom Properties, kombinierbare Tailwind-Klassen und Tree-Shaking für ESM. Er bewirbt außerdem Tastaturnavigation, ARIA-Labels, Reduced Motion und WCAG-AA-Kontrast; diese Zusagen sowie die beworbenen Bundlegrößen wurden nicht geprüft. [tweet-2021689840253968598](../sources/tweet-2021689840253968598.md)

## Evidenzgrenzen

Der zitierte Autor spricht von tatsächlichen Spieltexturen, während der Showcase behauptet, alle visuellen Assets seien neu erstellt. Die Herkunft ist damit widersprüchlich dokumentiert; eine Lizenzfreigabe für die Assets lässt sich daraus nicht ableiten. Der Showcase bezeichnet das Projekt als unabhängig von Blizzard. [tweet-2021689840253968598](../sources/tweet-2021689840253968598.md)

Die Bibliothek ergänzt die konkreten Komponentenressourcen auf [Design Skills for Coding Agents](../concepts/Design%20Skills%20for%20Coding%20Agents.md); ihr sehr spezifischer Spielstil ist keine allgemeine Designempfehlung. [tweet-2021689840253968598](../sources/tweet-2021689840253968598.md)
