# nvim

Neovim learning companion for Claude Code and Codex, published as `nvim@tj-agents` (repository marketplace
`nvim-agents`). The config it teaches is [`yanchikpiypiy/nvim-wsl`](https://github.com/yanchikpiypiy/nvim-wsl).

- `nvim:learning` — teaching method, placement check and staged curriculum over that config's keymaps.
- `nvim:knowledge` — what Tommy has proven he knows; updated as he progresses.

The tier applies in every project (`tier.json` `applies: always`): the editor is not a repository stack.

## Authoring and verification

```powershell
pwsh .agents/sync-generated.ps1
pwsh .agents/sync-generated.ps1 -Check
python -B -m unittest discover -s .agents/tests -p "test_*.py"
```

Push to `main`; sessions pick the change up when the plugin updates.
