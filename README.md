# windhawk-dynamic-island-plus

**Dynamic Island Plus** is a [Windhawk](https://windhawk.net) mod: a Dynamic
Island style pill overlay for Windows that reacts to media, notifications,
clipboard, battery and more. It is based on
[Dynamic Island for Windows](https://github.com/devcode90/Dynamic-Island-for-Windows)
v1.3.1 by devcode90, used under the MIT License.

## What this version adds

- **Nine more themes**, on top of the original eight: Glass Blue, Midnight
  Violet, Aurora, Crimson, Sunset, Ocean, Cyber Neon, and the light themes
  Sakura and Mint.
- **Right-click Position menu**: six anchor positions (top or bottom, left,
  center or right), 20 px nudges left, right, up and down, and a reset. The
  choice is remembered and overrides the Position and Offset settings until you
  reset it.
- **Alt + drag to move**: hold Alt and drag the island with the left mouse
  button to place it anywhere. The new spot is saved when you let go. A drag only
  starts when Alt is held, so the island's normal clicks are unchanged.

## What is unchanged

Everything else is the original code. The only edits to existing code are:

- the theme submenu's command ids moved from 20.. to 70.., so the longer theme
  list does not overlap the timer and tray menu commands;
- two small hooks in settings loading so the saved position and nudges are
  applied.

## Install
1. Open Windhawk and choose **Create a new mod**.
2. Paste the contents of `mods/dynamic-island-plus.wh.cpp` over the template.
3. Click **Compile Mod**. The file is large, so compiling takes a while.
4. **Turn off the original Dynamic Island mod first.** Both use the same window
   and the Ctrl+Alt+Space shortcut. Settings are stored per mod, so yours do not
   carry over.

## Notifications
Turn on **Settings > Privacy & security > Notifications > "Let apps access your
notifications"**. The island waits about 30 seconds after starting before it
connects to notifications.

## Licenses
- `LICENSE-original`: the original project's MIT license,
  Copyright (c) 2026 devcode90. Its notice is also at the top of the mod file.
- `LICENSE`: MIT for the changes made in this repo.

## Submitting to the Windhawk catalog
Open a pull request to `ramensoftware/windhawk-mods` that adds only
`mods/dynamic-island-plus.wh.cpp`. The `@github` line in the file must match the
username of the person opening the pull request. The catalog may be reluctant to
accept a modified copy of a mod that is already listed; sending the themes and
position menu upstream to the original author is the alternative.

## Status
v1.0.0. The themes and the Position menu have been compiled and run; Alt+drag
is newly added and still being tested. Report problems with your Windows
version and a screenshot.
