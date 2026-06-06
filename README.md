# grāmatr Gemini CLI Extension

> Real-time intelligent context engineering, in Gemini CLI.

## Install in 30 seconds

```
gemini extensions install https://github.com/gramatr/gemini-extension
```

That's it. Gemini CLI fetches this repo, registers `gramatr` as a remote MCP server pointed at `https://api.gramatr.com/mcp`, and runs OAuth on first connection — sign in with the same identity you use at [gramatr.com](https://gramatr.com). No API key, no manual config.

## What this gets you

Every prompt is pre-classified and loaded with an intelligence contract — behavioral directives, quality criteria, and relevant context from past work — before the model responds.

- **System-prompt collapse** — a structured contract replaces the tens of thousands of tokens of behavioral enforcement you'd otherwise hand-maintain
- **Semantic retrieval** — past decisions, preferences, and project state pulled in automatically
- **Consistent behavior** — the same directives and quality gates on every prompt, every session, every tool; each output gated with a recorded PASS/FAIL

## What this repo is

This repository is the **public, reviewable source** for the grāmatr Gemini CLI extension. It mirrors the files Gemini CLI reads at install time so a reviewer or user can audit the connector before installing.

- `gemini-extension.json` — the official Gemini CLI extension descriptor (remote MCP server via `httpUrl` at `https://api.gramatr.com/mcp`)
- `GEMINI.md` — context file the model sees on each session, instructing it to call `route_request` for the intelligence contract
- `LICENSE` — grāmatr License v1.0

The mirror is generated automatically from the [gramatr monorepo](https://github.com/gramatr/gramatr) release pipeline; do not open PRs against this repo directly.

## Learn more

- Product: <https://gramatr.com>
- Source (monorepo): <https://github.com/gramatr/gramatr>
- Gemini CLI extensions: <https://geminicli.com/extensions>

## Version

0.24.2
