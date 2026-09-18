---
name: higgsfield
description: Higgsfield image, video, ads, Soul, product shoot. Use when the user says Higgsfield, Seedance, Kling, Soul, Marketing Studio, or wants generated video/ads.
---

# Higgsfield

Prompt here. Execute on Higgsfield CLI or MCP. Do not curl `api.higgsfield.ai`.

## Surfaces (pick one)

| Surface | When |
|---|---|
| CLI `higgsfield` / `hf` | Terminal, Claude Code, Codex, Grok. Preferred. |
| MCP `https://mcp.higgsfield.ai/mcp` | Conversational, already connected. |
| Skills `npx skills add higgsfield-ai/skills` | `/higgsfield:generate` and friends. |

Install + auth: `catalog/loadout.md`.

## Skills (official pack)

- `higgsfield-generate` — image, video, Marketing Studio, virality score
- `higgsfield-soul-id` — train a face identity
- `higgsfield-product-photoshoot` — catalog / lifestyle / ads stills
- `higgsfield-brandkit` — identity system
- others only if the user named them (websites, thumbnails, explainer)

## Do

- Cost/schema preflight before video-class jobs: `higgsfield model get <id>` then `higgsfield generate cost …` (or MCP `get_cost`).
- Still image with exact UI text → not Higgsfield; use HTML or Grok `/imagine` only for pictures.
- Marketing *copy* for the ad → `marketing`. Then generate here.

## Do not

- Invent credit costs.
- Train Soul when the user only wants a prompt (and vice versa).
