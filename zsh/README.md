# Zsh

Shell configuration using:

* Zsh
* Oh My Zsh
* Powerlevel10k

Configured for development-focused terminal workflow.

---

## Structure

```text
zsh/
├── .p10k.zsh
└── .zshrc
```

---

## Features

* Powerlevel10k prompt
* Nerd Font support
* Git integration
* tmux workflow integration
* Shell aliases
* Improved terminal UX

---

## Dependencies

### Required Packages

Install:

```bash
sudo pacman -S zsh
```

---

## Oh My Zsh

Install Oh My Zsh:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

---

## Powerlevel10k

Install theme:

```bash id="8v5f7v"
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git \
${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

---

## Required Fonts

* Meslo Nerd Font
* JetBrainsMono Nerd Font

Required for:

* prompt icons
* terminal glyphs
* Neovim icons
* Waybar icons

---

## Configuration

### `.zshrc`

Main shell configuration.

Contains:

* aliases
* plugins
* PATH configuration
* shell behavior
* Powerlevel10k loading

---

### `.p10k.zsh`

Powerlevel10k prompt configuration.

Controls:

* prompt appearance
* git segments
* colors
* icons
* shell visual layout

---

## Notes

### Default Shell

Set Zsh as default shell:

```bash
chsh -s $(which zsh)
```

---

## tmux Workflow

Zsh is primarily used together with:

* tmux
* Ghostty
* WezTerm
* Neovim

---

## Related

* tmux
* Ghostty
* WezTerm
* Neovim
