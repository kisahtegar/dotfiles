# Hyprland Dotfiles

Personal Linux desktop setup using:

* Hyprland
* Waybar
* Rofi
* Ghostty
* Neovim
* tmuxV
* Zsh
* GNU Stow

---

## Screenshots

<img src="./previews/desktop-1.png" width="100%">
<img src="./previews/desktop-2.png" width="100%">

---

## Structure

```text
dotfiles/
├── ghostty
├── hypr
├── nvim
├── rofi
├── tmux
├── waybar
├── wezterm
├── wpaperd
└── zsh
```

---

## Requirements

### Packages

Install required packages:

```bash
sudo pacman -S \
hyprland \
waybar \
rofi \
ghostty \
wezterm \
zsh \
tmux \
neovim \
wpaperd \
eza \
zoxide \
git \
stow
```

---

## Fonts

Required fonts:

* JetBrainsMono Nerd Font
* Meslo Nerd Font

---

## Clone Repository

```bash
git clone <your-repo-url> ~/dotfiles
cd ~/dotfiles
```

---

## GNU Stow Setup

```bash
stow zsh
stow hypr
stow waybar
stow rofi
stow ghostty
stow tmux
stow nvim
stow wpaperd
```

---

## tmux Plugins

Default key using CTRL+A ...

Install TPM:

```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

Inside tmux:

```text
CTRL + A + SHIFT + I
```

---

## Wallpaper

Wallpapers stored in:

```text
~/Pictures/Wallpapers
```

---

## Notes

### Wayland

Some applications may require:

```bash
env WAYLAND_DISPLAY=wayland-1
```

depending on compositor session setup.
