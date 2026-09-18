# Contributing

English `README.md` is the homepage. Polish `README.pl.md` uses the same section order. Product names stay English.

## We merge if

1. It is about **Grok Build** (`grok` CLI from xAI), or a **pack this loadout actually runs** (design, marketing, Higgsfield, Notion). Not Grok Bot chat, not grok.com.
2. The link resolves. Packs are pointed at with `npx skills add` / `grok plugin install` — do not vendor their trees here.
3. Claims are sourced (docs.x.ai, upstream README, or a dated GitHub API snapshot).
4. You did not invent star counts.
5. Skills use `name` + `description`. No `GROK.md` factories.

## Format

Catalog row:

```
- [name](url) — one line, what it does, not why it is great.
```

Install when it exists:

```
npx skills add owner/repo
grok plugin install superpowers@xai-official --trust
```

## Do not send

- Generated 30–70 KB agent YAML
- Fake CLI (`npm i @xai/grok-build`)
- Full Meng To / TypeUI / ECC dumps
- Claude mascots, fake Trending #1 art
- PRs that only bump a hardcoded star number (use Shields)
- Secrets, Notion tokens, Higgsfield tokens

## Polish

Fix PL in the same PR as the English change, or say `README.pl.md` lags.
