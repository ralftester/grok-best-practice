# Contributing

English `README.md` is the source of truth. Polish `README.pl.md` is a condensed translation, not a dump.

## We merge if

1. It is about **Grok Build** (`grok` CLI from xAI), not Grok Bot and not grok.com chat.
2. The link resolves and the repo is not empty or archived.
3. Claims are sourced (docs.x.ai, xai-org/grok-build, or a dated GitHub API snapshot).
4. You did not invent star counts.
5. Skills use Grok frontmatter (`name`, `description`). No `GROK.md` factories.

## Format

Catalog row:

```
- [name](url) — one line, what it does, not why it is great.
```

Put Grok-native install commands when they exist:

```
grok plugin install superpowers@xai-official --trust
```

## Do not send

- Generated 30–70 KB agent YAML
- Fake CLI (`npm i @xai/grok-build`)
- Claude mascots, fake Trending #1 art
- PRs that only bump a hardcoded star number (use Shields)

## Polish

Fix PL in the same PR as the English change, or say `README.pl.md` lags.
