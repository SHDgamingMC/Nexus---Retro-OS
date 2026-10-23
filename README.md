# Nexus OS (1998 Edition) - Retro Operating System Website

A pixel-authentic recreation of a late-90s personal PC desktop built using **pure HTML, CSS, and vanilla JavaScript only**. No external frameworks, no third-party libraries, zero pre-recorded audio assets—powered entirely by native Web APIs and procedural audio synthesis.

> **Designed and developed by Suvin for Nexus competition.**

---

## 🌟 Key Features & Design Details

### 1. 🔤 Authentic Windows 95/98 System Typography
- Uses classic system font stacks: **`MS Sans Serif` (11px, non-antialiased)** and **`Tahoma`** for windows, menus, dialogs, and taskbars.
- **`Fixedsys` / `VT323`** monospaced font for the MS-DOS prompt and Notepad.
- **`Comic Sans MS` / `Times New Roman`** on the 1998 GeoCities personal page.

### 2. 🎨 Handcrafted 32x32 Integer Pixel-Art Icons
Rendered with crisp pixel rendering (`shape-rendering: crispEdges`):
- **My Computer**: 3D beige CRT monitor with screen window, stand, and desktop unit with floppy drive slot and power LED.
- **Recycle Bin**: Beige wire mesh wastebasket with crumpled documents and green recycle icon.
- **MS-DOS Prompt**: Classic black monitor with `C:\>` prompt.
- **Notepad**: Notebook with folded corner, ruled lines, and #2 pencil with eraser.
- **Paint**: Artist's palette with paint dollops and brush.
- **Minesweeper**: Black naval mine with 8 directional spikes, fuse, and sparks.
- **Media Player**: CD-ROM disc with iridescent highlights and music note.
- **The Internet**: Classic blue orbital world icon.
- **Control Panel**: Folder with gear and screwdriver.

### 3. 📏 Authentic Dimensions, Bevels & UI Styling
- **18px Titlebars**: Inactive/active gradient states with bold 11px text and raised 16x14px action buttons (`_`, `□`, `✕`).
- **28px Taskbar**: Sunken tray with live 12-hour clock, sound toggle, modem indicator, CRT toggle, and Start button.
- **Windows 3D Bevels**: Two-tone outset (`#ffffff` light highlight, `#808080` shadow, `#000000` hard edge) and inset styling for fields, buttons, and frames.
- **Selection Box**: 1px dotted outline focus indicator around highlighted desktop icons.

### 4. 💙 Interactive Blue Screen of Death (BSOD)
- Authentic fatal exception `0E at 0028:C0011E36` screen with white text on `#0000aa` blue screen.
- Triggered via `C:\Programs\DO_NOT_CLICK.EXE`, typing `bsod` in the DOS prompt, or clicking the screen to dismiss.

### 5. 📞 Procedural 56k Dial-Up Modem Handshake
- Pure Web Audio API simulation of dialing an ISP: dial tone &rarr; touch-tone DTMF beeps &rarr; carrier answer CED whistle &rarr; V.8 BIS dual-tone warble &rarr; chaotic negotiation noise &rarr; connection chime.

### 6. 📌 Draggable Desktop Sticky Note
- Real yellow sticky note pinned right on the desktop with to-do items from 1998.
- Fully draggable across the desktop workspace with editable content.

### 7. 📖 1998 Human Artifacts & GeoCities
- Suvin's personal diary entries in Notepad (`SUVIN_JOURNAL_OCT98.TXT`), garage band ideas, game cheat codes (Doom II, Warcraft II, SimCity 2000), and Grandma's cookie recipe.
- GeoCities personal cyber lair with hit counters, webring banner, and interactive guestbook saved to `localStorage`.

### 8. 🔊 Procedural Web Audio Synthesizer
- Zero external audio files—procedural sound generation via the Web Audio API.
- Retro startup chord chime, floppy drive stepped seek buzz, error and alert beeps, UI clicks, window open/close sounds, and minesweeper explosions.
- Multi-channel procedural 8-bit chiptune tracker in the Jukebox app with real-time frequency visualizer.

---

## 🪟 Built-in Applications & Utilities

| Application | Description |
|---|---|
| **Pixel Paint** | 16x16, 24x24, and 32x32 canvases with Pencil, Eraser, Fill Bucket, Eye Dropper, Grid toggle, 16-color retro palette, and PNG export. |
| **Minesweeper** | 9x9 grid with 10 mines, 7-segment LED counters, timer, and dynamic smiley face button. |
| **DOS Prompt** | Full interactive CLI with commands: `help`, `dir`, `cat`, `cls`, `echo`, `neofetch`, `dialup`, `snack`, `quote`, `theme`, `matrix`, `calc`, `whoami`, `ver`, `synth`, `bsod`, `reboot`, `beep`. |
| **Media Player** | 3 synthesized chiptune tracks with real-time canvas spectrum visualizer, volume slider, and track list. |
| **NetSurf 1.0** | 90s browser simulation featuring Suvin's Cyber Lair, RetroSearch directory, and interactive guestbook. |
| **Notepad** | Text editor supporting word wrap, status bar line/col counter, virtual disk saving, and local `.txt` download. |
| **Calculator** | Classic pocket calculator with addition, subtraction, multiplication, division, square root, percent, and sign negation. |
| **File Explorer** | Tree navigation, file metadata table, and direct application/document launching from `C:\`. |
| **Control Panel** | Switch between 5 retro color themes (Win95, Cyberpunk, Matrix, Vaporwave, Amiga), 3 wallpapers, CRT scanline overlay, and sound mute. |
| **Help & About** | Displays credits and details: *"Design and developed by Suvin for Nexus competition"*. |

---

## 📁 Project Structure

```
nexus/
├── index.html          # Main desktop markup, windows, menus & dialogs
├── README.md           # Project documentation
├── css/
│   └── style.css       # Complete retro styling, bevels, themes & CRT shaders
└── js/
    ├── app.js          # Main OS initialization, Start Menu, Clock & Shutdown
    ├── audio.js        # Web Audio procedural sound synthesizer & chiptune engine
    ├── browser.js      # NetSurf 1.0 simulated browser & guestbook
    ├── calculator.js   # Retro pocket calculator logic
    ├── desktop.js      # Desktop icons, selection, dragging & context menu
    ├── explorer.js     # Virtual file system & File Explorer tree view
    ├── mediaPlayer.js  # Chiptune player with real-time audio visualizer
    ├── minesweeper.js  # Classic Minesweeper game engine
    ├── notepad.js      # Text editor with file download & storage
    ├── paint.js        # Pixel art paint program with PNG exporter
    ├── settings.js     # Themes, wallpapers & CRT shader controller
    ├── terminal.js     # MS-DOS Command Prompt emulator & CLI commands
    └── windowManager.js# Window dragging, resizing, z-indexing & taskbar sync
```

---

## 🚀 How to Run

No build step, package manager, or compilation required. Open `index.html` directly in any modern browser:

- Double-click `index.html` in your file explorer, **or**
- Serve using any static HTTP server:
  ```bash
  # Python
  python -m http.server 8000

  # Node.js
  npx serve
  ```
