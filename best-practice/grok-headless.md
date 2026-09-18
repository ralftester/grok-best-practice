# Headless and ACP

```bash
grok -p "Explain this repo"
grok -p "Run the tests" --output-format json
grok -p "…" --output-format streaming-json
```

Useful flags: `-m`, `-s/--session-id`, `-r/--resume`, `-c/--continue`, `--cwd`, `--always-approve`, `--worktree`, `--no-auto-update`.

IDE path: `grok agent stdio` (ACP JSON-RPC). That is how [grok-build-web](https://github.com/AppleLamps/grok-build-web) and multi-agent GUIs attach.

CI: pin `--no-auto-update`, do not pass secrets on the command line, prefer permission deny-rules over `--always-approve` on untrusted repos.

Source: [Headless](https://docs.x.ai/build/cli/headless-scripting).
