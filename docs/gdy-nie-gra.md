# Gdy coś nie gra

Najpierw inspect. Potem ta lista. Nie dokładaj 200 skilli „na wszelki wypadek”.

## Skill się nie odpala

1. Czy jest na dysku? Grok: `grok inspect`. Claude/Codex: folder `skills/` albo `.claude/skills` / `.agents/skills`.
2. Czy `name` w YAML = nazwa folderu?
3. Czy `description` mówi **kiedy** — nie **jak**. Jak w description jest cała procedura, agent często nie otwiera body.
4. Czy nie ma kolizji nazwy z innym skilliem? Inspect pokaże prefiks.
5. Czy sesja wstała *po* instalacji? Skille biorą się na starcie.

Eval: [examples/eval-routing.md](../examples/eval-routing.md).

## `npx skills add` poszedł, a Grok nic nie widzi

Komenda często zapisuje do `.agents/skills/` albo `.claude/skills/`. Grok **skanuje** te katalogi, ale:

- odpal `grok inspect` w **tym** katalogu projektu,
- albo dołóż `-a` pod swój harness przy `npx skills add`,
- albo zainstaluj jeszcze raz z właściwym agentem.

Nie kopiuj paczki ręcznie do `skills/` tego playbooka (to tylko nasze dwa skille).

## Agent robi za dużo

Powiedz wprost: `One specialist only: design.` / `Fix this typo. No other files.`

Główny czat ma zostać szefem. Przepis 8.

## Plan Mode, a bash i tak leci

Na Grok tak ma być. Plan pilnuje **edycji pliku planu**, nie terminala. Dziecko-agent też nie jest piaskownicą. Szczegóły: [best-practice/grok-plan-mode.md](../best-practice/grok-plan-mode.md).

## Hook „miał zablokować”, a komenda poszła

Na Grok hooki są fail-open: crash albo timeout ≠ stop. Zaufanie: `/hooks-trust`. `allowed-tools` w SKILL.md **tu nic nie zamyka**. Na Claude Code `allowed-tools` już jest bramką — nie mieszaj tych dwóch.

## Higgsfield zjadł kredyty / zły obraz

- Preflight: `higgsfield model get <id>` i `higgsfield generate cost …` (albo MCP `get_cost`).
- Nie `curl api.higgsfield.ai`.
- Dokładny tekst UI → HTML, nie generate.
- Soul trenujesz raz; prompt z `reference_id` to drugi krok.

## Notion 401 / pusta lista skilli

- MCP i `npx skills add notion` to dwa wejścia. Oba potrzebują Twojego logowania, nie sekretu w gitcie.
- Widać tylko strony, do których połączenie ma dostęp.
- Grok Build ≠ Grok Bot. MCP jest drogą CLI.

## Gwiazdki / „trending #1”

W tym repo tylko żywe odznaki Shields. Nie wpisuj liczby z palca. Pytanie o gwiazdki Superpowers = badge, nie zgadywanie (eval #10).

## Za dużo paczek, sesja głupieje

Zdejmij to, czego dziś nie używasz. Daily set jest mały celowo. ECC i całe Meng To zostają w szafce, nie w starcie.
