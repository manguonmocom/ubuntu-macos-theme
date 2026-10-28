# Ubuntu macOS Theme Guide (English)

How to install a **macOS-like theme on Ubuntu** (MacTahoe) and use **MacTahoe Control** every day.

Search-friendly topics: *Ubuntu macOS theme*, *make Ubuntu look like Mac*, *MacTahoe Ubuntu*, *GNOME Mac Dock*, *Ubuntu 24.04 theme*.

---

## Install

### What you need

- Ubuntu **24.04** (best). 22.04: theme / Ngó Sen; Dock + Widgets need GNOME ≥ 45. **20.04: not supported.**
- Login session: **Ubuntu on Xorg** when possible.
- Your normal user with `sudo` — never run the installer with `sudo`.
- **GDM (login screen) theme:** optional. Shell **46** (Ubuntu 24.04) uses the classic installer; Shell **48+** uses the newer path. Shell **42** (22.04) is experimental. Keep it **off** unless you accept login-screen risk.

### Steps (graphical app)

1. Download **`Ubuntu-macOS-Theme-Setup-x86_64.AppImage`** from the [latest Release](https://github.com/manguonmocom/ubuntu-macos-theme/releases/latest).
2. Make it executable: right-click → **Properties** → **Executable as program** (or “Allow Launching”).
3. **Double-click** the AppImage. The **Setup Wizard** window opens — you do not need a terminal.
4. In the Wizard:
   - Leave **MacTahoe** checked (theme + Dock + Widgets).
   - Optional: **Ngó Sen** for Vietnamese typing.
   - Leave **GDM theme** off unless you know you need it.
5. Enter your password when asked. When it finishes, open **MacTahoe Control** from the app menu or Desktop.

Optional (terminal):

```bash
chmod +x Ubuntu-macOS-Theme-Setup-x86_64.AppImage
./Ubuntu-macOS-Theme-Setup-x86_64.AppImage
```

### Quick check after install

- One Mac-style Dock (not two docks).
- MacTahoe look on windows / icons.
- Optional: type Vietnamese with Ngó Sen (`Ctrl+Space` switches keyboard).

If Dock or Widgets are missing once: log out and log back in.

---

## Use MacTahoe Control

Open **MacTahoe Control** from the menu, Desktop shortcut, or:

```bash
mactahoe-control
```

Status text appears at the **top and bottom** of the window after each action.

### Color Themes

Choose how the MacTahoe **accent color** and light/dark look are applied.

| Control | Meaning |
|---------|---------|
| **Accent color** | MacTahoe accent: Default (Tahoe), Blue, Purple, Pink, Red, Orange, Yellow, Green, Grey. |
| **Light / Dark** | GTK + Shell appearance mode. |
| **Apply** | Install the variant if needed, then switch theme, Shell, and icons together. |
| **Theme Select → Open** | Opens the GTK4 theme picker (`gnome-theme-switcher`) for advanced theme choice. |

Tip: after Apply, reopen Quick Settings. On X11 you can press `Alt+F2`, type `r`, Enter if the Shell theme did not refresh.

### Dock

Mac-style app Dock (UbuntuTahoeDock). Ubuntu’s default Dock is turned off so you only have one bar.

| Control | Meaning |
|---------|---------|
| **Show Dock** | Enable or disable the MacTahoe Dock extension. |
| **Dock position** | Left (default macOS-like), Bottom, Right, or Top. |
| **Autohide Dock** | Hide the Dock until the pointer reaches the screen edge. |

### Desktop Widgets

Desktop widgets from UbuntuTahoeWidgets.

| Control | Meaning |
|---------|---------|
| **Show Widgets** | Master switch for the whole widget extension. |
| **Large clock** | Big clock on the desktop. |
| **Weather** | Weather widget. |
| **System monitor** | CPU / memory style system stats. |
| **Lunar calendar** | Âm lịch (lunar) calendar widget. |
| **Break reminder** | Reminder to take a break. |
| **Open advanced Widgets settings** | Opens the extension preferences UI. |

### Window buttons

Where the close / minimize / maximize buttons sit on title bars.

| Control | Meaning |
|---------|---------|
| **Button side** | **Left — macOS style (● ● ●)** or **Right — Windows/GNOME**. |

### Ngó Sen (Vietnamese input)

Optional fcitx5 IME for typing Vietnamese. Use when you enabled Ngó Sen in Setup.

| Control | Meaning |
|---------|---------|
| **Enable Vietnamese (Ngó Sen)** | Switch to Ngó Sen and prefer it as the input method. Off = English (US) keyboard. |
| **Fix Ngó Sen** | Rewrite fcitx5 profile/config and restart the IME if typing fails or the language jumps back to English. |
| **Ngó Sen settings → Open** | Official Ngó Sen settings window. |
| **Fcitx5 config → Open** | Add/remove input methods and shortcuts. |
| **Set Ngó Sen as default** | Same repair path as Fix: clean profile + `DefaultIM=ngosen`. |

Tip: **Ctrl+Space** toggles English keyboard ↔ Ngó Sen. If focus changes reset to English, click **Fix** once.

### Tools

Maintenance shortcuts for the MacTahoe desktop.

| Control | Meaning |
|---------|---------|
| **Open Setup Wizard** | Run Setup again to update or reinstall components. |
| **Re-activate Dock & Widgets** | Reload Dock/Widgets if they disappeared (safe; no full logout required in most cases). |
| **Icon manager / Extension Manager** | Manage MacTahoe icons or GNOME extensions when installed. |
| **Re-apply GTK overrides** | Restore Setup GTK tweaks (e.g. Files path bar). |
| **Restore MacTahoe glass** | Restore glass-style Quick Settings / panel look. |
| **Reset to Ubuntu defaults** | Remove the Mac look, bring back Ubuntu Dock / Yaru. Setup shortcut is kept so you can install again. |
| **Uninstall MacTahoe** | Remove MacTahoe theme/extensions. Ngó Sen packages stay unless you remove them separately. Setup shortcut is restored. |

---

## Troubleshooting

| Problem | What to do |
|---------|------------|
| “Oh no!” screen | Do **not** Log Out if you need open apps. On X11: `Alt+F2` → `r`. |
| Two Docks | In Control, keep MacTahoe Dock on; Ubuntu Dock should stay off. |
| Dock / Widgets missing (clean PC) | On **Wayland** you must **log out and back in once** (see `MacTahoe-CAN-DANG-XUAT.txt` on Desktop). Then enable Dock/Widgets in Control. |
| Ngó Sen lock timeout / Fix stuck | Latest AppImage breaks stale locks + times out `fcitx5-remote`. Click **Fix once** and wait. |
| Missing fcitx5-ngosen / “needs curl” | Latest AppImage installs the `.deb` directly (no curl). Control → **Fix Ngó Sen** (needs sudo). |
| GDM “requires Shell 48” on 24.04 | Latest AppImage uses the **classic** GDM path on GNOME 46. Re-run Setup with GDM checked, then reboot. |
| Ngó Sen → English | Control → **Fix Ngó Sen**. |
| Log files | On the **Desktop**: `MacTahoe-Setup-log.txt`, `MacTahoe-Control-log.txt`, `MacTahoe-DEBUG-README.txt`. Control → Tools → Open log… |

**Activities / Overview:** press **Super** (Windows key). The Apple menu only shows a tip.

---

## Vietnamese guide

Xem bản tiếng Việt: [HUONG-DAN.md](./HUONG-DAN.md).
