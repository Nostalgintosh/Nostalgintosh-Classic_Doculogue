# Nostalgintosh-Classic_Doculogue
This is for my small computer I created in a Macintosh Classic II case and I use Manjaro KDE Plasma operating system

# 🍏 Project Nostalgintosh
**A Cyber-Archeology Build: 1991 Chassis, 2026 Soul.**

![Status](https://img.shields.io/badge/Status-Operational-success)
![OS](https://img.shields.io/badge/OS-Fedora%20Kinoite-blue)
![Theme](https://img.shields.io/badge/Aesthetic-System%207%20Platinum-grey)

## 📖 About The Project
**Nostalgintosh** is a "Restomod" computer project that fits modern, immutable Linux architecture inside a vintage **Macintosh Classic II** chassis. 

Unlike typical Raspberry Pi emulators, this project runs a full-desktop **Atomic Linux** OS (Fedora Kinoite), customized to replicate the **System 7** environment of the early 90s while maintaining modern web browsing and development capabilities.

---

## 🛠️ Hardware Specifications
| Component | Details |
| :--- | :--- |
| **Chassis** | Original Macintosh Classic II (circa 1991) |
| **Display** | Retro-fitted 9" LCD Panel (Custom Mount) |
| **Compute** | x86_64 Architecture (Modern Laptop Mainboard/Mini PC) |
| **Input** | USB Keyboard/Mouse (ADB Converters planned) |

---

## 💾 The Software Stack: "Atomic Nostalgia"
Instead of a standard Linux distro that can break with updates, this build uses **Fedora Kinoite**. This ensures the "Console-like" reliability of the original Macintosh.

* **Base OS:** Fedora Kinoite (Immutable KDE Plasma).
* **Package Management:** `rpm-ostree` (Base) & `Flatpak` (Apps).
* **Browser:** Brave (Sandboxed via Flatpak).
* **Terminal:** Konsole (Themed as "SimpleText").

---

## 🎨 Aesthetic Configuration (The "System 7" Recipe)
Achieving the 1991 "Platinum" look on a 2026 operating system requires specific manual overrides.

### 1. The "Platinum" Window Manager
We replaced the modern rounded "Big Sur" style with hard-edged, pixel-perfect borders.
* **Theme:** `KDE Story` / `Platinum` (Window Decorations).
* **Controls:** Removed Maximize/Minimize buttons (Close & Collapse only).
* **Colors:** High-contrast White/Black/Grey.

### 2. Typography: The Return of Chicago
The interface uses a modern TrueType recreation of Susan Kare's original **Chicago** font.
* **Font File:** `ChicagoFLF.ttf`
* **Installation Path:** `~/.local/share/fonts/`
* **Rendering:** Anti-aliasing **Enabled**, Sub-pixel rendering **OFF**, Hinting **FULL**. (This forces the "crisp" pixelated look).

### 3. Desktop Environment
* **Wallpaper:** Solid Grey (`#808080`) to mimic the original 1-bit dither pattern.
* **Top Bar:** 24px height, Apple Logo Menu (Left), Clock (Right), Empty Center.
* **Dock:** "NeXTSTEP" style floating dock for modern utility (Brave, Terminal, Dolphin).

---

## 🚀 Installation & Reproduction
If you are building your own Nostalgintosh, here are the core setup commands used in this build.

### Enable Flatpak & Install Brave
```bash
# Add Flathub Repository
flatpak remote-add --if-not-exists flathub [https://dl.flathub.org/repo/flathub.flatpakrepo](https://dl.flathub.org/repo/flathub.flatpakrepo)

# Install Brave Browser
flatpak install flathub com.brave.Browser
