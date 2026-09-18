# Plan Mode

`/plan` or Shift+Tab. While a plan is open, Grok is supposed to edit the plan file, not the rest of the tree, until you approve.

Caveats that lists skip:

- Bash is **not** blocked. Redirects still write files.
- Child subagents do not inherit the edit-gate. They inherit permission mode.
- Auto / always-approve does not skip plan review.

Use Plan Mode for risky or multi-file work. Then still run tests. It is not an OS sandbox.

Source: [Modes and commands](https://docs.x.ai/build/modes-and-commands).
