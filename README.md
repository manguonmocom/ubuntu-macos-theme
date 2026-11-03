# Ubuntu macOS Theme — Make Ubuntu look like macOS

**MacTahoe Setup** turns Ubuntu GNOME into a **macOS-style desktop**: MacTahoe theme, Mac Dock, desktop Widgets, optional Vietnamese input (**Ngó Sen** / **Bamboo**), and optional **[Ubu Office](https://github.com/manguonmocom/ubuntu-office)** (World · Excel · Slide · Pdf).

**Supported:** **Ubuntu 20.04 → 26.04 LTS** (and current interim). Full Dock/Widgets on **24.04 → 26.04**.

## Gallery (Ubuntu 24.04 / 26.04-class)

<p align="center">
  <img src="images/01-desktop-after.jpg" alt="Ubuntu with MacTahoe desktop — Dock, Widgets, wallpaper" width="900" />
</p>

| Control app | Setup Wizard |
|-------------|--------------|
| <img src="images/02-control.jpg" alt="MacTahoe Control" width="420" /> | <img src="images/03-setup-welcome.png" alt="Setup Wizard welcome" width="420" /> |

<p align="center">
  <img src="images/01b-desktop-live.jpg" alt="Live MacTahoe desktop session" width="900" />
</p>

### Ubu Office (optional in Setup)

<p align="center">
  <img src="images/05-ubu-office-gallery.jpg" alt="Ubu Office — World, Excel, Slide, Pdf" width="720" />
</p>

| World | Excel |
|-------|-------|
| <img src="images/05a-ubu-world.jpg" alt="Ubu World" width="420" /> | <img src="images/05b-ubu-excel.jpg" alt="Ubu Excel" width="420" /> |

| Slide | Pdf |
|-------|-----|
| <img src="images/05c-ubu-slide.jpg" alt="Ubu Slide" width="420" /> | <img src="images/05d-ubu-pdf.jpg" alt="Ubu Pdf" width="420" /> |

Setup ticks **Ubu Office** by default and opens the latest **[Ubu Office Setup AppImage](https://github.com/manguonmocom/ubuntu-office/releases/latest)** in a separate window.

| Download / docs | |
|-----------------|--|
| **[AppImage Setup](https://github.com/manguonmocom/ubuntu-macos-theme/releases/latest/download/Ubuntu-macOS-Theme-Setup-x86_64.AppImage)** | Double-click GUI installer |
| **[GUIDE.md](./GUIDE.md)** | English guide |
| **[HUONG-DAN.md](./HUONG-DAN.md)** | Hướng dẫn tiếng Việt |

**Keywords:** Ubuntu macOS theme · make Ubuntu look like Mac · MacTahoe · GNOME Dock · Ubuntu 20.04 22.04 24.04 26.04 theme · macOS desktop Linux

## Support matrix

| Ubuntu | What you get |
|--------|----------------|
| **26.04 LTS** | Full: theme, icons, Dock, Widgets; IME Ngó Sen hoặc Bamboo; optional GDM |
| **24.04 LTS / 25.x** | Full: theme, icons, Dock, Widgets; IME Ngó Sen hoặc Bamboo; optional GDM |
| **22.04 LTS** | Theme + icons; IME Ngó Sen hoặc Bamboo (no Dock/Widgets — needs GNOME ≥45) |
| **20.04 LTS** | Theme + icons + Bamboo (PPA); CLI Setup if no GTK4/Adw |

## Install

1. Download **`Ubuntu-macOS-Theme-Setup-x86_64.AppImage`** from [Releases](https://github.com/manguonmocom/ubuntu-macos-theme/releases/latest).
2. Mark executable (Properties → *Executable as program* / Allow Launching).
3. **Double-click** — Setup Wizard opens (no terminal required on 22.04+ with GTK4).
4. Keep **MacTahoe** and **Ubu Office** checked (Office is on by default). Pick IME if you want. Enter your password when asked.
5. If Ubu Office is checked, Setup downloads and opens the **Ubu Office Setup** AppImage (separate window) so you can pick language + apps there.

```bash
chmod +x Ubuntu-macOS-Theme-Setup-x86_64.AppImage
./Ubuntu-macOS-Theme-Setup-x86_64.AppImage
```

Then open **MacTahoe Control** → **Preset Mac-like** (optional) for Dock left, traffic-light buttons, wallpaper, and panel clock in one click.

## Highlights after Setup

- **Wallpaper** Day/Night — Control → Apply wallpaper
- **Preset Mac-like** — Dock left · buttons left · panel · theme
- **Ubu Office** — opens [Ubu Office Setup](https://github.com/manguonmocom/ubuntu-office/releases/latest) AppImage (language + World/Excel/Slide/Pdf)
- **Fonts** — optional SF Pro / Inter pack from Control
- **Search** — use Ubuntu Activities / Super (no extra launcher)

## Requirements

- Ubuntu **20.04 → 26.04** (GNOME session; best on 24.04–26.04)
- Prefer **Ubuntu on Xorg** when available
- Normal user with `sudo` — **do not** run the AppImage with `sudo`
- After first install on Wayland: **log out and back in** once so Dock/Widgets load

## Guides

- English: [GUIDE.md](./GUIDE.md)
- Tiếng Việt: [HUONG-DAN.md](./HUONG-DAN.md)
