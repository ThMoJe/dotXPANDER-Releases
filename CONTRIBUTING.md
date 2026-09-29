# Contributing to dotXPANDER

Thank you for your interest in improving dotXPANDER!

dotXPANDER is a high-performance Windows text expander and productivity utility developed by [aiVOLUTION ApS](https://www.aivolution.dk/xpander). It is distributed as proprietary software under the [End-User License Agreement (EULA)](EULA.txt).

While the underlying engine source code is proprietary, the **dotXPANDER-Releases** repository is our official public hub for releases, issue tracking, and community feedback. Your bug reports, feature suggestions, and diagnostic findings directly influence the development roadmap.

---

## Ways to Contribute

- [Report a Bug](#reporting-bugs)
- [Suggest an Enhancement](#suggesting-enhancements)
- [Request 3rd-Level Technical Support](#3rd-level-technical-support)
- [Provide Documentation & Translation Feedback](#documentation--translations)

> [!NOTE]
> Because dotXPANDER's core engine is closed-source, this repository does not accept unsolicited pull requests containing application source code. If you wish to propose improvements to public documentation, installer scripts, or issue templates, pull requests are welcome.

---

## Reporting Bugs

Before creating a new bug report, please check the [existing Issues](https://github.com/ThMoJe/dotXPANDER-Releases/issues) to ensure the problem has not already been reported or resolved in a recent release.

### How to Submit
To report a bug, open a ticket using our structured form:
👉 **[New Bug Report](https://github.com/ThMoJe/dotXPANDER-Releases/issues/new?template=bug_report.yml)**

Please provide as much relevant detail as possible:
1. **dotXPANDER Version**: e.g., `v0.2.0` (visible in Settings or file properties).
2. **Installation Mode**:
   - Installed (via Setup executable)
   - Portable (`.zip` / standalone executable)
   - Windows Package Manager (`winget install aiVOLUTION.dotXPANDER`)
   - Microsoft Store
3. **Windows Environment**:
   - Windows version and build number (e.g., Windows 11 23H2 Build 22631)
   - Architecture: `x64` (Intel/AMD) or `ARM64` (Snapdragon / Copilot+ PC)
4. **Target Application(s)**: Which application(s) were active when the issue occurred (e.g., VS Code, Chrome, Word, PowerShell, Windows Terminal).
5. **Reproduction Steps**: Step-by-step instructions to reproduce the issue reliably.
6. **Expected vs. Actual Behavior**: What you expected to happen versus what actually occurred.

### Runtime Logs & Diagnostics
Standard release builds automatically write diagnostic events to a local log file:
- **Default path**: `%APPDATA%\aiVOLUTION\dotXPANDER\debug.log`
- **Portable mode**: Located alongside `dotXPANDER.exe`

> [!IMPORTANT]
> dotXPANDER is **100% offline with zero telemetry**. We never collect your keystrokes or snippet contents. When attaching log snippets or configuration excerpts to public issues, please **redact any sensitive information or private triggers** before submitting.

---

## Suggesting Enhancements

We welcome ideas that make dotXPANDER faster, more capable, and more ergonomic.

### Our Design Philosophy
- **Ultra-Low Latency**: Keystroke processing and snippet matching must remain imperceptibly fast.
- **Minimal Footprint**: 0% idle CPU and minimal RAM usage. Zero background runtimes or speculative bloat.
- **Privacy & Security**: All data remains local and offline, with optional AES-256-GCM encryption at rest.

### How to Submit
To propose a feature or improvement, use our structured form:
👉 **[New Feature Request](https://github.com/ThMoJe/dotXPANDER-Releases/issues/new?template=feature_request.yml)**

Please explain:
- The problem or workflow limitation you are trying to solve.
- How you envision the solution working.
- Any alternatives or workarounds you currently use.

---

## 3rd-Level Technical Support

For deep-dive technical issues — such as low-level keyboard hook (`WH_KEYBOARD_LL`) collisions with third-party software, antivirus false positives, or User Account Control (UAC) elevation boundaries — please open a technical case:
👉 **[3rd Level Support / Technical Case](https://github.com/ThMoJe/dotXPANDER-Releases/issues/new?template=support_case.yml)**

Before submitting, check whether:
- Other keyboard or macro utilities are active (e.g., Microsoft PowerToys Keyboard Manager, AutoHotkey, Razer Synapse).
- The target application is running elevated as Administrator while dotXPANDER is running as a standard non-elevated user (Windows UAC security boundaries prevent standard apps from sending input to elevated windows).
- Your security software is monitoring or blocking low-level input hooks.

---

## Documentation & Translations

dotXPANDER currently supports English and Danish. If you spot a typo, an awkward translation, or unclear documentation:
- Open a [Feature Request / Improvement](https://github.com/ThMoJe/dotXPANDER-Releases/issues/new?template=feature_request.yml) describing the correction.
- Or submit a pull request if the change applies to markdown files in this repository.

---

## Code of Conduct

We are committed to providing a friendly, constructive, and professional environment for everyone. Please be respectful, helpful, and courteous when discussing issues and feature proposals.
