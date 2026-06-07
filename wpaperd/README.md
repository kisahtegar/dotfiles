# wpaperd

Wallpaper daemon configuration for Wayland desktop setup. Used for automatic wallpaper management and transitions.

---

## Structure

```text
wpaperd/
├── .config/
│   └── wpaperd/
│       └── config.toml
└── wallpapers/
```

---

## Features

* Automatic wallpaper rotation
* Random wallpaper selection
* Smooth transitions
* Multi-monitor support
* Wayland-native wallpaper daemon

---

## Dependencies

Install wpaperd:

```bash
sudo pacman -S wpaperd
```

---

## Wallpaper Directory

Wallpapers stored in:

```text
wpaperd/wallpapers/
```

---

## Configuration

### Wallpaper Source

```toml id="c2e9oj"
path = "~/dotfiles/wpaperd/wallpapers"
```

Directory used for wallpaper rotation.

---

## Duration

```toml id="ak5b8x"
duration = "15m"
```

Changes wallpaper every:

* 15 minutes

---

## Sorting

```toml id="myn3ck"
sorting = "random"
```

Randomizes wallpaper order.

---

## Transition Effects

### Directional Wipe

```toml
[default.transition.directional-wipe]
direction = [1.0, 0.0]
```

Uses directional wipe transition effect.

Direction:

* left → right

---

## Autostart

wpaperd is automatically launched by Hyprland configuration.

---

## Notes

### Supported Formats

Recommended:

* PNG
* JPG
* WebP

---

## Related

* Hyprland
* Waybar
