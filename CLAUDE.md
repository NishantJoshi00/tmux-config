# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a tmux configuration repository containing a single, well-organized `tmux.conf` file. The configuration focuses on performance optimization, visual clarity, and workflow efficiency.

## Configuration Architecture

### Core Design Philosophy
- **Performance-first**: High history limits (100,000 lines) with aggressive resizing for optimal memory usage
- **Minimalist UI**: Clean status bar with essential information only (time, session ID, window status)
- **Vi-mode integration**: Uses vi key bindings for copy mode with macOS clipboard integration via `pbcopy`

### Key Configuration Sections
1. **Core Optimization** (lines 1-3): Memory and resizing settings
2. **Status Bar & Tabs** (lines 5-17): Visual appearance and update intervals  
3. **Pane Management** (lines 19-33): Borders, mouse support, and copy mode
4. **System Integration** (lines 35-49): Terminal integration and indexing
5. **Custom Bindings** (lines 51-59): Reload and navigation shortcuts

## Common Operations

### Testing Configuration Changes
```bash
# Reload tmux configuration
tmux source-file ~/.tmux.conf
# Or use the built-in binding: Ctrl-b + r
```

### Key Bindings (Custom)
- `Ctrl-b + r`: Reload configuration with confirmation message
- `Ctrl-b + C`: Clear pane history and screen
- Copy mode uses vi bindings (`v` to select, `y` to copy to clipboard)

## Development Notes

- The configuration uses 1-second status updates for real-time feedback
- Mouse support is enabled for modern terminal workflows
- Pane and window indexing starts at 1 (not 0) for intuitive navigation
- Optional Alt-arrow navigation is commented out but available (lines 56-59)
- All visual bells and activity notifications are disabled to prevent distractions