# .XPANDER

**A lightweight, high-performance Windows text expander and productivity utility.**  
Native Rust and Slint UI for Windows 11 ARM64 and Windows 10/11 x86_64.

🌐 [Website](https://www.dotxpander.com) · 💬 [Support](https://www.dotxpander.com/support/) · 📦 [Releases](https://github.com/ThMoJe/dotXPANDER-Releases/releases) · 🐛 [Issues](https://github.com/ThMoJe/dotXPANDER-Releases/issues)

dotXPANDER is a native Windows productivity tool designed for speed, low resource usage, and seamless compatibility with modern Windows applications. It runs as a single, highly optimized native binary that requires no background runtime, uses minimal memory, and draws 0.0% CPU while idle.

## Installation

### Option A: Microsoft Store (Recommended)

Install directly from the [Microsoft Store](https://apps.microsoft.com/detail/9NCXXM1SKCW4) with automatic background updates, or via PowerShell:

```powershell
winget install ".XPANDER" --source msstore
```

### Option B: Windows Package Manager (Winget)

For standalone desktop installer deployment (including environments without Microsoft Store access):

```powershell
winget install aiVOLUTION.dotXPANDER
```

### Option C: Windows Installer

Download the latest setup executable (`dotXPANDER-x64-Setup.exe` or `dotXPANDER-arm64-Setup.exe`) from the [Releases](https://github.com/ThMoJe/dotXPANDER-Releases/releases) tab.

The setup wizard installs to your local user directory (no Administrator/UAC prompt required) and supports automated silent deployment.

### Option D: Portable ZIP

Download the portable zip archive from the [Releases](https://github.com/ThMoJe/dotXPANDER-Releases/releases) tab and extract it to a directory of your choice. When launched without installation, dotXPANDER runs in Portable Mode, storing its configuration alongside the executable. As encryption and Cloud folder synchronization requires writing to Windows registry and Credential Manager, both are disabled in portable mode.

## Features

- **Snippet Expansion**: Expands trigger strings instantly as you type (Immediate Mode) or on demand using a configurable keyboard shortcut (Hotkey Mode, default: `Ctrl + Alt + X`).
- **Low Resource Footprint & Automatic Memory Buffer**: Zero-allocation ring buffer matching engine (~4.6 MB RAM, 0% idle CPU) that automatically sizes its capacity (`32..=256` characters) to match your longest active snippet trigger on load, save, and sync without restarting.
- **Rich Text & Image Snippets**: Paste formatted text (`HTML Format`, `RTF`) or screenshots/images directly into snippet replacements with Paste-and-Lock (compressed `.xblob` sidecar container storage, authenticated AES-256-GCM encrypted when Configuration Encryption is enabled).
- **Highlight & Freeze (`Ctrl + CapsLock` -> `Freeze as Snippet...`)**: Capture selected plain text, rich formatting (`HTML Format`, `RTF`), or images directly from any application into a compact Freeze dialog, or press `Ctrl + S` on any entry in the `Clipboard` Search Palette tab. Enter a trigger and press `Enter` to save immediately (including encrypted `.xblob` storage for rich text or images), sync the ring buffer, and return focus to your active app.
- **Unified Search Palette (Snippets & Clipboard History)**: Press the `.XPANDER` hotkey with no trigger typed (or `Ctrl + CapsLock` with no text selected) to open a floating, searchable palette to select and inject snippets or recent clipboard items. Supports live multi-word search, live hot-reloading while open when synced updates arrive, image thumbnails with hover preview, and a moveable and 8-way resizable two-tab (`Snippets | Clipboard`) layout with `Tab` / `Ctrl + Tab` switching, `Alt/Ctrl + 1..0` quick-paste slots, `Shift + Enter` plain-text paste, `Ctrl + P` pin, `Ctrl + S` Freeze / Save as Snippet, and `Del` delete.
- **Smart Encrypted Clipboard History**: Opt-in rolling capture of copied plain text, rich text (`HTML Format`, `RTF`), and images, strictly gated on AES-256-GCM Configuration Encryption and Installed Mode. Each PC writes exclusively to encrypted per-machine shards (`clipboard.<machine_id>.{hot,daily,weekly,monthly}.toml` + `clipboard_blobs/<blob_id>.xblob`) merged conflict-free across synced PCs, with configurable retention limits, an opt-in Windows system tray notification (`Notify when new clips arrive from another PC`, count-only and silent, click to open the `Clipboard` palette tab), live storage stats, Clear History, and Rebuild from Blobs in the **Clipboard** settings tab.
- **In-Settings Filter, Sync Reload Chip & Keyboard Reordering**: Live search and filter large snippet collections directly within the Expandings settings tab, reload incoming peer updates non-destructively via the Expandings notification chip without losing unsaved edits, and reorder snippet rows via click controls or `Alt + Up` / `Alt + Down`.
- **Dynamic Snippet Tokens**: Embed live, context-aware placeholders (dates, times, clipboard contents) in your snippets.
- **Case & Space Changer**: Global shortcut (`Ctrl + CapsLock`) opening a 4-theme `.XPANDER` (`Case & Freeze`) popup with right-aligned `[Key]` shortcut badges to transform selected text (uppercase, lowercase, camelCase, Windows filename sanitization, etc.), freeze selected text or images into a new snippet (`Freeze as Snippet...`), or open the `Clipboard` Search Palette tab when no text is selected.
- **Productivity ROI & Time-Saved Strip (`About` Tab)**: Live offline counter tracking cumulative **Expansions**, **Keystrokes Saved**, and **Est. Time Saved** (at 50 WPM = 250 chars/min, with +50 keystrokes credited per image snippet) across **This PC** or **All PCs** in cloud-synced folders, complete with peer handover preservation, hover formula breakdown, and inline-confirmed reset.
- **File Dialog Navigation (Quick Switch)**: Automatically synchronizes standard Windows Open/Save file dialogs to the active File Explorer window.
- **Configurable Storage, Autostart & Encryption**: Save your configuration locally or in a cloud-synced folder (OneDrive, Dropbox, Google Drive) with conflict-free multi-PC synchronization (per-machine replica merge), optional authenticated AES-256-GCM encryption at rest (integrated with Windows Credential Manager and one-time recovery key support), and an in-app **Start .XPANDER with Windows** autostart toggle inside the **For installed version only** settings section (`This PC` / `All PCs` scope badges).
- **4 Built-In Themes**: Switch between **Graphite** (default, Fluent Graphite + `#FFF100` yellow accent), **Daylight Light**, **Fluent Dark**, and classic **aiVOLUTION** (`#0B1F3B` deep navy + `#FFF100` yellow header, as seen across all the User Guide videos).
- **Privacy-Focused**: 100% offline, zero telemetry, secure memory buffer zeroization, zero logging in release builds, and encryption at rest.

## License

dotXPANDER is proprietary software licensed under the [End-User License Agreement](EULA.txt) by aiVOLUTION ApS. All rights reserved.

Third-party open-source components and their respective licenses are documented in [THIRDPARTY.txt](THIRDPARTY.txt).

## Support & Resources

- **Official Product Website**: [https://www.dotxpander.com](https://www.dotxpander.com)
- **Support & Feedback Portal**: [https://www.dotxpander.com/support/](https://www.dotxpander.com/support/)
- **Bug Reports & Feature Requests**: If you encounter an issue or have a feature request, please open a ticket in the [Issues tab](https://github.com/ThMoJe/dotXPANDER-Releases/issues) of this repository.
