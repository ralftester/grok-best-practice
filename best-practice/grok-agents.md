# Subagents

Built-in types: `general-purpose`, `explore`, `plan`. Custom agents: `.grok/agents/` and `~/.grok/agents/`.

This playbook ships four:

| Agent | File | Job |
|---|---|---|
| `design` | [design.md](../.grok/agents/design.md) | UI, polish, anti-slop |
| `marketing` | [marketing.md](../.grok/agents/marketing.md) | Copy, CRO, SEO, launch |
| `higgsfield` | [higgsfield.md](../.grok/agents/higgsfield.md) | Image/video/ads |
| `notion` | [notion.md](../.grok/agents/notion.md) | Notion MCP + skills library |

Spawn **one**. Parent orchestrates. Packs they expect: [catalog/loadout.md](../catalog/loadout.md).

Personas overlay tone. They are not extra tools.

Worktrees: `--worktree` / `-w`. Workflows are `.rhai`, not YAML.

Source: [Modes and commands](https://docs.x.ai/build/modes-and-commands).
