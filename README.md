# .XPANDER

**A lightweight, high-performance Windows text expander and productivity utility.**  
Native Rust and Slint UI for Windows 11 ARM64 and Windows 10/11 x86_64.

🌐 [Website](https://www.dotxpander.com) · 💬 [Support](https://www.dotxpander.com/support/) · 📦 [Releases](https://github.com/ThMoJe/dotXPANDER-Releases/releases) · 🐛 [Issues](https://github.com/ThMoJe/dotXPANDER-Releases/issues)

dotXPANDER is a native Windows productivity tool designed for speed, low resource usage, and seamless compatibility with modern Windows applications. It runs as a single, highly optimized native binary that requires no background runtime, uses minimal memory, and draws 0.0% CPU while idle.

## Installation

### Option A: Windows Package Manager (Winget)

Once Winget submission approval is complete:

```powershell
winget install aiVOLUTION.dotXPANDER
```

*(Package submission is currently undergoing final verification; Windows Installer or Portable ZIP recommended in the interim).*

### Option B: Windows Installer (Recommended)

Download the latest setup executable (`dotXPANDER-x64-Setup.exe` or `dotXPANDER-arm64-Setup.exe`) from the [Releases](https://github.com/ThMoJe/dotXPANDER-Releases/releases) tab.

The setup wizard installs to your local user directory (no Administrator/UAC prompt required) and supports automated silent deployment.

### Option C: Portable ZIP

Download the portable zip archive from the [Releases](https://github.com/ThMoJe/dotXPANDER-Releases/releases) tab and extract it to a directory of your choice. When launched without installation, dotXPANDER runs in Portable Mode, storing its configuration alongside the executable.

## Features

- **Snippet Expansion**: Expands trigger strings instantly as you type (Immediate Mode) or on demand using a configurable keyboard shortcut (Hotkey Mode, default: `Ctrl + Alt + X`).
- **Low Resource Footprint**: Zero-allocation ring buffer matching engine ensures extreme performance with minimal RAM usage (~4.6 MB) and 0% idle CPU.
- **Rich Text & Image Snippets**: Paste formatted text (`HTML Format`, `RTF`) or screenshots/images directly into snippet replacements with Paste-and-Lock (`.xblob` container storage).
- **Floating Snippet Search Palette**: Press the .XPANDER hotkey with no trigger typed to open a floating, searchable palette to select and inject snippets without typing triggers. Image snippets show thumbnails with a hover preview.
- **In-Settings Filter**: Live search and filter large snippet collections directly within the Expandings settings tab.
- **Dynamic Snippet Tokens**: Embed live, context-aware placeholders (dates, times, clipboard contents) in your snippets.
- **Case & Space Changer**: Global shortcut (`Ctrl + CapsLock`) to transform selected text (uppercase, lowercase, camelCase, Windows filename sanitization, etc.).
- **File Dialog Navigation (Quick Switch)**: Automatically synchronizes standard Windows Open/Save file dialogs to the active File Explorer window.
- **Configurable Storage & Encryption**: Save your configuration locally or in a cloud-synced folder (OneDrive, Dropbox, Google Drive) with conflict-free multi-PC synchronization (per-machine replica merge) and optional authenticated AES-256-GCM encryption at rest, integrated with Windows Credential Manager and one-time recovery key support.
- **3 Built-In Themes**: Switch between the default `aiVOLUTION` brand theme, classic `Dark`, and `Light` modes.
- **Privacy-Focused**: 100% offline, zero telemetry, secure memory buffer zeroization, zero logging in release builds, and encryption at rest.

## License

dotXPANDER is proprietary software licensed under the [End-User License Agreement](EULA.txt) by aiVOLUTION ApS. All rights reserved.

Third-party open-source components and their respective licenses are documented in [THIRDPARTY.txt](THIRDPARTY.txt).

## Support & Resources

- **Official Product Website**: [https://www.dotxpander.com](https://www.dotxpander.com)
- **Support & Feedback Portal**: [https://www.dotxpander.com/support/](https://www.dotxpander.com/support/)
- **Bug Reports & Feature Requests**: If you encounter an issue or have a feature request, please open a ticket in the [Issues tab](https://github.com/ThMoJe/dotXPANDER-Releases/issues) of this repository.
