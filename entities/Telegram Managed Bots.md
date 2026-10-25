---
tags: [agents, tools, product-building]
sources: [tweet-2048139791737164141.md]
created: 2026-10-16
updated: 2026-10-16
---

# Telegram Managed Bots

## Dokumentierte Funktion (Stand 2026-04; gespeicherte Doku separat geprüft 2026-10-16)

[Telegrams Bot-Dokumentation](https://core.telegram.org/bots/features#managed-bots) beschreibt Bots, die im Auftrag ihrer Eigentümer weitere Bots erstellen und verwalten. Ein bestehender Drittanbieter-Bot oder ein eigener Bot kann diese Managerrolle übernehmen; dies ist Infrastruktur für eigene Agenten und andere Bot-Anwendungen. [tweet-2048139791737164141](../sources/tweet-2048139791737164141.md)

## Ablauf

1. Eigenen Bot über BotFather auswählen oder erstellen und in der BotFather-MiniApp Bot Management Mode aktivieren. [tweet-2048139791737164141](../sources/tweet-2048139791737164141.md)
2. Nutzer öffnen https://t.me/newbot/{manager_bot_username}/{new_username}?name={new_name} und bestätigen den vorgeschlagenen Namen und Benutzernamen. [tweet-2048139791737164141](../sources/tweet-2048139791737164141.md)
3. Der Manager erhält ein managed_bot-Update mit ManagedBotUpdated. getManagedBotToken liefert den Zugangstoken; replaceManagedBotToken widerruft und ersetzt ihn. [tweet-2048139791737164141](../sources/tweet-2048139791737164141.md)
4. getManagedBotAccessSettings und setManagedBotAccessSettings lesen beziehungsweise ändern Zugriffsregeln. Der Manager kann anschließend über die Bot API Nachrichten, Profil und Einstellungen des neuen Bots verwalten. [tweet-2048139791737164141](../sources/tweet-2048139791737164141.md)

## Abgrenzung und Evidenzgrenze

Der Tweet behauptet, ein offizieller Lobster-Father-Bot programmiere und starte beliebige Agenten allein aus einem Prompt. Die gespeicherte Primärdoku belegt den Management-Ablauf, aber weder diese offizielle Produktidentität noch universelle No-Code-Programmierung. Die kurze Videoanlage ist ein Film-Meme ohne technische Zusatzanleitung; ein eigener Bot wurde hier nicht eingerichtet. [tweet-2048139791737164141](../sources/tweet-2048139791737164141.md)
