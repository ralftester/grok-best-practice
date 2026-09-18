# Plugins and marketplaces

A plugin bundles skills, agents, hooks, MCP, sometimes LSP.

Load from `./.grok/plugins/`, `~/.grok/plugins/`, marketplace cache, `[plugins] paths`, `--plugin-dir`.

TUI: `/plugins`, `/hooks`, `/skills`, `/mcps`, `/marketplace`.

Official example that is real on Grok:

```bash
grok plugin install superpowers@xai-official --trust
```

Self-host from git via `[[marketplace.sources]]`. This is not the Grok Bot `.grok-plugin` Cursor format.

Source: [Skills, plugins, marketplaces](https://docs.x.ai/build/features/skills-plugins-marketplaces).
