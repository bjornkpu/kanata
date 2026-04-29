# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal kanata keyboard configuration. Kanata is a cross-platform keyboard remapping tool using S-expression syntax. See <https://github.com/jtroo/kanata>.

## Key Files

- `kanata.kbd` - Active config (used w/ kanata_gui.exe)
- `documentation/config.adoc` - Official config guide (from kanata docs)
- `documentation/config_examples/` - Reference configs
- `keymap-cheatsheet.html` - Visual cheatsheet

## Running Kanata

```bash
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
- `layer-while-held <layer>` / `layer-switch <layer>` - layer switching (toggle vs permanent)
- `C-` `A-` `S-` `M-` prefixes for Ctrl/Alt/Shift/Meta chords
- `AG-` prefix for AltGr combinations (used heavily for Nordic symbol access)
- `lrld` - live reload config
- `macro` - sequence of keypresses with optional delays

## Windows & Nordic Notes

- `kanata_gui.exe` uses browser event.code key names
- `windows-altgr cancel-lctl-press` in defcfg mitigates AltGr issues on Windows
- `process-unmapped-keys yes` needed for tap-hold to work with unmapped keys
- Nordic layout: many programming symbols require `S-` or `AG-` combos (e.g., `S-7` = `/`, `AG-7` = `{`, `AG-8` = `[`)
- `102d` = IntlBackslash key (between lsft and z on Nordic ISO)

## Current Config Structure

Five layers:

- **base** - Main layer; Caps=Esc, Space=nav on hold, Grave=system on hold, AltGr=symbols on hold
- **navigation** - Arrows on HJKL (vim-style), F-keys on number row, media on top-left, programming symbols across bottom rows, pgup/pgdn/home/end
- **symbols** - AltGr number row passthrough, markdown code block macro on `g`
- **system** - Config utilities (1=live reload, 2=gaming mode switch)
- **gaming** - Pure passthrough, no remaps; Grave switches back to base

## Design Constraints

- Must remain usable on standard keyboards (no extreme muscle memory conflicts)
- Must allow others to use the computer (shared computer)
- Gaming layer = raw passthrough for game compatibility
- Home row mods are defined but commented out due to misfire issues
- Chords (`defchordsv2`) are defined but commented out (got in the way)

## Hardware Context

Nordic ISO layout on Logitech MX Mechanical Mini (compact, no numpad). `IntlBackslash` (`102d`) key exists between lsft and z.
