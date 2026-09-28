---
name: learning
description: How to teach Tommy Neovim through his own config — read `nvim:knowledge` first, pitch the next curriculum stage, teach 3–5 keys at a time with a hands-on drill in a real file, answer "how do I X in nvim" with this config's actual binding, and promote a skill only after he proves it. Use whenever Tommy asks how to do something in Neovim/nvim/vim, wants a lesson, drill or cheat sheet, says he learned or is struggling with a key, or asks to update his nvim progress.
kind: knowledge
domain: nvim
profile: core
applicability: Neovim use and learning
requires: neovim
provenance: house
---

# Teaching Tommy Neovim

## The config

Tommy runs `yanchikpiypiy/nvim-wsl`, cloned at `~/source/repos/nvim-wsl`, with `%LOCALAPPDATA%\nvim`
junctioned to it. Its `README.md` lists the keymaps; `lua/config/keymaps.lua` and `lua/plugins/*.lua` are
the real bindings. Read them before naming a key. This config rebinds stock keys (`s` is Flash, not
substitute; `<leader>f` alone formats), so stock-vim or LazyVim memory gives wrong answers. Leader is
`Space`, and pausing after it opens which-key. Teach him to use that popup to find keys.

Verify a binding by reading the config, never by scripting `nvim --headless`: an insert-mode probe
orphans the Copilot server and has frozen the machine (README Notes).

## Method

- Read `nvim:knowledge` first. It is the only record of what he knows. Config code or a past explanation
  is not evidence that he knows something.
- With an empty tracker, start with a two-minute placement check. For each stage, list its keys and ask
  which he already uses without thinking. Record what he confirms and start at the first stage with gaps.
- Teach 3–5 keys per lesson, never a wall of keymaps. Each lesson has a concept, its keys, and a drill:
  a concrete sequence he performs in a real file in whatever repo he is in. For example: open a file with
  `<leader>ff`, press `]f` three times to reach the third function, rename it with `ciw`. He does it and reports back.
- Teach the grammar, not isolated keys: operator + count + motion or text object (`d3w`, `ci"`, `yap`).
  Once he has the grammar, new motions compose for free.
- Where a plugin key has a vanilla equivalent, show both so the skill transfers to any vim.
- For "how do I X", answer with the binding plus one sentence. Offer a drill only if he wants one.
- Build habits for looking things up: `:h <topic>`, `:Tutor` for stage 0, and the which-key popup.
- Explain in chat. Change his nvim config only when he asks, commit those changes on the clone, and push
  to the upstream `yanchikpiypiy/nvim-wsl` only with his say-so.

## Progress

- Promote a skill in `nvim:knowledge` only after he proves it: he reports doing the drill, uses it
  unprompted, or explains it back. Explaining it to him is not the same as him knowing it, and he is
  the judge. 🟡 means met but shaky (he asks again, or reaches for the arrows or mouse); ✅ means fluent.
- If he says he is struggling with something, demote it to 🟡 and drill it again.
- To update: edit `.agents/knowledge/knowledge/SKILL.md` in `~/source/repos/tj-agents/nvim`, run
  `pwsh .agents/sync-generated.ps1`, then commit and push to `main`. Sessions get the change once the
  `nvim@tj-agents` plugin updates.

## Curriculum

0. **Survive** — modes; `i a I A o O`, `<Esc>`; `:w :q :wq :q!`; `u <C-r>`; `hjkl`; `:Tutor`.
1. **Move** — `w b e` / `W B E`; `0 ^ $`; `gg G`; `{ }`; `f t F T ; ,`; `%`; counts using the relative
   line numbers (`5j`); `<C-d> <C-u> zz`; `/ ? n N *`; `<Esc>` clears the search highlight.
2. **Edit grammar** — operators `d c y > <` with a motion; `dd cc yy`; `x r ~ J`; `p P`; `.`; text
   objects `iw aw i" i( i{ it ip` plus the config's `af if ac ic aa ia`; visual `v V <C-v>`. Every yank
   already reaches the Windows clipboard (`clipboard=unnamedplus`).
3. **Get around the project** — `<leader>ff fg fb fr fR`; `<leader>e` (neo-tree: `l h H P`); Flash
   `s S`; `[b ]b`; windows `<C-w>v s w q o` and `<C-w>hjkl`, resized with `<C-arrows>`; jumplist
   `<C-o> <C-i>`; Harpoon `<leader>a`, `<leader>h`, `<leader>1`–`4`; `<C-\>` for the terminal.
4. **Code with LSP** — `K gd gD gr gi gy`; `<leader>rn`, `<leader>ca`; `[d ]d <leader>d`;
   `<leader>xx xd xs`; completion `<C-x> <CR> <Tab> <C-e>`; `<leader>f` to format; `]f [f ]] [[`;
   `<leader>ls lw`.
5. **Git** — `<leader>gg` (lazygit); hunks `]c [c`, `<leader>gs gR gp gb`; `<leader>gv gV`; review mode
   `<leader>gn` with `]r [r`; file history `<leader>gh`.
6. **.NET, tests, debug** — `<leader>nb nr`; `<leader>ntt ntr nta ntp`; `<F9> <F5> <F10> <F11> <F8>`;
   `<leader>ndv nde`.
7. **Power** — registers `"a` and `:reg`; macros `qa @a @@`; marks `ma 'a` and `` `. ``;
   `:s/x/y/g`, `:%s`, `&`; `:g/pat/d`; quickfix `]q [q` and `:cdo`; `gv` and `o` in visual mode;
   `<C-a> <C-x>`; the `*` + `ciw` + `n.` refactor loop.
