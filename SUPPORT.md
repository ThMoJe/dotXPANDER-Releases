# Getting Support for dotXPANDER

Welcome to the dotXPANDER support guide. Whether you need help troubleshooting an issue, reporting unexpected behavior, or exploring licensing options, we have several channels available.

---

## Support Channels at a Glance

| Channel | Best For | Expected Response Time |
| :--- | :--- | :--- |
| **[GitHub Issues](https://github.com/ThMoJe/dotXPANDER-Releases/issues)** *(Recommended)* | Bug reports, feature requests, keyboard hook conflicts, technical diagnostics | **Fastest** (Tracked directly by the development team) |
| **[Official Support Portal](https://www.aivolution.dk/xpander-support)** | Users without a GitHub account, pre-sales inquiries, general feedback | Typically within a few business days |
| **Email Support** (`support@aivolution.dk`) | Commercial licensing, private inquiries, or security reports | Typically within 2–3 business days |

> [!TIP]
> **Have a GitHub account?**  
> We strongly recommend opening a ticket on GitHub. As noted on our official support page:  
> *"Har du en GitHub konto går det hele hurtigere og nemmere hvis du opretter din sag her."*  
> (Having a GitHub account makes issue resolution faster, easier, and fully trackable.)

---

## 1. GitHub Issues (Fastest & Recommended)

Our GitHub repository uses structured issue forms to ensure all necessary system information is collected up front:

- 🪲 **[Report a Bug](https://github.com/ThMoJe/dotXPANDER-Releases/issues/new?template=bug_report.yml)**  
  Use this template if dotXPANDER behaves unexpectedly, fails to expand a snippet, or encounters an application error.

- 💡 **[Request a Feature](https://github.com/ThMoJe/dotXPANDER-Releases/issues/new?template=feature_request.yml)**  
  Suggest new snippet capabilities, dynamic tokens, formatting options, or UX enhancements.

- 🛠️ **[3rd Level Support / Technical Case](https://github.com/ThMoJe/dotXPANDER-Releases/issues/new?template=support_case.yml)**  
  For advanced system-level issues, such as low-level keyboard hook collisions (`WH_KEYBOARD_LL`), antivirus false positives, or User Account Control (UAC) elevation boundary concerns.

---

## 2. Official Web Portal & In-App Link

The in-app **"🪲 Report a Bug"** button in dotXPANDER links directly to our official support portal:
👉 **[https://www.aivolution.dk/xpander-support](https://www.aivolution.dk/xpander-support)**

If you do not have a GitHub account, you can submit inquiries directly through the website form. Inquiries are reviewed by the XPANDER team in the order received, typically within a few business days.

---

## 3. Quick Self-Help & Common Questions

Before opening a support ticket, checking these common Windows configuration points often resolves the issue immediately:

### A. dotXPANDER Does Not Expand in an Administrator / Elevated Window
- **Cause**: Windows User Account Control (UAC) prevents standard-user processes from injecting simulated keystrokes into elevated (Administrator) windows (e.g. elevated PowerShell or Task Manager).
- **Solution**: If you frequently type into elevated applications, start dotXPANDER as Administrator ("Run as administrator"), or run both applications under the same privilege level.

### B. Conflicts with Other Hotkey or Macro Software
- **Cause**: dotXPANDER uses a standard low-level Windows keyboard hook (`WH_KEYBOARD_LL`). When multiple tools (such as Microsoft PowerToys Keyboard Manager, AutoHotkey, or gaming macro software) intercept keystrokes simultaneously, hook chaining delays or suppression can occur.
- **Solution**: Test by temporarily disabling or exiting competing hotkey utilities to isolate the conflict.

### C. Where Are My Settings and Logs?
- **Installed Mode**:
  - Configuration: `%APPDATA%\aiVOLUTION\dotXPANDER\config.toml`
  - Runtime Log: `%APPDATA%\aiVOLUTION\dotXPANDER\debug.log`
- **Portable Mode**:
  - Configuration and logs are stored in the same folder as `dotXPANDER.exe`.

### D. Restoring an Encrypted Configuration
- If you enabled AES-256-GCM encryption on your configuration file and move to a new machine or reset your Windows user profile, you can restore your snippets using the **One-Time Recovery Key** generated when encryption was first activated.

---

## 4. Reporting Security Vulnerabilities

We take security and user privacy seriously. dotXPANDER operates 100% offline with zero telemetry.

If you believe you have discovered a security vulnerability or sensitive defect:
- **Do not disclose it publicly in a GitHub issue.**
- Email details directly to `support@aivolution.dk` with the subject line: `[Security] dotXPANDER Vulnerability Report`.
- We will acknowledge receipt within 48 hours and work with you on a coordinated fix.

---

## 5. Company & Publisher Information

dotXPANDER is developed and published by:

**aiVOLUTION ApS**  
Haraldsgade 14  
7400 Herning  
Denmark  

- **CVR / VAT ID**: DK 46652649  
- **Phone**: +45 20 64 63 93  
- **Product Website**: [https://www.aivolution.dk/xpander](https://www.aivolution.dk/xpander)  
- **Support Portal**: [https://www.aivolution.dk/xpander-support](https://www.aivolution.dk/xpander-support)  
- **Email**: `support@aivolution.dk`
