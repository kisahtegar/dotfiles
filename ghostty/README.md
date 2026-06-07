# Ghostty

GPU-accelerated terminal emulator configuration for Wayland desktop setup.

## Features

* Minimal terminal appearance
* Nerd Font support
* Custom color palette
* Transparent-ready configuration
* tmux-friendly workflow
* Neovim optimized

---

## Structure

```text
ghostty/
└── .config/
    └── ghostty/
        └── config.ghostty
```

---

## Dependencies

### Required Packages

Install Ghostty:

```bash
sudo pacman -S ghostty
```

### Required Fonts

* JetBrainsMono Nerd Font Mono

Nerd Fonts are required for:

* terminal icons
* tmux icons
* Neovim UI
* Waybar glyphs

---

## Configuration Explanation

### Font

```properties
font-family = JetBrainsMono Nerd Font Mono
font-size = 10
```

Sets:

* terminal font family
* font size

JetBrainsMono Nerd Font Mono is used for:

* programming ligatures
* consistent terminal spacing
* Nerd Font icon support

---

## Window Padding

```properties
window-padding-x = 10
window-padding-y = 10
```

Adds spacing inside terminal window for cleaner appearance.

---

## Transparency

```properties
background-opacity = 1
```

Controls terminal transparency.

Values:

* `1` = fully opaque
* `0.9` = slightly transparent
* `0.8` = more transparent

---

## Theme Colors

### Background / Foreground

```properties
background = #00111E
foreground = #CBE0F0
```

Sets:

* terminal background color
* default text color

---

## Cursor

```properties
cursor-color = #47FF9C
cursor-text = #011423
```

Custom cursor colors.

---

## Selection

```properties
selection-background = #033259
selection-foreground = #CBE0F0
```

Controls selected text colors.

---

## Terminal Palette

```properties
palette = ...
```

Defines ANSI terminal colors used by:

* CLI applications
* tmux
* Neovim
* shell tools

Palette indexes:

* `0-7` = normal colors
* `8-15` = bright colors

---

## Notes

### Wayland

Ghostty runs natively on Wayland.

Some applications may require:

```bash
env WAYLAND_DISPLAY=wayland-1
```

depending on compositor session behavior.

---

## Related

* tmux
* zsh
* Neovim
* Hyprland
