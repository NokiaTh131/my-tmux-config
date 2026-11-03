# my-tmux-config

My tmux setup, using [TPM](https://github.com/tmux-plugins/tpm) for plugins.

## Install

```sh
# 1. Clone the config
git clone https://github.com/NokiaTh131/my-tmux-config ~/.config/tmux

# 2. Install TPM (the config loads it from ~/.tmux/plugins/tpm)
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm

# 3. Start tmux, then press prefix + I (capital i) to install plugins
tmux
```

Requires tmux 3.1+ (for `~/.config/tmux/tmux.conf` support).

## Key bindings

The prefix is **`Ctrl+s`** (instead of the default `Ctrl+b`).

| Keys | Action |
| --- | --- |
| `prefix` + `h` / `j` / `k` / `l` | Move to the pane left / down / up / right |
| `prefix` + `Ctrl+s` | Send a literal `Ctrl+s` to the app inside (e.g. save in vim) |
| `prefix` + `I` | Install plugins (TPM) |
| `prefix` + `U` | Update plugins (TPM) |
| `prefix` + `Ctrl+r` | Restore session (tmux-resurrect) |
| `Ctrl+h` / `j` / `k` / `l` | Move between tmux panes and Vim splits (vim-tmux-navigator, no prefix) |

In copy mode (`prefix` + `[`), vi keys are enabled:

| Keys | Action |
| --- | --- |
| `v` | Begin selection |
| `y` | Copy selection and exit copy mode |

## Settings

- **Mouse** is on (click panes, drag to resize, scroll).
- **Vi mode keys** in copy mode.
- **Terminal**: `tmux-256color`, with true color enabled for WezTerm.

## Plugins

| Plugin | What it does |
| --- | --- |
| [tpm](https://github.com/tmux-plugins/tpm) | Plugin manager |
| [tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect) | Save/restore sessions across restarts (also restores Neovim sessions) |
| [tmux-continuum](https://github.com/tmux-plugins/tmux-continuum) | Auto-saves sessions and auto-restores on tmux start |
| [vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator) | Seamless navigation between tmux panes and Vim/Neovim splits |
| [tmux-yank](https://github.com/tmux-plugins/tmux-yank) | Copy to the system clipboard |
| [tmux-monokai-pro](https://github.com/maxpetretta/tmux-monokai-pro) | Monokai Pro theme |

## Notes

The `plugins/` directory is git-ignored; TPM installs plugins itself.
