# Install

## Download

[Releases](https://github.com/jtroo/kanata/releases)

### Variants

- **x64** vs. arm64: Select x64 if your machine's CPU is Intel or AMD. If ARM, use arm64.
- tty vs **gui**: tty runs in a terminal, gui runs as a system tray application.
- **cmd_allowed** vs. not: cmd_allowed allows the cmd actions; otherwise, they are compiled out of the application.
- **winIOv2** vs. wintercept: winIOv2 uses the LLHOOK and SendInput, wintercept uses the Interception driver.

> kanata_windows_gui_winIOv2_cmd_allowed_x64.exe

## How to run on startup - Windows

Source: [https://github.com/jtroo/kanata/discussions/193](https://github.com/jtroo/kanata/discussions/193)

1. Install katana gui exe
2. Make shortcut of it
3. Go to the startup folder, press `windows + r` for run, and type this: `shell:common startup`
4. Put the shortcut in startup folder
