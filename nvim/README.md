# Neovim

Modern Lua-based Neovim configuration focused on:

* development workflow
* LSP support
* productivity
* terminal integration
* modular architecture

Built using:

* lazy.nvim
* Lua configuration
* plugin modularization

---

## Structure

```text
nvim/
└── .config/
    └── nvim/
        ├── init.lua
        ├── lazy-lock.json
        ├── .stylua.toml
        └── lua/
            └── kisarch/
                ├── core/
                │   ├── init.lua
                │   ├── keymaps.lua
                │   └── options.lua
                ├── plugins/
                │   ├── lsp/
                │   └── *.lua
                ├── lazy.lua
                └── lsp.lua
```

---

## Features

* Lua-based configuration
* lazy.nvim plugin manager
* LSP support
* Treesitter syntax parsing
* Telescope fuzzy finder
* Git integration
* Auto completion
* Auto formatting
* Session management
* tmux integration

---

## Dependencies

### Required Packages

Install:

```bash
sudo pacman -S \
    neovim \
    ripgrep \
    fd \
    git \
    gcc \
    npm \
    python \
    unzip
```

---

## Plugin Manager

Uses:

```text
lazy.nvim
```

for plugin management.

---

## Core Configuration

### `core/options.lua`

Contains:

* editor options
* indentation
* line numbers
* tabs/spaces
* UI behavior

---

### `core/keymaps.lua`

Contains:

* custom keybindings
* workflow shortcuts
* navigation mappings

---

## Plugin Architecture

Each plugin has its own configuration file:

```text
plugins/
├── telescope.lua
├── treesitter.lua
├── lualine.lua
└── ...
```

This improves:

* readability
* modularity
* maintainability

---

## LSP Setup

LSP configuration separated into:

```text
plugins/lsp/
├── lsp.lua
└── manson.lua
```

Uses:

* mason.nvim
* mason-lspconfig.nvim
* nvim-lspconfig

---

## Completion

Completion powered by:

| Plugin       | Purpose           |
| ------------ | ----------------- |
| nvim-cmp     | Completion engine |
| LuaSnip      | Snippet engine    |
| cmp-buffer   | Buffer completion |
| cmp-path     | Path completion   |
| cmp-nvim-lsp | LSP completion    |

---

## Main Plugins

| Plugin          | Purpose            |
| --------------- | ------------------ |
| telescope.nvim  | Fuzzy finder       |
| nvim-treesitter | Syntax parsing     |
| lualine.nvim    | Statusline         |
| bufferline.nvim | Buffer tabs        |
| gitsigns.nvim   | Git indicators     |
| trouble.nvim    | Diagnostics UI     |
| auto-session    | Session management |
| lazygit.nvim    | Git UI integration |
| nvim-tree.lua   | File explorer      |

---

## Formatting

Uses:

```text
conform.nvim
```

for formatting support.

---

## Linting

Uses:

```text
nvim-lint
```

for diagnostics and linting.

---

## Styling

Lua formatting configured using:

```text
.stylua.toml
```

---

## Lockfile

```text
lazy-lock.json
```

pins plugin versions for:

* reproducible setup
* stability
* safer reinstalls

---

## tmux Integration

Integrated with:

```text
vim-tmux-navigator
```

for seamless movement between:

* Neovim splits
* tmux panes

---

## Workflow

This setup is designed for:

* web development
* terminal workflow
* Linux productivity
* keyboard-driven navigation

---

## Related

* tmux
* Zsh
* Ghostty
* WezTerm
* Hyprland
