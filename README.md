# PPTShowAssistant

**Keeps PowerPoint show PCs running – reliably, unattended, and simple enough for anyone on the crew.**

PPTShowAssistant turns a Windows PC into a dependable PowerPoint player for conferences, live events and professional show environments. It sits in the system tray, watches PowerPoint, prepares Windows for show use and shows every problem before the audience sees it – including on headless PCs without a monitor or keyboard.

🌐 [pptshowassistant.com](https://pptshowassistant.com)

> **Status: early development.** All current versions are *dev* pre-releases (0.1.x). Test them on your own PCs before using them in a show. The first stable version will be **1.0.0**.

---

## Download

**[⬇ Download the latest PPTShowAssistant.exe](https://github.com/konftools/PPTShowAssistant-releases/releases)**

One single file: no installer package and no runtime to install first.

**Requirements**
- Windows 10 or Windows 11 (64-bit)
- Microsoft PowerPoint 2016 or newer, ideally Microsoft 365 Apps. PPTShowAssistant can help you install it.

> Windows SmartScreen may warn about the downloaded file because it is not code-signed yet. Choose *More info → Run anyway*.

---

## Installation

1. Start `PPTShowAssistant.exe` from anywhere, for example your Downloads folder.
2. The **setup assistant** guides you through a few short steps:
   - **Install and autostart.** The program copies itself to `C:\PPTShowAssistant` and starts automatically with Windows.
   - **Automatic sign-in.** Windows signs in by itself, so the PC is ready after power-on without a keyboard.
   - **Windows preparation.** These are the *Showsafe Tweaks*: show-friendly settings, each one optional.
   - **Name and role of this PC.** For example `ppt1` as *PowerPoint player* or `operator-pc1` as *Operator PC*.
   - **PowerPoint watchdog** and the other modules.
3. Windows asks once for administrator rights. That is the only time.

After that, the PC runs on its own. The coloured logo in the tray shows the overall state at a glance:
- **Green:** all OK
- **Orange:** warning
- **Red:** error

---

## What it does

### PowerPoint watchdog
- Keeps PowerPoint open at all times. After a crash, a hang or an accidental close, it restarts PowerPoint and reopens the presentation at the same slide.
- Handles blocking PowerPoint dialogs that would otherwise stop a show unattended. This works in every PowerPoint and Windows language.
- Checks the PowerPoint version, the licence and the activation, and warns early. A missing licence is shown as an error.
- **Install PowerPoint…** offers the right Microsoft download for your situation: winget, Microsoft account, work account or product key. It also detects remains of old Office versions.
- **PowerPoint Add-Ins…** lists useful add-ins for show use, with links to free downloads and the Microsoft Store.
- Screen settings for the presenter view.

### Windows Showsafe Tweaks
These are show-friendly Windows settings. Each one can be switched on or off, and everything can be undone:
- Automatic sign-in
- High performance: no standby or hibernation, and the display never turns off
- No screen saver and no lock screen
- Silenced Windows notifications
- No Windows sounds
- No Windows tips, ads or "finish setting up" screens after updates
- Windows and Office updates: downloaded at any time, installed only at 2:00 at night
- Wake on LAN prepared
- Firewall rules for the network features

A file in the program folder undoes the whole Windows preparation and restores the previous settings.

### Network view
- Shows every PPTShowAssistant on the network: name, IP address, version, state, and the status of each module. Problems on any PC are visible from every PC.
- Also lists other show devices found via mDNS / Bonjour: Bitfocus Companion, Companion Satellite, NDI sources, Dante devices, QLab, OSC and Blackmagic devices. Companion and Satellite get a direct **Open** button to their web interface.
- Every PC gets a unique, readable name. Duplicate names are detected.

### OSCPoint
- Installs and updates [OSCPoint](https://oscpoint.com) by Nick Roberts with one click, even offline. OSCPoint is the PowerPoint add-in for remote control via OSC, for example from Bitfocus Companion.
- Edits OSCPoint's settings from the settings window, and finds Companion instances on the network for you.
- If OSCPoint is useful to you, please consider [supporting its author](https://oscpoint.com).

### Coming later
- Pre-show check of presentations and media: fonts, links, formats, videos
- Local file synchronisation between the show PCs of a room
- Remote control and status via OSC / Bitfocus Companion
- Watchdog for other show programs

---

## Updates

PPTShowAssistant updates itself in the background. PowerPoint keeps running during an update, and no update is installed while one of its windows is open.

Every update is checked before it is installed: the manifest must carry a valid signature and the file hash must match.

**Version numbers**

| Version | Meaning |
|---|---|
| `x.0.0` | Major version |
| `x.y.0` | Stable version for shows |
| `x.y.z` | Dev version (only with the *dev* update channel) |

You choose the update channel in *Settings → Automatic updates*.

---

## Uninstall

Open the tray menu and choose **Uninstall PPTShowAssistant…**. You can also choose to undo the Windows preparation and restore the previous settings.

PPTShowAssistant only ever touches its own files and the settings it changed itself.

---

## Licence and open source

PPTShowAssistant is © 2026 Robert Skiba, [konferenzregie.de](https://konferenzregie.de).

It uses open-source components and bundles OSCPoint (© Nick Roberts). All components, copyrights and licence texts are listed in the program under **Open source and licences…** at the top of the tray menu.

Microsoft, PowerPoint, Windows and Microsoft 365 are trademarks of Microsoft Corporation. Bitfocus Companion is a product of Bitfocus AS. PPTShowAssistant is an independent tool and is not affiliated with Microsoft or Bitfocus.
