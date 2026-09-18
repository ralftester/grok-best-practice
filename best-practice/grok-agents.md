# Subagents and worktrees

Built-in types: `general-purpose`, `explore` (read/search, no shell/edits), `plan` (plan, no shell/edits). Custom: `.grok/agents/` and `~/.grok/agents/`.

Personas overlay behaviour. They are not extra capabilities.

Worktrees: `--worktree` / `-w`, `grok clone`, hooks `WorktreeCreate` / `WorktreeRemove`. Isolation is per worktree, not per marketing slide.

Workflows (`.rhai`) can fan out with a budget. `/create-workflow`, `/workflow`. Do not paste LifeJiggy YAML here. Grok will not load it.

Source: [Modes and commands](https://docs.x.ai/build/modes-and-commands), bundled `create-workflow` skill.
