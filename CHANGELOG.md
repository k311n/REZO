# Changelog

## 3.15 — 2026-10-31
- Check for updates: Settings → Updates. Asks GitHub Releases (k311n/REZO) for the latest version and updates in one click: installed copy downloads and runs the silent installer, portable copy downloads REZO.exe, swaps itself and restarts
- Downloads only from github.com, the file must pass Authenticode and be signed by the same k311n.intg certificate, otherwise the update is cancelled
- "Check on startup" (off by default, tray notice when a new version is found). No other network requests, no telemetry
- Custom palette in Look: background, cards, accent, accent 2, text and muted colors, picked with the Windows color dialog, applied live, "Reset" button
- Fixes: an empty or unreadable REZO.ini now starts with default hotkeys and slots; settings are saved atomically (temp file + replace)
- Fixes: a failed saturation change now shows a status / tray warning; gamma failure also warns from the tray
- Slot name field: long names scroll and stay inside the field, emoji are not cut in half, Ctrl+V pastes, global hotkeys are paused while typing
- Assigning a combo only takes it from visible/enabled actions and tells you it was taken
- Autostart (--tray) no longer pops up the window of an already running REZO
- Notifications are not shown while the REZO window is open
- "Reset all settings" in Settings → Extra

## 3.14 — 2026-10-31
- 5 tabs in a fixed order: Resolution, Color, Look, Settings, About. No dropdown menu: icons expand into a labeled pill on hover
- Tab menu position: top / left (default) / right / bottom
- About tab with links (Made by Poganka · For Sakume)
- Color tab reworked: collapsible groups, digital vibrance on/off, per-resolution saturation, saturation hotkey X ↔ Y, presets group, "night graphics for Rust" toggle with its own hotkey, «?» on every option
- Settings grouped into collapsible sections
- "Minimize to tray on close" option (off by default, asked in the installer)
- Window: resizes by edges and corners, native maximize, Aero Snap, Win11 Snap Layouts, text scales with the window size
- First-start guide (shown once)
- Slots can be renamed; the name is shown in the Resolution list, tray menu and quick access (empty = resolution and Hz)
- Bolder fonts, more readable labels in the Violet palette; new configs start with Modern style + Kova palette
- The kitty is switched off for now (in development)

## 3.13 — 2026-10-31
- Immediate-mode UI: 4 styles × 2 palettes, S/M/L window sizes, up to 8 slots, cycle hotkey
- Autostart, auto text scaling per resolution (DPI), tray (left click opens the window)
- New icon, installer / uninstaller (Program Files, shortcuts, Apps entry, certificate, gamma unlock)
- Color tab: NVIDIA vibrance presets, saturation per slot, night gamma with unlock button
- Signed build (CN=k311n.intg)

## 2.0
- Violet theme, falling dots, tabs, monitor picker, RU/ENG, kitty v1
- Signed with a self-signed certificate

## 1.0
- First version: one .bat with embedded C#, 3 slots + default, global hotkeys, settings in REZO.ini
