# CLAUDE.md

## Project overview

Personal dotfiles and editor configuration repository. Contains configuration for NeoVim (NvChad), Tmux, Vim, Bash, and Obsidian.

## Repository structure

- `.bash_aliases` - Bash shell aliases
- `.vimrc` - Vim editor configuration
- `.tmux.conf` - Tmux terminal multiplexer configuration (prefix: C-a)
- `.obsidian.vimrc` - Vim keybindings for Obsidian
- `nice-to-haves` - List of desired tools and packages
- `nvchad-config/nvim/` - NeoVim configuration using NvChad v2.5
  - `init.lua` - Entry point
  - `lua/chadrc.lua` - NvChad theme/UI config
  - `lua/options.lua` - Editor options
  - `lua/mappings.lua` - Key mappings
  - `lua/configs/` - Plugin configurations (LSP, formatting, lazy.nvim)
  - `lua/plugins/` - Plugin declarations and autocompletion setup

## Code style

- Lua files: 2-space indentation, 120 column width, Unix line endings, double quotes preferred (enforced by `.stylua.toml`)
- Vim script: Standard vim configuration conventions

## Key tools and plugins

- **Plugin manager:** lazy.nvim (lock file: `lazy-lock.json`)
- **LSP:** nvim-lspconfig with Mason for server management; Solargraph (Ruby) configured
- **Formatting:** conform.nvim with stylua for Lua
- **Tmux plugins:** managed via TPM (Tmux Plugin Manager)

## Common tasks

- No build system, test suite, or CI pipeline - this is a dotfiles repo
- To check Lua formatting: `stylua --check nvchad-config/nvim/`
- To format Lua files: `stylua nvchad-config/nvim/`
