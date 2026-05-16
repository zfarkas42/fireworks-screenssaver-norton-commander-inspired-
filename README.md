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
- A C++ compiler to build from source (see below)

---

## Building from Source

### Option A — Visual Studio Build Tools (recommended)

1. Download and install **Visual Studio Build Tools** (free):
   https://visualstudio.microsoft.com/visual-cpp-build-tools/
   During install, select: **Desktop development with C++**

2. Open **Developer Command Prompt for VS 2022** from the Start menu

3. Navigate to the folder containing `fireworks_v2.cpp`:
   ```
   cd C:\path\to\your\folder
   ```

4. Compile:
   ```
   cl /O2 /EHsc fireworks_v2.cpp user32.lib gdi32.lib /link /SUBSYSTEM:WINDOWS /OUT:fireworks.scr
   ```

### Option B — MinGW / g++

1. Install **MSYS2**: https://www.msys2.org/

2. Inside the MSYS2 terminal, install MinGW:
   ```
   pacman -S mingw-w64-x86_64-gcc
   ```

3. Compile from the MinGW64 shell:
   ```
   g++ -O2 -o fireworks.scr fireworks_v2.cpp -lgdi32 -luser32 -mwindows
   ```

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

## Customisation

All tuneable values are constants at the top of `fireworks_v2.cpp`:

| Constant | Default | Effect |
|---|---|---|
| `MAX_ROCKETS` | 8 | Maximum simultaneous rockets |
| `MAX_PARTICLES` | 350 | Maximum simultaneous particles |
| `PARTICLE_LIFE` | 120 | How long sparks live (frames) |
| `GRAVITY` | 0.07 | Gravitational pull on particles |
| `TIMER_MS` | 16 | Frame interval (~60 fps) |
| `TRAIL_LEN` | 10 | Length of rocket smoke trail |
| `FLASH_LIFE` | 8 | Duration of explosion flash (frames) |

Change any value, recompile, and reinstall.

---

## Screensaver Command Line Flags

Windows passes these flags automatically — you don't need to use them manually:

| Flag | Behaviour |
|---|---|
| `/s` | Run fullscreen (normal screensaver mode) |
| `/p <hwnd>` | Preview in the Screen Saver Settings dialog |
| `/c` | Show configuration dialog |

---

## Background

**Norton Commander** was a legendary two-panel file manager for DOS, developed by Peter Norton and hugely popular in the late 1980s and early 1990s. Among its features was a graphical fireworks screensaver that activated after a period of inactivity — one of the most fondly remembered screensavers of the DOS era.

This project recreates that screensaver as a proper native Windows `.scr` file, with faithful physics and colours while adding modern touches like double explosions and variable spread modes.

---

## License

Do whatever you like with this. No warranties. Enjoy the show. 🎆
