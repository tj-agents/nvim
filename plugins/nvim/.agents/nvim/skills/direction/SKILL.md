---
name: direction
description: Neovim learning orientation and config references. Use when locating Tommy's goal, staged keymap curriculum or proven knowledge, or sourcing a binding; nvim:learning owns teaching and progress.
kind: reference
domain: nvim
profile: knowledge
applicability: Neovim learning
requires: neovim
provenance: house
---

# Neovim learning orientation

## Orientation

Tommy's goal and complete staged keymap curriculum are in [the direction record](../../learning/direction.md).
[The learner record](../../learning/knowledge.md) records what he has proven he knows.
`nvim:learning` owns lesson selection, placement checks, drills and progress updates.

```text
Question: What is Tommy learning, and where is the actual binding defined?
Goal and curriculum: .agents/nvim/learning/direction.md
Proven knowledge: .agents/nvim/learning/knowledge.md
Binding source: ~/source/repos/nvim-wsl/lua/config/keymaps.lua and lua/plugins/*.lua
Teaching and progress: nvim:learning
```

## References

Tommy runs `yanchikpiypiy/nvim-wsl`, cloned at `~/source/repos/nvim-wsl`, with `%LOCALAPPDATA%\nvim`
junctioned to it. Its `README.md` lists the keymaps; `lua/config/keymaps.lua` and `lua/plugins/*.lua` are
the real bindings — read them before naming a key, since this config rebinds stock keys (`s` is Flash,
not substitute; `<leader>f` alone formats). Verify a binding by reading the config, never by scripting
`nvim --headless`: an insert-mode probe orphans the Copilot server and has frozen the machine (that
README's Notes section).
