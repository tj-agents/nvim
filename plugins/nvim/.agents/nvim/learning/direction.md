# Neovim learning direction

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

