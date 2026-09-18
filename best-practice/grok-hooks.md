# Hooks

JSON (and `config.toml` on recent builds). User hooks: `~/.grok/hooks/*.json`. Project hooks: `.grok/hooks/` after `/hooks-trust` or `--trust`.

`PreToolUse` is the only blocking event. Matcher is a regex on the tool name. Claude names (`Bash`, `Read`, `Edit`) map over.

**Fail-open:** timeout, crash, or bad JSON → the tool still runs. A deny or exit 2 is the block. That is weaker than treating PreToolUse as CI.

If you need a hard gate, pair hooks with `[permission]` rules and a sandbox profile. Do not put the gate only in SKILL.md.

Source: Grok Build user-guide hooks chapter, [cc-safety-net](https://github.com/kenryu42/cc-safety-net) (community, declares Grok Build).
