# Charon Save Manager

The official standalone save manager for *No Man's Sky*, built by the Charon team.

Edit **bases**, **corvettes**, **ships**, **inventories**, **companions** and **wonders** in your save. Teleport anywhere with the **glyph teleporter**. Every save is backed up automatically before it's written, so you can roll back if anything feels wrong.

Written in Rust + egui. Runs on Windows, Linux and macOS (Apple Silicon).

---

## Status: Public Beta (0.8.0)

This is the first public release. Expect rough edges — please report what you find in [Issues](https://github.com/xX-Charon-Xx/charon-save-manager-release/issues).

Automatic slot backups are on by default. If an edit does something you didn't expect, your previous save slot is intact.

---

## Download

Grab the latest build for your platform from the [Releases page](https://github.com/xX-Charon-Xx/charon-save-manager-release/releases/latest).

| Platform | File |
|----------|------|
| **Windows** | `CharonSaveManager-X.Y.Z-beta-windows.exe` |
| **Linux** | `CharonSaveManager-X.Y.Z-beta-linux` |
| **macOS (Apple Silicon)** | `CharonSaveManager-X.Y.Z-beta-macos-arm.zip` |

---

## Running it

### Windows
Double-click the `.exe`. Windows SmartScreen may warn you the first time — click **More info** → **Run anyway** (the binary is not code-signed yet; the warning goes away once SmartScreen sees enough people run it).

### Linux
```bash
chmod +x CharonSaveManager-*-beta-linux
./CharonSaveManager-*-beta-linux
```
Most distros Just Work. If the window doesn't open, check that your system has a recent Vulkan/OpenGL stack — egui is GPU-accelerated.

### macOS (Apple Silicon)
```bash
unzip CharonSaveManager-*-beta-macos-arm.zip
xattr -cr CharonSaveManager.app
open CharonSaveManager.app
```
The `xattr -cr` step clears Gatekeeper's download quarantine so the unsigned app will launch. Signed builds are coming — this is a beta thing.

Intel Macs: not yet. If there's enough demand we'll cut an `x86_64` build; open an issue to say you want one.

---

## Backups

Charon Save Manager writes a backup of your current save slot **before every save operation**. Backups live next to your save file with a timestamp suffix. If something goes sideways, delete the modified slot and rename the most recent backup back to the original name — NMS will load it normally on next launch.

---

## Reporting issues

Please include:
- OS + version (Windows 11 24H2, macOS 15.1, Fedora 41, etc.)
- Charon Save Manager version (shown in the About dialog)
- What you were doing when it broke
- The save slot involved (so we can ask you to send it if we need to, privately)

File it at [Issues](https://github.com/xX-Charon-Xx/charon-save-manager-release/issues).

---

## About Charon

Charon Save Manager is one of several tools from the Charon team. The core service — automated in-game corvette delivery — lives at [charon.gg](https://charon.gg). The save manager is a standalone companion tool that doesn't require a Charon account to use; it's offered to the whole NMS community.

---

*Charon Save Manager is a fan-made tool and is not affiliated with Hello Games or endorsed by them. "No Man's Sky" is a trademark of Hello Games.*
