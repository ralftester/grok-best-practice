# Skills

A Grok skill is a folder with `SKILL.md` plus optional `scripts/` and `references/`.

Discovery (highest first): `./.grok/skills/`, repo `.grok/skills/`, `~/.grok/skills/`, plugin `skills/`, `[skills] paths`, then Claude/Cursor/Agents compat dirs.

Frontmatter Grok actually uses: `name`, `description`, `when-to-use`, `paths`, `argument-hint`, `user-invocable`, `disable-model-invocation`.

## Caveats (not Claude)

- `allowed-tools` **does not grant or restrict tools**.
- `model` and `effort` in the skill are accepted and ignored.
- Body cap is about 25k tokens.
- Colliding names get a prefix. Built-ins keep the bare slash.

Create with `/create-skill` (user guide). Some landing copy still says `/skillify`. Same idea, two names.

Install someone else’s pack only when they document a Grok path. Daily set: [catalog/loadout.md](../catalog/loadout.md).

```bash
grok plugin install superpowers@xai-official --trust
npx skills add higgsfield-ai/skills
npx skills add coreyhaines31/marketingskills
npx skills add pbakaus/impeccable
npx skills add notion
```

This repo’s own skills live in `skills/` (see [skills/README.md](../skills/README.md)) and are linked into `.grok/skills/`, `.claude/skills/`, and `.agents/skills/`. Packs stay pointers in [catalog/loadout.md](../catalog/loadout.md).

Sources: [Skills, plugins, marketplaces](https://docs.x.ai/build/features/skills-plugins-marketplaces), [xai-org/grok-build](https://github.com/xai-org/grok-build).
