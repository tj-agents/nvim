---
name: direction
description: Where Tommy is headed with Neovim — the goal, the staged skill tree over his own config's keymaps, and the references every lesson cites. Use when choosing or sequencing what to teach next, running the placement check, or sourcing a Neovim explanation.
kind: knowledge
domain: nvim
profile: knowledge
applicability: Neovim learning
requires: neovim
provenance: house
---

# Where Tommy is headed with Neovim

`nvim:knowledge` tracks where Tommy is now; this tracks where he is going.

## The goal

Fluency in `yanchikpiypiy/nvim-wsl`'s own bindings, through its real grammar (operator + count + motion
or text object), not a memorised list of isolated keys.

## The skill tree

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

## The rule

Drills happen in a real file in whatever repo Tommy is already in, never a toy sandbox. A slower path he
understands beats a fast one he doesn't; check that it landed by having him explain a binding back or do
the next one himself before moving on.

## References

Tommy runs `yanchikpiypiy/nvim-wsl`, cloned at `~/source/repos/nvim-wsl`, with `%LOCALAPPDATA%\nvim`
junctioned to it. Its `README.md` lists the keymaps; `lua/config/keymaps.lua` and `lua/plugins/*.lua` are
the real bindings — read them before naming a key, since this config rebinds stock keys (`s` is Flash,
not substitute; `<leader>f` alone formats). Verify a binding by reading the config, never by scripting
`nvim --headless`: an insert-mode probe orphans the Copilot server and has frozen the machine (that
README's Notes section).
