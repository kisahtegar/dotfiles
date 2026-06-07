# Rofi

Application launcher and desktop menu configuration for Hyprland setup.

Used for:

* application launching
* command execution
* calculator mode
* emoji picker
* clipboard history

---

## Structure

```text
rofi/
└── .config/
    └── rofi/
        ├── config.rasi
        └── themes/
            └── spotlight-dark.rasi
```

---

## Features

* Minimal launcher UI
* Spotlight-inspired design
* Dark theme
* Rounded appearance
* Keyboard-driven workflow
* Integrated with Hyprland keybinds

---

## Dependencies

Install Rofi:

```bash
sudo pacman -S rofi-wayland
```

---

## Theme

Current theme:

```text
spotlight-dark.rasi
```

Inspired by:

* macOS Spotlight
* minimal dark UI
* productivity-focused launcher design

---

## Configuration

### Main Config

```text
config.rasi
```

Controls:

* launcher behavior
* enabled modes
* keybindings
* theme imports

---

### Theme File

```text id="w5xj1m"
themes/spotlight-dark.rasi
```

Controls:

* colors
* spacing
* fonts
* border radius
* layout
* transparency

---

## Theme Colors

Uses centralized variables:

```css id="7hkp0r"
bg0
bg1
bg2
fg0
fg1
fg2
```

for easier theme maintenance.

---

## Hyprland Integration

Integrated with Hyprland keybindings.

Example:

| Keybind           | Action            |
| ----------------- | ----------------- |
| SUPER + Space     | Open launcher     |
| SUPER + C         | Calculator        |
| SUPER + E         | Emoji picker      |
| SUPER + SHIFT + C | Clipboard history |

---

## Notes

### Wayland Version

Uses:

```text id="1q9b2w"
rofi-wayland
```

instead of X11 Rofi.

Recommended for Hyprland/Wayland setups.

---

## Related

* Hyprland
* Waybar
* Ghostty
