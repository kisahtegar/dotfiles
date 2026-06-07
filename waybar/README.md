# Waybar

Status bar configuration for Hyprland Wayland desktop setup.

Provides:

* workspace indicators
* media controls
* system monitoring
* tray integration
* audio controls
* interactive modules

---

## Structure

```text
waybar/
└── .config/
    └── waybar/
        ├── auto-reload.sh
        ├── config.jsonc
        ├── custom_modules/
        │   └── media/
        │       ├── media-animation.sh
        │       ├── media-now-playing.sh
        │       └── media-time.sh
        └── style.css
```

---

## Features

* Hyprland workspace integration
* Interactive modules
* Custom media widgets
* Volume slider
* Bluetooth integration
* Network controls
* System monitoring
* Tray support
* Custom CSS styling

---

## Dependencies

### Required Packages

Install:

```bash
sudo pacman -S \
    waybar \
    playerctl \
    pavucontrol \
    networkmanager \
    brightnessctl
```

---

## Additional Dependencies

### zscroll

Required for scrolling media titles:

```bash
yay -S zscroll-git
```

---

## Layout

### Left Modules

* Workspaces
* Media information

---

### Center Modules

* Clock

---

### Right Modules

* Submap indicator
* Volume controls
* Battery
* Bluetooth
* Network
* CPU
* Memory
* Tray

---

## Interactive Modules

| Module    | Action               |
| --------- | -------------------- |
| CPU       | Open btop            |
| Memory    | Open htop            |
| Bluetooth | Open bluetui         |
| Network   | Open nmtui           |
| Clock     | Open Google Calendar |
| Volume    | Open pavucontrol     |

---

## Styling

Main styling located in:

```text
style.css
```

Uses:

* dark theme
* rounded modules
* cyan highlight color
* compact spacing

---

## Custom Media Modules

### media-animation.sh

Animated playback indicator.

Displays:

* animation while playing
* pause icon while paused

---

### media-now-playing.sh

Scrolling song title using:

* playerctl
* zscroll

---

### media-time.sh

Displays:

* current playback position
* total duration

---

## Auto Reload

```text
auto-reload.sh
```

Automatically reloads Waybar when configuration files change.

---

## Notes

### Fonts

Requires Nerd Fonts for icons.

Recommended:

* JetBrainsMono Nerd Font

---

## CSS Variables

Theme colors defined using:

```css
@define-color
```

for easier theme management.

---

## Related

* Hyprland
* Rofi
* wpaperd
* Ghostty
