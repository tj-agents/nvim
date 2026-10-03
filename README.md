# nvim

Neovim learning companion for Claude Code and Codex, published as plugin `nvim` from this repository's
`nvim-agents` marketplace. The config it teaches is [`yanchikpiypiy/nvim-wsl`](https://github.com/yanchikpiypiy/nvim-wsl).

## Skills

- Knowledge: `nvim:direction`, `nvim:knowledge`, `nvim:learning`.

The tier applies in every project (`tier.json` `applies: always`): the editor is not a repository stack.

## Authoring and verification

```powershell
pwsh .agents/sync-generated.ps1
pwsh .agents/sync-generated.ps1 -Check
```

The layout, the vendored generator and CI come from [kit](https://github.com/tj-agents/kit).

Push to `main`; sessions pick the change up when the plugin updates.
