# Keyboard Configuration

This repository is the keyboard configuration for my computers. The main software for remapping my keys is `Kanata` but it supports `Kanawin` for automatic layer switching.

## Kanata

<https://github.com/jtroo/kanata>

Improve keyboard comfort and usability with advanced customization. This is a cross-platform software keyboard remapper for Linux, macOS and Windows.

## Kanawin

<https://github.com/Aqaao/kanawin>

Automatic switch layer plugin for kanata.

## My hardware

### Keyboard

- **Model:** Logitech MX Mechanical Mini
- **Layout:** Nordic
- **Form Factor:** Mini (compact layout without numpad)

### Operating System

- **OS:** Windows

### Notes

The Logitech MX Mechanical Mini is a wireless mechanical keyboard with a compact form factor. The Nordic layout includes specific keys for Scandinavian characters (Å, Ä, Ö) which may require special consideration in Kanata configurations.

## Configuration Goals

### Primary Use Case

Software development and heavy typing workload. The configuration aims to improve ergonomics and accessibility without sacrificing portability or usability for others.

### Design Constraints

- **Portability:** Must be comfortable using other standard keyboards without muscle memory conflicts
- **Shared Computer:** Configuration should allow others to use my computer without significant difficulty
- **No Custom Hardware:** Avoiding split keyboards or heavily customized hardware to maintain flexibility
- **Gaming Compatibility:** Need a dedicated gaming layer with no remaps to avoid conflicts in games

### Nordic Layout Challenges

Programming tools and IDEs typically assume US keyboard layout, making common programming characters less accessible:

- Special characters like `/ ( [ { }` require awkward key combinations on Nordic layout
- Standard shortcuts (Ctrl+/, etc.) may not work as expected
- Need to balance programming efficiency with maintaining Nordic characters (Å, Ä, Ö)

### Home Row Mods Considerations

Experimenting with home row modifiers but facing challenges:

- Typing speed causes accidental chord triggers
- Need to adjust timing parameters to distinguish between holds and fast typing
- May require gradual adoption or alternative approach

### Modifier Strategy (Work in Progress)

Developing a consistent philosophy for modifier usage:

- **Win:** OS-level operations (window management, system functions)
- **Ctrl:** Layer activation and key modifications
- **Shift:** Alternative related remaps (contextual variations)
- **Alt:** Application-specific functions
- *Note: This strategy is still being refined and tested*

## Layer Strategy

- **Base Layer:** Modified Nordic layout optimized for programming
- **Gaming Layer:** Pure passthrough with no remaps
- **Additional Layers:** TBD based on evolving needs
