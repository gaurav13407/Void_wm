# void_wm

A Wayland compositor built from scratch in Rust using [Smithay](https://github.com/Smithay/smithay).

Inspired by Hyprland, void_wm aims to be a minimal, fast, and hackable compositor
for people who want to understand and control every part of their desktop environment.

## Status

Early development — core compositor infrastructure in progress.

- [x] Project structure
- [ ] Wayland backend
- [ ] Output/monitor initialization  
- [ ] Wallpaper rendering
- [ ] Input handling
- [ ] Window management
- [ ] Keybindings
- [ ] XWayland support

## Architecture
```
void_wm/
├── src/
│   ├── main.rs          # Entry point, event loop
│   ├── state.rs         # Global compositor state
│   ├── backend/
│   │   ├── mod.rs
│   │   ├── winit.rs     # Nested compositor backend (dev/testing)
│   │   └── udev.rs      # Real hardware backend (production)
│   ├── handlers/
│   │   ├── mod.rs
│   │   ├── compositor.rs
│   │   ├── output.rs
│   │   └── input.rs
│   └── render/
│       ├── mod.rs
│       └── wallpaper.rs
└── assets/
    └── wallpaper.jpg
# Void_wm
