# Glossary

Short. How you’d explain it to someone new.

| Word | What it is | Why it exists |
|---|---|---|
| **Grok Build** | The `grok` program in a terminal. An agent that can read and change files. | Code and docs. **Not** grok.com chat. |
| **Grok Bot** | A different product (cloud computer in a browser). | Out of scope here. |
| **Agent** | A model with tools (read, write, run commands). | More than a chatbot. |
| **Harness** | The app the agent runs in: Grok Build, Claude Code, Codex, Cursor. | The same `SKILL.md` can load in several harnesses. |
| **Skill** | A folder with `SKILL.md`: what it does and when to pick it. | Repeatable instructions. You don’t paste them every time. |
| **Pack** | Many skills from one git repo. | One command: `npx skills add owner/repo`. |
| **Loadout** | The small daily set, not the whole internet. | [catalog/loadout.md](../catalog/loadout.md) |
| **Specialist** | An agent in this repo: `design`, `marketing`, `higgsfield`, `notion`. | One job, one type. The main chat stays in charge. |
| **AGENTS.md** | The contract for *every* agent in this repo. | Claude reads it through `CLAUDE.md` (an alias). |
| **Inspect** | A look around: skills, hooks, MCP, name collisions. | Grok: `grok inspect`. Others: list `skills/`. |
| **Plan Mode** | On Grok: plan first; file edits go through a gate. | Bash and child agents are **not** that same gate. |
| **Hook** | A script around a tool call (e.g. before a dangerous command). | On Grok, hooks are *fail-open*: a crash does not block the tool. |
| **MCP** | A plugin to another service (Notion, Higgsfield) in the same session. | The agent calls tools. You don’t commit tokens. |
| **Notion (here)** | The team shelf for skills. | Write a page → `npx skills add <url>` → the agent loads it. |
| **Higgsfield** | Image, video, ads, Soul faces. | Prompt in the agent; job on CLI/MCP. Don’t `curl` their API. |
| **`npx skills add`** | Installer from [skills.sh](https://skills.sh) / GitHub. | Writes files where the harness can see them. |
| **Name collision** | Two skills share a name. | Grok prefixes them. Inspect; don’t guess. |

A **pack** is other people’s instructions. **This git repo** is the map plus two of our skills. We don’t copy vendor trees here.
