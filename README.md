# An SDL2 Wrapper to run Pico-8 natively on the Miyoo Mini/Miyoo Mini Plus.
A wrapper to run Pico-8 Native on the Miyoo Mini/Miyoo Mini plus.

### v0.8
- Display mode shortcut added -> SELECT + R1 will toggle between scaled, fullscreen, native output (384x384 from pico-8) (which also has its own bezel selection).
- Frame time adjustments.
- "border" -> "bezel" - folder name replaced, all references replaced to make it a more relatable name.
- Added "integer_scaled" bezel directory, added "standard" bezel directory.
- Removed "def_" version of bezels logic.
- Redraw mouse icon if overlay is changed while in mouse mode

### v0.7.2
- Fix repeating input when swapping to mouse.

### v0.7.1
- Slight performance uplift.

### v0.7
- Fix audio issue when Wi-Fi is disabled/enabled (new launch.sh).
- Add mouse icon by Hoo; mouse icon now shows on screen when L2 is pressed.
- Add min/max CPU values as configurable config options in the performance object in onioncfg.json.
- Added a new default bezel by drkhrse and a remix by xk.
- Add location for bezels/digits to onioncfg.json, defaults to /res/digits and /res/bezels.
- Lowered the wait time in config.txt for frame processing for foreground/background.
- Disabled some debugging for drawing items.
- Add sighandler.

### v0.6.1
- Fix overclock display.

### v0.6
- Housekeeping - removed backup libs/unrequired libs.
- Added bezel scrolling with SELECT + LEFT/RIGHT - saves on graceful exit, reads on good load.
- Updated JSON saving function to save it in PRETTY format instead of inline for readability.
- Added some default bezels/bezels for examples.

### v0.5
- Fixed mouse bounds so it can't go into the screen bezel edges (pico window area = 240x240).
- App name for applist changed to `Pico-8`.
- Ceiling of CPU clock set to `1700` after feedback.
- Added basic overlay/bezel for proof of concept (delete it or rename/edit to whatever).
- Guard against missing onioncfg.json (set all defaults for mouse, keyboard, cpuclock).
- Guard against missing res (digits/bezels).
- Added CPU clock indicator and bezel refresh logic.
    - CPU clock will decay over time and stop being drawn.
    - Bezel will be permanent (upcoming keybinds for this).
- Removed carts from the package.

### v0.4
- Housekeeping of package (removed res dirs).
- Swapped A & B.
- X now brings up the in-game menu and allows to exit when at menu (instead of menu btn).
- L2 now acts as a toggle for mouse mode.
- Exit gracefully shortcut is now select + menu.
- All keys not used by single-player games bound to D.
- Select + L1 now restarts the current cart.
- Added shortcut to raise/lower the CPU clock with Select + UP/DOWN and option in onioncfg.json with max 100 increment size, default 25.
- Changed CPU clock ceiling to 1800 and floor to 600.
- Lowered default clock to 1300.

### v0.3
- neon_memcpy ASM added for video performance uplift.
- Mouse support added -> `Select + A` to enter mouse mode, `Start` to exit (config in cfg/onioncfg.json for scaling/acceleration/increment values etc).
- Quit hotkey added -> `Select + Start` - Can't use Select + Menu as pico seems to release the key occasionally and it locks up.
- Overclocking added -> configure currently in the cfg/onioncfg.json file - set to 1400 by default.
- Keybinds added but don't edit these as there's no way to rebind within pico8 currently (needs console support).
- Again, if you dropped into the console you'll have to quit out. The console ignores any input I send to it currently (apart from enter/return).
- Mount bind added to launch.sh to bind your Roms/PICO location to the carts directory.

### v0.2
- Audio.

