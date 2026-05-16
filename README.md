# Fireworks Screensaver (Norton Commander inspired)

A faithful recreation of the classic fireworks screensaver from the DOS-era **Norton Commander** file manager, rebuilt as a native Windows screensaver using C++ and the Win32 GDI API.

---

## Features

- 🚀 Multiple rockets launching simultaneously with natural arcing flight paths
- 💥 Bright explosive bursts with a white flash at the explosion center
- 🎆 Four explosion spread modes — tight, wide, normal, and mixed double-ring
- 🎇 Double explosions — some rockets burst twice for extra drama
- ✨ Up to 350 particles per frame with gravity, air resistance, and turbulence
- 🌈 Eight classic colour palettes inspired by the original CGA/EGA era
- ⚫ Pure black background
- 🖥️ All explosions guaranteed to be visible on screen
- ⚡ Lightweight native binary — no runtimes, no dependencies, ~100 KB

---

## Requirements

- Windows 10 or Windows 11
---

## Installation

1. Copy `fireworks.scr` to:
   ```
   C:\Windows\System32\
   ```
   You may be prompted for administrator permission — click Yes.

2. Right-click the Desktop → **Personalize**

3. Go to **Lock screen** → scroll down to **Screen saver**

4. In the dropdown, select **fireworks**

5. Set your desired wait time and click **OK**

---

## Quick Test (without installing)

Double-click `fireworks.scr` to run it immediately in fullscreen.
Press any key or move the mouse to exit.

To test screensaver mode from the command line:
```
fireworks.scr /s
```

---

## Uninstalling

1. Go to Desktop → Personalize → Lock screen → Screen saver
2. Select a different screensaver (or **None**) and click OK
3. Delete `C:\Windows\System32\fireworks.scr`

No registry entries or additional files are left behind.

---

## Background

**Norton Commander** was a legendary two-panel file manager for DOS, developed by Peter Norton and hugely popular in the late 1980s and early 1990s. Among its features was a graphical fireworks screensaver that activated after a period of inactivity — one of the most fondly remembered screensavers of the DOS era.

This project recreates that screensaver as a proper native Windows `.scr` file, with faithful physics and colours while adding modern touches like double explosions and variable spread modes.

---

## License

Do whatever you like with this. No warranties. Enjoy the show. 🎆
