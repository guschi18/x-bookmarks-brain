---
tags: [agents, tools]
sources: [tweet-2106039761320518126.md]
created: 2026-10-04
updated: 2026-10-04
---

# Answer Me With HTML

## Mechanism (Stand 2026-10)

[Answer Me With HTML](https://github.com/QingYunA/answer-me-with-html) combines an agent skill with a bundled Node CLI: the model writes short Markdown, while code handles panels, themes and diagram layout. This implements [HTML as LLM Output](../concepts/HTML%20as%20LLM%20Output.md) with less generated markup. [tweet-2106039761320518126](../sources/tweet-2106039761320518126.md)

Components include flows, sequences, trees, timelines, limits, annotations and tables. Pages embed their Markdown, work offline and support blueprint/shadcn themes and light/dark mode. [tweet-2106039761320518126](../sources/tweet-2106039761320518126.md)

## Installation and controls (Stand 2026-10)

The README requires Node 20+ and offers npx skills add QingYunA/answer-me-with-html or Claude marketplace/plugin installation. The bundled skill needs no npm install for normal use. [tweet-2106039761320518126](../sources/tweet-2106039761320518126.md)

The CLI supports render, lint, list, config and per-component help; browser opening can be disabled, and style checking can warn or refuse rendering. Optional always-on mode adds pages to routine conclusions, without opening them. [tweet-2106039761320518126](../sources/tweet-2106039761320518126.md)

## Benchmark and limits (Stand 2026-10)

The author's three-topic, three-run Sonnet 5.5 benchmark reports medians of 6,873 versus 923 output tokens and 46 versus 13 seconds, but $0.22 versus $0.26 per answer: extra skill/CLI turns re-read context. Faster output is not evidence of lower total cost. The benchmark was not reproduced here. [tweet-2106039761320518126](../sources/tweet-2106039761320518126.md)

Requested videos add narration beats, stepwise diagrams and camera focus. Voice uses ElevenLabs when configured, otherwise system TTS or captions; MP4 export requires Chrome, ffmpeg and Node 22+. Platform-specific voice examples use macOS, not a verified Windows setup. [tweet-2106039761320518126](../sources/tweet-2106039761320518126.md)

The writing checks adapt [Simplified Technical English](Simplified%20Technical%20English.md) and support English/Chinese; they are not certification of official ASD-STE100 compliance. The saved demo transcript contains only Bye!. [tweet-2106039761320518126](../sources/tweet-2106039761320518126.md)
