
## Installation Steps

Follow these exact steps used in your setup for universal compatibility on Windows 11+ systems with AutoHotkey v1.1:

1. Download and install AutoHotkey v1.1 from the official site.
2. Save `SmartVoiceMouse.ahk` from the repository to your desktop.
3. Press `Win+R`, type `shell:startup`, and press Enter to open the Startup folder.
4. Copy `SmartVoiceMouse.ahk` into the Startup folder.
5. Restart Windows—the script auto-launches on boot.[3]

Test by holding both mouse buttons (L+R) for 300ms to toggle Voice Access (Win+Ctrl+S hotkey), confirmed by on-screen tooltip.[4]

## Core Features

- **Voice Access Toggle**: Hold LButton + RButton for 300ms to activate/deactivate Windows Voice Access. Uses `^#{s}` shortcut for seamless integration.[5]
- **Chrome Launcher**: Hold RButton alone for 700ms to open Google Chrome (no LButton pressed).
- **Tray Menu**: Right-click tray icon for manual Voice Access toggle or script exit.
- **Startup Automation**: Persists across reboots via shell:startup placement.[6]

Note: Right-click long-press for 1500ms mentioned is not implemented; current code uses 700ms for Chrome only.[7]

## Voice Access Commands

Once activated (say "Voice access wake up" or "Unmute"), use these Windows 11 native commands hands-free:

| Category | Examples |
|----------|----------|
| Basic Controls | "Click", "Right click", "Double-click", "Press Enter", "Scroll up" [5] |
| App Management | "Open Chrome", "Switch to Notepad", "Minimize window", "Go to desktop" [5] |
| Text Editing | "New line", "Select that", "Delete word", "Bold that", "Caps hello world" [5] |
| Navigation | "Show numbers", "Move mouse right", "Show grid", "Go to top" [5] |
| Punctuation | "Period", "Comma", "Open quotes", "Question mark" [5] |

Full list available via "What can I say?" command. Deactivate with "Voice access sleep" or "Mute".[5]

## Customization Guide

Edit timings in the script header: `holdThreshold := 300` (both buttons), adjust `700` in `CheckRightHold` for Chrome. Add features like 1500ms RButton hold by extending the timer logic. Fork the repo, test changes, and submit pull requests. Users can create personalized shortcuts matching their workflow.

