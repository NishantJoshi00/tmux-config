# Tmux Configuration

A clean, performance-optimized tmux configuration focused on minimalism and efficiency.

## Features

- **High Performance**: 100K line history with aggressive resizing
- **Clean Interface**: Minimal status bar showing time, session ID, and active window
- **Vi Integration**: Vi-mode copy with macOS clipboard support
- **Mouse Support**: Modern terminal workflow compatibility
- **Smart Indexing**: Windows and panes start at 1, auto-renumber on close

## Installation

```bash
# Backup existing config (if any)
mv ~/.tmux.conf ~/.tmux.conf.backup

# Copy configuration
cp tmux.conf ~/.tmux.conf

# Reload tmux (if running)
tmux source-file ~/.tmux.conf
```

## Key Bindings

| Binding | Action |
|---------|--------|
| `Ctrl-b + r` | Reload configuration |
| `Ctrl-b + C` | Clear pane history |
| `v` (copy mode) | Begin selection |
| `y` (copy mode) | Copy to clipboard |
| `Escape` (copy mode) | Cancel selection |

## Status Bar Layout

```
12:34 ◆ 06-21        window1  window2        ⎔ session-name
└─ time/date         └─ windows             └─ session ID
```

## Configuration Highlights

- **Escape time**: Set to 0 for responsive key handling
- **Activity monitoring**: Visual cues without audio bells
- **Copy integration**: Seamless clipboard sync with `pbcopy`
- **Terminal titles**: Automatic terminal tab naming

## Customization

Uncomment lines 56-59 to enable Alt-arrow pane navigation:

```bash
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D
```