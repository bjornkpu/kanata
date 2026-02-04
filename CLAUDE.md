# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal kanata keyboard configuration files. Kanata is a cross-platform keyboard remapping tool using S-expression syntax.

## Key Files

- `kanata.kbd` - Active config (used w/ kanata_winIOv2.exe or kanata_gui.exe)
- `documentation/config.adoc` - Official config guide (from kanata docs)
- `documentation/config_examples/` - Reference configs

## Running Kanata

```bash
# Run with specific config
kanata_winIOv2.exe -c kanata.kbd
kanata_gui.exe -c kanata.kbd

# Force exit: hold Lctrl+Space+Esc simultaneously
```

## Config Syntax Essentials

- Comments: `;;` single-line, `#| ... |#` multi-line
- Required sections: `defsrc` (keys to intercept), `deflayer` (at least one)
- Aliases: defined in `defalias`, referenced as `@aliasname`
- Variables: defined in `defvar`, referenced as `$varname`
- Transparent key: `_` (use base layer behavior)
- No-op key: `XX` (disable key)

## Common Actions

- `tap-hold <tap-timeout> <hold-timeout> <tap-action> <hold-action>` - tap/hold behavior
- `layer-toggle <layer>` / `layer-switch <layer>` - layer switching
- `C-` `A-` `S-` `M-` prefixes for Ctrl/Alt/Shift/Meta chords
- `lrld` - live reload config

## Windows Notes

- Use `kanata_winIOv2.exe` for browser event.code key names
- `windows-altgr cancel-lctl-press` in defcfg mitigates AltGr issues
- `process-unmapped-keys yes` needed for tap-hold to work with unmapped keys

## Current Config Structure

- **base** - Main layer; caps->Ctrl, space->nav layer on hold, grave->menu on hold
- **navigation** - Arrows on HJKL, F-keys on number row, media controls on ZXCVB, pgup/pgdn/home/end
- **menu** - Config utilities (1=live reload)

## Hardware Context

Nordic layout on Logitech MX Mechanical Mini. `IntlBackslash` key exists between lsft and z.
