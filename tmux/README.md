# tmux

Terminal multiplexer configuration for terminal-based development workflow.

Used together with:

* Zsh
* Neovim
* Ghostty
* WezTerm

---

## Structure

```text
tmux/
└── .tmux.conf
```

---

## Features

* Vim-style keybindings
* tmux plugin manager (TPM)
* Persistent sessions
* Mouse support
* Neovim integration
* Pane resizing
* tmux power statusline
* Session restoration

---

## Dependencies

### Required Packages

Install tmux:

```bash
sudo pacman -S tmux
```

---

## Plugin Manager

### Install TPM

```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

---

## Install Plugins

Inside tmux:

```text
CTRL + A + SHIFT + I
```

---

## Prefix Key

Default tmux prefix:

```text
CTRL + B
```

replaced with:

```text
CTRL + A
```

for more ergonomic Vim-style workflow.

---

## Keybindings

| Keybind        | Action                    |
| -------------- | ------------------------- |
| PREFIX + |     | Split pane horizontally   |
| PREFIX + -     | Split pane vertically     |
| PREFIX + h     | Resize pane left          |
| PREFIX + j     | Resize pane down          |
| PREFIX + k     | Resize pane up            |
| PREFIX + l     | Resize pane right         |
| PREFIX + m     | Toggle pane zoom          |
| PREFIX + r     | Reload tmux configuration |
| PREFIX + Mouse | Resize/select panes       |

---

## Copy Mode

Vim-style copy mode enabled.

| Key | Action               |
| --- | -------------------- |
| v   | Begin text selection |
| y   | Copy selected text   |

---

## Mouse Support

```tmux
set -g mouse on
```

Enables:

* pane selection
* scrolling
* resizing
* mouse interaction

---

## Neovim Optimization

### ESC Delay Fix

```tmux
set -sg escape-time 10
```

Improves ESC responsiveness inside Neovim.

---

## Plugins

### Installed Plugins

| Plugin                         | Purpose                                     |
| ------------------------------ | ------------------------------------------- |
| tmux-plugins/tpm               | Plugin manager                              |
| christoomey/vim-tmux-navigator | Seamless navigation between tmux and Neovim |
| wfxr/tmux-power                | Statusline theme                            |
| tmux-plugins/tmux-resurrect    | Save and restore sessions                   |
| tmux-plugins/tmux-continuum    | Automatic session persistence               |

---

## Session Persistence

Sessions are automatically:

* saved
* restored
* continued after reboot

using:

* tmux-resurrect
* tmux-continuum

---

## Reload Configuration

Reload tmux config without restarting session:

```text
PREFIX + r
```

---

## Notes

### Current Path Splitting

New panes automatically open in:

```text
#{pane_current_path}
```

which preserves working directory context.

---

## Workflow

This tmux setup is designed for:

* terminal-heavy workflow
* Neovim development
* persistent workspaces
* multi-pane productivity

---

## Related

* Zsh
* Neovim
* Ghostty
* WezTerm
