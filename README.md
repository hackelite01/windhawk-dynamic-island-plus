# windhawk-dynamic-island-plus

**Dynamic Island Plus** is a [Windhawk](https://windhawk.net) mod: a Dynamic
Island style pill overlay for Windows that reacts to media, notifications,
clipboard, battery and more.

## What this version adds

- **Nine more themes**, on top of the original eight: Glass Blue, Midnight
  Violet, Aurora, Crimson, Sunset, Ocean, Cyber Neon, and the light themes
  Sakura and Mint.
- **Right-click Position menu**: six anchor positions (top or bottom, left,
  center or right), 20 px nudges left, right, up and down, and a reset. The
  choice is remembered and overrides the Position and Offset settings until you
  reset it.
- **Battery in the idle strip**: the collapsed island shows the battery
  percentage after the clock and weather, with a lightning bolt while charging.
  Laptops only, and it can be turned off in Mod Settings > Modules.
- **Auto-expand duration**: choose how long the island stays expanded after a
  track change (1 to 30 seconds; it was fixed at 5).
- **Full title on the collapsed pill**: always shows the song title on the
  collapsed media pill and widens the pill to fit it instead of scrolling it, up
  to a maximum width you set. While on, lyrics no longer replace the title on the
  collapsed pill. Both media options answer issue #99 of the original project.

## What is unchanged

Everything else is the original code. The only edits to existing code are:

- the theme submenu's command ids moved from 20.. to 70.., so the longer theme
  list does not overlap the timer and tray menu commands;
- two small hooks in settings loading so the saved position and nudges are
  applied;
- a battery slot added to the idle strip's width measuring and painting code;
- the fixed 5 second auto-expand window now reads a setting, and the collapsed
  media pill's width can follow the title's length.

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
- `LICENSE-original`: MIT license of the project this mod is built on,
  Copyright (c) 2026 devcode90. Its notice is also kept in a comment in the mod
  file, as the license requires.
- `LICENSE`: MIT for the additions made in this repo.

## Credits
Dynamic Island Plus is built on
[Dynamic Island for Windows](https://github.com/devcode90/Dynamic-Island-for-Windows)
v1.3.1 by **devcode90**, used under the MIT License, together with the work of
its contributors listed in the mod's own readme. The themes, Position menu,
battery strip, auto-expand duration and full-title option added here are by
**hackelite01**.

## Submitting to the Windhawk catalog
Open a pull request to `ramensoftware/windhawk-mods` that adds only
`mods/dynamic-island-plus.wh.cpp`. The `@github` line in the file must match the
username of the person opening the pull request. The catalog may be reluctant to
accept a modified copy of a mod that is already listed; sending the themes and
position menu upstream to the original author is the alternative.

## Status
v1.0.0. The themes and the Position menu have been compiled and run. The
battery slot is newly added and still being tested. Report problems with your
Windows version and a screenshot.
