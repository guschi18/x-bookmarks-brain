---
tags: [agents, tools]
sources: [tweet-2105710796198322659.md, tweet-2098354614856744978.md]
created: 2026-10-04
updated: 2026-10-08
---

# OpenDots

## Role and architecture (Stand 2026-10)

[OpenDots](https://github.com/CopilotKit/OpenDots) is an early self-hosted workspace template, not a hosted product: Spaces hold editable pages, while specialist Dots have roles, instructions and permitted tools. [tweet-2105710796198322659](../sources/tweet-2105710796198322659.md)

AG-UI carries messages, tools and state to CopilotKit components; TanStack AI handles model streaming/server tools, Intelligence provides durable Threads, and local metadata stores pages and work state separately. [tweet-2105710796198322659](../sources/tweet-2105710796198322659.md)

Optional per-Dot OpenBot computers expose persistent browser profiles, files, terminal, permissions and human takeover; the unconfigured template does not execute host commands. [tweet-2105710796198322659](../sources/tweet-2105710796198322659.md)

## Setup and work controls (Stand 2026-10)

Use Node.js 24: git clone https://github.com/CopilotKit/OpenDots.git, cd OpenDots, npm ci, cp .env.example .env, npm run dev; open http://127.0.0.1:5173 and configure conversation/model services. Calls and computers need separate providers/services. [tweet-2105710796198322659](../sources/tweet-2105710796198322659.md)

Human review cards can pause before saving a draft; approval creates an authorized Space page, and retries recover the same page. Realtime speech can continue alongside a separate compute agent sharing conversation context and permissions. [tweet-2105710796198322659](../sources/tweet-2105710796198322659.md)

## Verification and limits (Stand 2026-10)

The README reports local live checks for model/page chat, computer persistence and voice controls; Slack, spoken compute delegation and cloud learning/skill delivery still need connected-service verification. These are project reports, not independent checks. [tweet-2105710796198322659](../sources/tweet-2105710796198322659.md)

This is a single-owner starting point without shared editing, invitations, uploads, interactive embeds, multi-Dot group chat or automatic delegation. The tweet's broad enterprise-ready/any-harness claims exceed the documented verification. [tweet-2105710796198322659](../sources/tweet-2105710796198322659.md)

Public-web research uses Parallel by default and sends queries, URLs, a stable session identifier and the research objective; memories and complete conversations are not automatically forwarded, but objectives can carry context. A disabled provider is available. [tweet-2105710796198322659](../sources/tweet-2105710796198322659.md)

The saved native-video transcript is empty; the quoted OpenAI dots announcement does not establish feature parity. [tweet-2105710796198322659](../sources/tweet-2105710796198322659.md)

## Ergänzende Infrastrukturquelle (Stand 2026-09)

[OpenBot](OpenBot.md) beschreibt sein eigenes AG-UI-Agentensystem mit isolierten Computern, Policy-Gateway, Audit und Deployment. Seine gespeicherte README wird separat erfasst; ihre Konfiguration und Funktionsliste sind kein Nachweis gleicher Eigenschaften dieses OpenDots-Templates. [tweet-2098354614856744978](../sources/tweet-2098354614856744978.md)
