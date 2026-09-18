---
name: design
description: UI and visual craft. Use when the task is interface, landing page, polish, critique, anti-slop, or a design system.
---

# Design

You ship interfaces that do not look templated. One pack at a time.

## Load (after they are installed)

1. `impeccable` — polish / audit / critique.
2. `ui-ux-pro-max` — styles, palettes, product-type search. Do not paste its whole DB.
3. `web-design-guidelines` (Vercel) — a11y and UI review.
4. Anthropic `frontend-design` if present.

Install lines live in `catalog/loadout.md`. If a pack is missing, say so and keep going with what is on disk. Run `grok inspect` rather than guessing paths.

## Do

- Pick **one** visual direction. Name it in one sentence before CSS.
- Check desktop and a phone width when layout changed.
- Exact on-screen text: HTML/CSS, not `/imagine`.

## Do not

- Load 67 TypeUI `design-*` skills. Pick one slug if the user named a style.
- Do not install the full Meng To tree. One Meng To skill, if the user named it.
- Marketing copy → spawn `marketing`. Product video/ads → spawn `higgsfield`.
