---
tags: [agents, tools]
sources: [tweet-2098941338297458746.md]
created: 2026-10-08
updated: 2026-10-08
---

# Agentic Inbox

## Architektur (Stand 2026-09)

[Repository](https://github.com/cloudflare/agentic-inbox): E-Mail-Client auf Cloudflare Workers, Email Routing, Durable Objects mit SQLite und R2 für Anhänge. Der Agents-SDK-/Workers-AI-Agent kann lesen, suchen und Antworten vorbereiten. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

Neue E-Mails können automatische Antwortentwürfe auslösen; laut README verlangt Senden eine ausdrückliche Bestätigung. Systemprompt pro Mailbox und Agenten-Chatverlauf sind persistent. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

## Einrichtung und Zugriffsgrenze (Stand 2026-09)

Deployment allein genügt nicht: Domain, Cloudflare Access mit POLICY_AUD und TEAM_DOMAIN, Catch-all Email Routing, ausgehender send_email-Zugang und eine Mailbox müssen eingerichtet sein. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)

Die zentrale Access-Policy schützt alle Mailboxen gemeinsam. Wer diese Policy passiert, kann laut README auch über /mcp jede Mailbox mit mailboxId bedienen; getrennte Speicherung ist keine Autorisierung je Mailbox. Apache 2.0 und Cloudflare-Abhängigkeiten stehen neben der unbelegten pauschalen Gratis-Ersatzbehauptung des Tweets. [tweet-2098941338297458746](../sources/tweet-2098941338297458746.md)
