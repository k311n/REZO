# Changelog

## 5.1.1 — 2026-11-01
- **Four new styles** in Look (same layout and features, only the look changes; each comes with its own palette):
  - **Nightshade** (RU «для альтух») — black, deep wine and violet, silver; sharp corners, double frames, crosses, a chain in the title bar, fishnet and a cobweb in the background, serif titles
  - **Riot** (RU «ыы женщины») — punk zine: dirty graphite, acid orange + electric cyan, torn paper edges, masking tape, stickers, a marker title with a highlighter stroke
  - **Pick Me** (RU «я пикми») — pink background, light pink cards, soft rounded corners, bows and hearts, falling heart petals, script title
  - **Sugar Bunny** (RU «я пикминяшка») — bubblegum pink to lavender, maximum rounding, bubble-letter title, sparkles and bubbles, stitched cards
- Four matching palettes (8 in total). Picking a new style switches to its palette; going back to an old style from a new palette drops it (Acid → Acid Chapel, Kova → Kova, others → Violet). Any palette can still be picked by hand
- Look shows 9 style cards in a 3×3 grid (2 columns with scrolling in S/M)
- The feedback form follows the new styles; the game profile window is a bit taller so OK/Cancel are not cut off
- Defaults are unchanged (new configs start with Acid Chapel); old settings are kept; an unknown style falls back to Acid Chapel, an unknown palette to the style's own

## 5.0.1 — 2026-11-01
- **Feedback form restyled:** the «Write feedback» window now follows the app's style (Modern, Kova, Minimal, Retro, Acid Chapel) — fonts, colors, cut corners, focus highlight, DPI scaling; the type is chosen with three buttons instead of a drop-down. Texts, limits and what is sent are unchanged
- Fixed: the old feedback form crashed on the Violet palette
- **Sharper icon:** redrawn with supersampling, ICO now holds 16/20/24/32/40/48/64/96/128/256 px (256 as PNG); the installer refreshes the Windows icon cache so the desktop shortcut shows the new icon right away

## 5.0 — 2026-11-01
- **Game profiles:** per game — resolution slot (or don't change), NVIDIA saturation (or don't change), night gamma on/off/don't change. Popular presets: Valorant, CS2, Rust, Dota 2; add, edit, delete in Settings → Game profiles (up to 8)
- **Four trigger modes, Off by default:** Launch via REZO (▶ on a profile or a desktop shortcut `REZO.exe --play N`, recommended), Process (process name list every 2 s), Focus (focused window, riskiest — warned in «?»), WMI (instant start/stop events; without admin rights REZO says so and falls back to Process)
- Everything is restored exactly as before (resolution, saturation, gamma) when the game closes, when REZO exits, and on the next start after a crash
- Anti-cheat rules in code: only process names from a Toolhelp snapshot, no process handles, memory, hooks, overlays, input or messages to game windows; games are started via ShellExecute without a handle. Second-instance messages now go only to REZO's own windows instead of a broadcast
- README: Anti-cheat section (EN + RU)

## 4.0 — 2026-10-31
- **Start in 30 seconds:** first-start guide in 3 short steps with ready sets — Stretched (1280×960, 1440×1080, 1024×768) or Native + 1080p. Only modes your monitor supports, keys Ctrl+Alt+F1…F3
- **Safe switch:** a resolution applied for the first time asks «Keep?» with a 10 s countdown; Enter keeps, Esc or no answer puts the old one back. Toggle in Settings → Behavior (on by default)
- Shorter hint under the slots; tip about games in exclusive fullscreen swallowing hotkeys
- Acid Chapel polish: brighter footer and labels, title no longer repeats the lime accent
- Settings files: missing hotkey keys get their defaults one by one (a partial ini no longer wipes hotkeys), junk key codes are dropped, `1920×1080` with «×» is understood, a broken palette value falls back to the style's own palette
- Updater compares versions by numbers (4.0 > 3.16)
- New configs open in size L
- Feedback in About: «Idea» / «Thanks» open a prefilled GitHub issue; «Write feedback» sends type, message and optional contact to a Google Form (TLS 1.2, once a minute max). Only REZO and Windows versions are attached, nothing else

## 3.16 — 2026-10-31
- New default style **Acid Chapel**: black, acid lime and neon magenta, 45° cut corners, scanlines, magenta glare, "+" marks, glitchy title, Bahnschrift + Consolas Bold. Same layout and features as before, only the look changed
- Acid Chapel palette; new configs start with Acid Chapel style + palette, existing settings are kept
- Acid Chapel is the first card in Look; all other styles, palettes and Custom work as before
- New icon: cut-corner tile with a lime frame and a bold R with a magenta shadow (app, tray and installer)

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
