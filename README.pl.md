**Język:** [English](README.md) · **Polski**

<p align="center">
  <img src="docs/assets/banner-1280x640.png" width="800" alt="grok-best-practice" />
</p>

<p align="center">
  <a href="https://github.com/ralftester/grok-best-practice/stargazers"><img src="https://img.shields.io/github/stars/ralftester/grok-best-practice?style=flat&label=%E2%98%85&labelColor=111&color=1d9bf0" alt="Gwiazdki" /></a>
  <a href="README.md"><img src="https://img.shields.io/badge/lang-EN-blue" alt="English" /></a>
  <a href="README.pl.md"><img src="https://img.shields.io/badge/lang-PL-red" alt="Polski" /></a>
</p>

# grok-best-practice

**od klepania w czacie do inżynierii agentów na Grok Build**

Kurs i mapa ekosystemu dla terminalowego agenta xAI. Skille, wtyczki, hooki, `AGENTS.md`, `grok inspect`, Plan Mode, headless, ACP.

> Nieoficjalne. Bez afiliacji z xAI. **Grok Build ≠ Grok Bot ≠ grok.com.** Angielski README jest źródłem prawdy. Tu jest skrót, nie kalka.

## Start

```bash
curl -fsSL https://x.ai/cli/install.sh | bash
cd projekt
grok inspect
grok plugin install superpowers@xai-official --trust
grok
```

W TUI: `Use inspect-and-ship. Do not edit yet.`

Czytaj to jak kurs. Jedna paczka na raz. Nie wsypuj 292 skilli do `.grok/`.

## Koncepcje

Pełna tabela i linki: [README.md](README.md#concepts).

| Co | Gdzie | Uwaga |
|---|---|---|
| Reguły | `AGENTS.md` | Ładuje też `CLAUDE.md` jako kompat. |
| Skille | `.grok/skills/` | `allowed-tools` **nie zamyka** narzędzi. |
| Wtyczki | `grok plugin install …` | Superpowers jest na oficjalnym marketplace. |
| Hooki | `.grok/hooks/` | Fail-open: crash nie blokuje toola. |
| Inspect | `grok inspect` | Tego Claude nie ma. |
| Plan | `/plan` | Nie blokuje bash. |
| Headless | `grok -p` | CI i skrypty. |
| ACP | `grok agent stdio` | IDE / GUI. |
| Demo | [inspect-and-ship](.grok/skills/inspect-and-ship/SKILL.md) | Pierwsza sesja. |

## Grok vs Claude vs Cursor

Uczciwie, 2026-09-17. Grok wygrywa inspect, ACP, otwarty harness, BYO model, imagine. Claude wygrywa wielkość marketplace i to, że `allowed-tools` naprawdę działa. Cursor to edytor; Grok Bot to inny produkt (cloud VM).

Nie pisz „drop-in Claude”. Grok **czyta** pliki z `.claude/`. Semantyki security nie kopiuje.

## Workflowy i community

Żywe ★: [catalog/workflows.md](catalog/workflows.md), [catalog/community.md](catalog/community.md).

Pierwszy install: `grok plugin install superpowers@xai-official --trust`

Starter kit, który już był: [DominikTobureto/awesome-grok-build](https://github.com/DominikTobureto/awesome-grok-build) (62★, last push 23 sie 2026). Szacunek, CLI od tego czasu jest na 1.0.x.

Grok Bot: [awesome-grok-bot](https://github.com/ZeroPointRepo/awesome-grok-bot). Inna półka.

## Czego nie robić

- YAML/`GROK.md` z LifeJiggy — Grok tego nie ładuje. Workflowy to `.rhai`.
- Twarde gwiazdki wpisane z palca.
- Farmy followi / fake Trending #1.
- 60 wygenerowanych „agentów” po 40 KB.

## Licencja

[CC BY 4.0](LICENSE).

Jeśli to skróciło setup, [daj gwiazdkę](https://github.com/ralftester/grok-best-practice/stargazers). Tego jednego prosimy.
