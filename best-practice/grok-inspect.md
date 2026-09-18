# grok inspect

`grok inspect` is the discovery dump Claude Code does not have. Run it before you invent a path.

```bash
grok inspect
grok inspect --json
```

It reports, from the current directory:

- config sources (`~/.grok/config.toml`, project files)
- instruction files and a token count (`AGENTS.md`, `CLAUDE.md`, `.grok/rules/`)
- skills (project / user / bundled / plugin) plus collisions and invocable names
- plugins, hooks, MCP origin
- sandbox, status line, Claude/Cursor/Codex compatibility flags

If a skill “does not start”, inspect first. Qualified names (`/local:commit` vs `/user:commit`) show up here.

Source: [docs.x.ai/build](https://docs.x.ai/build/overview), `grok --help`.
