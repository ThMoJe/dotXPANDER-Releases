# dotXPANDER

A lightweight, high-performance Windows text expander and productivity utility.
Native Rust and Slint UI for Windows 11 ARM64 and Windows 10/11 x86_64.

dotXPANDER is a native Windows productivity tool designed for speed, low resource usage, and seamless compatibility with modern Windows applications. It runs as a single, highly optimized native binary that requires no background runtime, uses minimal memory, and draws 0.0% CPU while idle.

## Installation

### Option A: Windows Package Manager (Winget) - Recommended

You can install dotXPANDER directly via Windows Package Manager:

```powershell
winget install aiVOLUTION.dotXPANDER
```

### Option B: Windows Installer

Download the latest setup executable (`dotXPANDER-x64-Setup.exe` or `dotXPANDER-arm64-Setup.exe`) from the [Releases](https://github.com/ThMoJe/dotXPANDER-Releases/releases) tab.

The setup wizard installs to your local user directory (no Administrator/UAC prompt required) and supports automated silent deployment.

### Option C: Portable ZIP

Download the portable zip archive from the [Releases](https://github.com/ThMoJe/dotXPANDER-Releases/releases) tab and extract it to a directory of your choice. When launched without installation, dotXPANDER runs in Portable Mode, storing its configuration alongside the executable.

## Features

- Snippet Expansion: Expands trigger strings instantly as you type or on demand using a configurable keyboard shortcut.
- Low Resource Footprint: Zero-allocation ring buffer matching engine ensures extreme performance with minimal RAM usage and 0% idle CPU.
- Dynamic Snippet Tokens: Embed live, context-aware placeholders (dates, times, clipboard contents) in your snippets.
- Case & Space Changer: Global shortcut to transform selected text (uppercase, lowercase, camelCase, Windows filename sanitization, etc.).
- File Dialog Navigation: Automatically synchronizes standard Windows Open/Save file dialogs to the active File Explorer window.
- Configurable Storage: Save your configuration locally or in a cloud-synced folder (OneDrive, Dropbox, Google Drive) to share snippets across devices.
- Privacy-Focused: 100% offline, zero telemetry, and secure memory buffer zeroization.

## License

dotXPANDER is proprietary software licensed under the [End-User License Agreement](EULA.txt) by aiVOLUTION ApS. All rights reserved.

Third-party open-source components and their respective licenses are documented in THIRDPARTY.txt.
