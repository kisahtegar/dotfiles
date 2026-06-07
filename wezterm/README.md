# WezTerm

GPU-accelerated terminal emulator configuration. Used as an alternative terminal setup alongside Ghostty.

---

## Structure

```text
wezterm/
└── .wezterm.lua
```

---

## Features

* Lua-based configuration
* Minimal terminal appearance
* Transparent background
* Nerd Font support
* tmux-friendly setup
* Custom terminal palette

---

## Dependencies

Install WezTerm:

```bash
sudo pacman -S wezterm
```

---

## Required Fonts

* MesloLGS Nerd Font Mono

Used for:

* terminal glyphs
* Powerlevel10k
* tmux icons
* Neovim icons

---

## Configuration

### Font

```lua
config.font = wezterm.font("MesloLGS Nerd Font Mono")
config.font_size = 10
```

Sets terminal font and size.

---

## Tab Bar

```lua
config.enable_tab_bar = false
```

Disables tab bar for cleaner tmux workflow.

---

## Window Decorations

```lua id="9f1cr0"
config.window_decorations = "RESIZE"
```

Keeps resize border while removing title bar.

---

## Transparency

```lua
config.window_background_opacity = 0.8
```

Adds terminal transparency.

---

## Theme

Custom blue/cyan terminal palette inspired by dark neon themes.

Includes:

* custom cursor colors
* ANSI palette
* bright palette
* selection colors

---

## Notes

### tmux Workflow

WezTerm is primarily used together with:

* tmux
* Neovim
* zsh

---

## Related

* Ghostty
* tmux
* Neovim
* zsh
