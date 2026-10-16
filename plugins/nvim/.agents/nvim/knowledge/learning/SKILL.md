---
name: learning
description: How to teach Tommy Neovim through his own config — read `nvim:knowledge` first, pitch the next step on the `nvim:direction` skill tree, teach 3–5 keys at a time with a hands-on drill in a real file, answer "how do I X in nvim" with this config's actual binding, and promote a skill only after he proves it. Use whenever Tommy asks how to do something in Neovim/nvim/vim, wants a lesson, drill or cheat sheet, says he learned or is struggling with a key, or asks to update his nvim progress.
kind: knowledge
domain: nvim
profile: knowledge
applicability: Neovim use and learning
requires: neovim
provenance: house
---

# Teaching Tommy Neovim

`nvim:knowledge` records what Tommy has proven he knows; `nvim:direction` records where he is headed and
the config he's learning. Read both before teaching.

## Calibrate to `nvim:knowledge`

- It is the only record of what Tommy knows. Config code or a past explanation is not evidence that he
  knows something.
- With an empty tracker, start with a two-minute placement check against `nvim:direction`'s skill tree:
  for each stage, list its keys and ask which he already uses without thinking. Record what he confirms
  and start at the first stage with gaps.

## Working rules

- Teach 3–5 keys per lesson, never a wall of keymaps. Each lesson has a concept, its keys, and a drill:
  a concrete sequence he performs in a real file in whatever repo he is in. For example: open a file with
  `<leader>ff`, press `]f` three times to reach the third function, rename it with `ciw`. He does it and reports back.
- Teach the grammar, not isolated keys: operator + count + motion or text object (`d3w`, `ci"`, `yap`).
  Once he has the grammar, new motions compose for free.
- Where a plugin key has a vanilla equivalent, show both so the skill transfers to any vim.
- For "how do I X", answer with the binding plus one sentence. Offer a drill only if he wants one.
- Build habits for looking things up: `:h <topic>`, `:Tutor` for stage 0, and the which-key popup
  (pausing after `Space`, his leader, opens it).
- Explain in chat. Change his nvim config only when he asks, commit those changes on the clone, and push
  to the upstream `yanchikpiypiy/nvim-wsl` only with his say-so.

## Progress

- Promote a skill in `nvim:knowledge` only after he proves it: he reports doing the drill, uses it
  unprompted, or explains it back. Explaining it to him is not the same as him knowing it, and he is
  the judge. 🟡 means met but shaky (he asks again, or reaches for the arrows or mouse); ✅ means fluent.
- If he says he is struggling with something, demote it to 🟡 and drill it again.
- To update: edit `.agents/nvim/knowledge/knowledge/SKILL.md` in `~/source/repos/tj-agents/nvim`, run
  `pwsh .agents/sync-generated.ps1`, then commit and push to `main`. Sessions get the change once the
  `nvim@tj-agents` plugin updates.
