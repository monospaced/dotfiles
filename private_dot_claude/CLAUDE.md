# Machine conventions

## Node

- Node is managed by `fnm`. Never install Node via Homebrew or any other method.
- Use `pnpm` for packages. Install global JS CLIs with `pnpm`, not Homebrew
  or `npm`.

## When something is blocked

- Say which layer blocked it: a permission rule, or the sandbox.
- Default to a one-off: name the host, or ask to run it un-sandboxed, and I'll
  decide. Don't rephrase a command to get around a rule.
- Suggest a settings change if the same block will recur every session. Machine
  facts go in `~/.claude/settings.json`, project facts in the repo's. I make
  the change.
- Excluded commands (`gh`, git network and signing) must be the whole call: no
  pipes, `&&` or `cd`, or they run sandboxed.
