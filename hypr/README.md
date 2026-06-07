# Hyprland

Main Wayland compositor configuration. This setup uses Lua-based Hyprland configuration instead of the default `.conf` format.

---

## Structure

```text id="t1a8bq"
hypr/
└── .config/
    └── hypr/
        ├── hyprland.lua
        └── .luarc.json
```

---

## Features

* Lua-based Hyprland configuration
* Multi-monitor setup
* Dynamic keybind behavior
* Custom submaps
* Rofi integration
* Waybar integration
* Wallpaper management
* Multimedia controls
* Workspace-aware navigation
* Layout-aware movement
* Touchpad gestures

---

## Dependencies

### Core Packages

```bash
sudo pacman -S \
    hyprland \
    waybar \
    rofi \
    ghostty \
    wpaperd \
    playerctl \
    brightnessctl \
    cliphist \
    wl-clipboard \
    nemo \
    brave
```

---

## Monitor Configuration

Configured monitors:

* Laptop display (`eDP-1`)
* External monitor (`HDMI-A-1`)

Example:

```lua
hl.monitor({
    output   = "HDMI-A-1",
    mode     = "1920x1080@144",
    position = "1366x0",
    scale    = "1",
})
```

---

## Programs

Configured default applications:

| Program      | Application |
| ------------ | ----------- |
| Terminal     | Ghostty     |
| File Manager | Nemo        |
| Browser      | Brave       |
| Music        | Spotify     |

---

## Rofi Integration

Rofi is used for:

* app launcher
* calculator
* emoji picker
* clipboard history

Keybind examples:

| Keybind       | Action       |
| ------------- | ------------ |
| SUPER + Space | App launcher |
| SUPER + C     | Calculator   |
| SUPER + E     | Emoji picker |

---

## Autostart

Automatically starts:

* Waybar
* wpaperd
* playerctl daemon
* hyprpolkitagent

---

## Environment Variables

```lua
hl.env("QT_QPA_PLATFORMTHEME", "qt6ct")
```

Used for Qt application theming.

---

## Window Management

### Focus Movement

| Keybind   | Action      |
| --------- | ----------- |
| SUPER + H | Focus left  |
| SUPER + J | Focus down  |
| SUPER + K | Focus up    |
| SUPER + L | Focus right |

Behavior changes dynamically depending on active layout.

---

## Workspace Management

| Keybind             | Action                   |
| ------------------- | ------------------------ |
| SUPER + 1-0         | Switch workspace         |
| SUPER + SHIFT + 1-0 | Move window to workspace |

---

## Submaps

### Power Menu

Activated with:

```text id="s4p7a5"
SUPER + SHIFT + P
```

Actions:

* Suspend
* Shutdown
* Reboot
* Logout

---

### Wallpaper Controls

Activated with:

```text id="wx44vd"
SUPER + SHIFT + W
```

Actions:

* Next wallpaper
* Previous wallpaper

---

## Multimedia Keys

Supports:

* volume control
* microphone mute
* brightness control
* media playback

---

## Touchpad Gestures

Three-finger horizontal swipe switches workspaces.

---

## Notes

### Lua Configuration

This setup uses Hyprland Lua configuration API.

Benefits:

* cleaner logic
* reusable functions
* conditional behavior
* improved readability

---

## Related

* Waybar
* Rofi
* Ghostty
* wpaperd
* tmux
* Neovim
