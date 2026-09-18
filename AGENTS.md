# AGENTS.md

Contract for every coding agent in this repo (Grok Build, Claude Code, Codex, Cursor).

Unofficial playbook. In scope: xAI Grok Build CLI (`grok`). **Not** Grok Bot, **not** grok.com chat.

English `README.md` is the homepage. Polish `README.pl.md` is the same course and the same sections — not a shorter translation.

For humans: `docs/README.md` (when-to-use, recipes, glossary, help). Pack list: `catalog/library.md`.

`CLAUDE.md` is an alias of this file. Do not fork rules there.

## Discovery

| You are | First move |
|---|---|
| Grok Build | `grok inspect` (add `--json` if you need a dump) |
| Claude Code | Read this file. List `skills/` and `.claude/skills/` |
| Codex | Read this file. List `skills/` and `.agents/skills/` |
| Cursor / other | Read this file. List `skills/` |

Then skill `inspect-and-ship`. Do not edit yet.

Canonical skills live in `skills/`. `.grok/skills`, `.claude/skills`, and `.agents/skills` are thin links to that folder.

## Loadout

Install packs with `npx skills add`. Table: `catalog/loadout.md`. Do not dump 292 skills into the project.

Spawn **one** specialist per job: `design` · `marketing` · `higgsfield` · `notion` (`.grok/agents/`). Parent stays orchestrator.

## Notion

Prefer Notion MCP for workspace pages. Author a skill as a Notion page, then `npx skills add <notion-url>` or `npx skills add notion`. Notion is the shared library; this repo’s agents are runners.

## Hard rules

- Live Shields for stars. Never invent counts.
- No generated YAML agents, no LifeJiggy `GROK.md`, no secrets, no session dumps.
- **Grok Build:** `allowed-tools` in SKILL.md does not restrict tools. Hooks fail-open (`/hooks-trust`). Plan Mode gates file edits on the plan, not bash.
- **Claude Code:** `allowed-tools` is enforced. Do not assume Grok semantics.
