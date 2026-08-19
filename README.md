# CXS Crosshair Studio

> **Build precise crosshairs. Switch them instantly. Keep your games untouched.**

**CXS Crosshair Studio 1.0.0** is a local-first crosshair editor and transparent, click-through overlay for **macOS** and **Windows**. Start with 52 factory presets or create a completely original design with the layered visual editor.

[![Version](https://img.shields.io/badge/version-1.0.0-8b5cf6)](#downloads)
[![macOS](https://img.shields.io/badge/macOS-Intel%20%7C%20Apple%20Silicon-111827)](#downloads)
[![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-2563eb)](#downloads)
[![Privacy](https://img.shields.io/badge/privacy-local--first-16a34a)](#privacy-and-safety)

## Downloads

| Platform | Release | Format |
| --- | --- | --- |
| macOS | [Download CXS 1.0.0](completed/1.0.0.dmg) | Universal DMG for Intel and Apple Silicon |
| Windows | [Download CXS 1.0.0](completed/1.0.0.exe) | Portable x64 EXE for Windows 10 and 11 |

> [!NOTE]
> These development releases are unsigned. macOS may require **Control-click → Open**. Windows may show SmartScreen; choose **More info → Run anyway** only if you obtained the file from a trusted source.

## Highlights

- 🎯 **52 built-in presets** with search, style filters, favorites, and factory reset
- 🧩 **Layered visual editor** for lines, circles, dots, boxes, chevrons, triangles, diamonds, arcs, pluses, and stars
- 🛠️ **Complete transform controls** for position, size, thickness, angle, rotation, opacity, fill, color, ordering, duplication, and deletion
- 🧲 **Precision layout tools** with multi-select, edge alignment, centering, distribution, mirroring, grid snapping, and pixel nudging
- 🔍 **Editor zoom** with live previews and direct canvas manipulation
- 🖥️ **Click-through overlay** with exact centering, per-display calibration, multi-monitor support, and live updates
- ⚡ **Four profiles** with configurable global shortcuts for fast in-game switching
- ↩️ **Familiar commands** for undo, redo, select all, copy, paste, duplicate, save, and delete
- 📦 **Portable presets** through validated `.cxs.json` import/export and QR sharing
- ✨ **Local style assistant** that recommends presets from descriptions such as color, game, size, mood, and aiming style
- 🔒 **Offline-first storage** with automatic migration, atomic saves, and invalid-state recovery

## Custom Studio

Open **Editor → Custom Studio**, add shapes from the tool palette, and combine up to 64 layers into one crosshair.

Each layer supports:

- Shape, position, width, height, thickness, and angle
- Independent color, opacity, outline, fill, and rotation
- Drag-to-move, corner-handle resizing, and rotation handles
- Layer reordering, duplication, deletion, and move-to-front
- Proportional scaling, mirroring, centering, and 15-degree rotation
- Multi-layer alignment, distribution, and five-pixel grid snapping

Save the result as a new preset or update the currently selected preset. Built-in designs can always be restored to their factory values.

## Keyboard Controls

### Editor

| Shortcut | Action |
| --- | --- |
| `Ctrl/⌘ + A` | Select every custom layer |
| `Ctrl/⌘ + C` | Copy selected layers |
| `Ctrl/⌘ + V` | Paste copied layers |
| `Ctrl/⌘ + D` | Duplicate selected layers |
| `Ctrl/⌘ + Z` | Undo |
| `Ctrl/⌘ + Shift + Z` or `Ctrl/⌘ + Y` | Redo |
| `Ctrl/⌘ + S` | Update the active preset |
| `Ctrl/⌘ + Shift + S` | Save as a new preset |
| `Delete` / `Backspace` | Delete selected layers |
| Arrow keys | Nudge selected layers by one pixel |
| `Shift + Arrow` | Nudge selected layers by ten pixels |
| `Escape` | Clear the selection |

Every common command also has an on-screen button.

### In-game Alignment

| macOS | Windows | Action |
| --- | --- | --- |
| `Control + Option + Arrow` | `Control + Alt + Arrow` | Nudge overlay one pixel |
| `Control + Option + Shift + Arrow` | `Control + Alt + Shift + Arrow` | Nudge overlay ten pixels |
| `Control + Option + C` | `Control + Alt + C` | Return to exact center |

Calibration is saved separately for every display.

## Fullscreen and Overlay Behavior

CXS renders the active design in a transparent, focus-free window that ignores mouse input. The overlay automatically hides while the CXS editor is focused, so it never covers the controls.

For games, use **Borderless Fullscreen** or the standard macOS fullscreen mode. A truly exclusive fullscreen surface can block every third-party desktop overlay; switching the game to Borderless Fullscreen restores compatibility.

Use **Settings → Display Alignment → Center** before playing. This clears the selected display's calibration and the active preset offset so the crosshair lands on the exact screen midpoint.

## Profiles and Presets

- Assign any preset to one of four profiles.
- Give each profile a configurable global shortcut.
- Search presets by name, color, shape, or style.
- Favorite frequently used designs.
- Create, rename, update, duplicate, import, export, reset, or delete presets.
- Share validated preset data through a generated QR code.

## Settings

CXS includes launch-at-login, automatic overlay startup, theme selection, overlay opacity, performance mode, recording mode, tournament mode, display selection, and per-monitor calibration.

## Privacy and Safety

CXS is a visual desktop overlay. It does **not**:

- Read game memory
- Inject code into another process
- Modify game files
- Automate aiming
- Control keyboard or mouse input
- Require an internet connection

Presets, profiles, favorites, editor state, settings, and display calibration stay in Electron's local user-data directory. Writes use a temporary file and atomic rename. Invalid state is preserved before safe defaults are restored.

> [!IMPORTANT]
> Overlay permission varies by game and anti-cheat system. Review the rules for the game you play. CXS does not attempt to bypass game restrictions.

## Development

### Requirements

- Node.js 20 or newer
- npm 10 or newer
- macOS for DMG packaging

### Install and Run

```bash
npm install
npm run dev:mac
```

### Verify

```bash
npm test
npm run check
```

### Build Releases

```bash
# Universal macOS DMG
npm run dist:mac

# Windows x64 portable EXE
npm run dist:win
```

Architecture-specific Mac builds are available through `npm run dist:mac:arm64` and `npm run dist:mac:x64`. Generated artifacts are written to `dist/`.

## Project Structure

```text
apps/mac/                  Electron desktop application
packages/crosshair-core/  Shared geometry and canvas renderer
packages/preset-schema/   Shared preset schema and validation
completed/                Ready-to-use 1.0.0 release files
docs/                     Release and verification notes
```

---

**CXS Crosshair Studio 1.0.0** — accurate, flexible crosshairs without changing the game.
