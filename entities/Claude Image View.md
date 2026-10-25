---
tags: [agents, tools]
sources: [tweet-2106153410697564235.md]
created: 2026-10-04
updated: 2026-10-04
---

# Claude Image View

## Behavior and installation (Stand 2026-10)

[Claude Image View](https://github.com/jarrodwatts/claude-image-view) is a [Claude Code](Claude%20Code.md) mod with numbered thumbnails above the input; previews preserve aspect ratio and clear after sending or deleting tags. [tweet-2106153410697564235](../sources/tweet-2106153410697564235.md)

Install: /plugin marketplace add jarrodwatts/claude-image-view, /plugin install image-view, then /reload-plugins. [tweet-2106153410697564235](../sources/tweet-2106153410697564235.md)

## Requirements and implementation (Stand 2026-10)

The README requires Claude Code v2.1.287+, macOS/Linux and kitty graphics (for example Ghostty or kitty). Other terminals show tags, Desktop already has previews, and Windows compatibility is not documented. [tweet-2106153410697564235](../sources/tweet-2106153410697564235.md)

The mod polls the input every 200 ms and reads the local session image cache and PNG headers; the README says it makes no network requests and writes no files. [tweet-2106153410697564235](../sources/tweet-2106153410697564235.md)

For background sessions the README suggests CLAUDE_CODE_FORCE_TERMINAL_IMAGES=1 in the settings env block and a new session; this was not tested here. [tweet-2106153410697564235](../sources/tweet-2106153410697564235.md)

The demo transcript is empty; recorded properties come from the stored README. [tweet-2106153410697564235](../sources/tweet-2106153410697564235.md)
