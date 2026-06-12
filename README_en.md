# 🐾 AnimalTransferMod

<!-- MULTILANG_NAV_START -->
[🇨🇳 中文](./README.md) | **🇬🇧 English** | [🇯🇵 日本語](./README_ja.md)
<!-- MULTILANG_NAV_END -->

---

<p align="center">
  <img src="https://img.shields.io/badge/game-Climber%20Animals%20Together-blue?style=for-the-badge" alt="Game">
  <img src="https://img.shields.io/badge/melonloader-v0.7.2-green?style=for-the-badge" alt="MelonLoader">
  <img src="https://img.shields.io/badge/version-2026.03.30-orange?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/license-MIT-lightgrey?style=for-the-badge" alt="License">
</p>

<h1 align="center">🐾 AnimalTransferMod</h1>
<p align="center"><strong>Climber Animals Together — Player Teleport & Position Rollback MOD</strong></p>

<p align="center">
  <a href="#-features">Features</a> ·
  <a href="#-quick-start">Quick Start</a> ·
  <a href="#-usage">Usage</a> ·
  <a href="#-rollback-system">Rollback System</a> ·
  <a href="#-known-issues">Known Issues</a> ·
  <a href="#-roadmap">Roadmap</a>
</p>

---

## 📖 Introduction

**AnimalTransferMod** is a MelonLoader MOD for *Climber Animals Together* that provides player-to-player teleportation, custom coordinate teleportation, and a **position save/rollback** feature.

The core highlight is a **reliable position rollback system** — save your position anytime, experiment without fear, and roll back with a single keystroke, **without affecting achievement unlocks**.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 📍 **Real-time Coordinates** | Display real-time coordinates of all online players in the room |
| 🚀 **Teleport to Target** | One-click teleport yourself to a target player |
| 🔄 **Target Teleport to You** | Pull a target player to your location |
| 🎯 **Custom Coordinates** | Input custom X/Y/Z coordinates for precise teleportation |
| 💾 **Position Save/Rollback** | `Ctrl+S` to save, `Ctrl+Z` to roll back — unlimited retries |

---

## 🚀 Quick Start

### Prerequisites

- [MelonLoader](https://github.com/LavaGang/MelonLoader) v0.7.2+
- [Climber Animals Together](https://store.steampowered.com/) (Steam)

### 1. Install MelonLoader

Download [MelonLoader.Installer.exe](https://github.com/LavaGang/MelonLoader/releases/download/v0.7.2/MelonLoader.Installer.exe), right-click and run as administrator:

```
1. Click SELECT → choose the game executable (Climber Animals Together.exe)
2. Click INSTALL
3. The installer will automatically download dependencies and create Mods / Plugins / UserData folders
```

### 2. Install the MOD

```bash
# Place AnimalTransferMod.dll into the Mods folder
D:\steam\steamapps\common\Climber Animals Together\Mods\
│
├── AnimalTransferMod.pdb           # ← For debugging error stacks   
├── AnimalTransferMod.deps          # ← JSON dependency configuration file to mark MOD dependent libraries
├── AnimalTransferMod.dll          # ← This MOD
└── AnimalTransferMod_Save.txt     # ← Coordinate save file (auto-generated)
```

### 3. Launch the Game

The MOD loads automatically on game launch. Press **F4** to open the teleport menu.

---

## 🎮 Usage

### Teleport Menu

```
F4  →  Open / Close teleport GUI
```

### Teleport Functions

1. **View Coordinates** — The menu displays real-time coordinates of all players in the room
2. **Teleport to Target** — Select a target player, click to teleport to their side
3. **Pull Target to You** — Select a target player, pull them to your location
4. **Custom Coordinates** — Manually enter X/Y/Z for precise teleportation

---

## 💾 Rollback System

> ⭐ **This is the MOD's core feature**: a reliable position rollback with unlimited retries that does not affect achievements.

### Save

```
Ctrl + S
```

Saves your current character position coordinates to `AnimalTransferMod_Save.txt`.

### Load / Restore

```
Ctrl + Z
```

Reads the last saved coordinates and teleports your character back to the saved position.

### Typical Use Case

```
You're about to attempt a difficult jump
    ↓
Ctrl+S   Save your current position
    ↓
Go for it (doesn't matter if you fall)
    ↓
Ctrl+Z   Return to the saved position
    ↓
Retry until you succeed ✨
```

### ⚠️ Notes

| Scenario | Solution |
|----------|----------|
| Character stuck after rollback | Press jump to recover |
| Immediate flashback after teleport | Network latency — try again |
| GUI causes frame drops | Close the GUI (F4), coordinate polling uses frames |

---

## 🐛 Known Issues

| Issue | Status | Solution |
|-------|--------|----------|
| Flashback due to network fluctuation | 🟡 Monitoring | Retry teleport |
| Character occasionally stuck in terrain after rollback | 🟡 Monitoring | Jump to resolve |
| Slight frame drops with GUI open for long periods | 🟡 Optimizing | Close when not in use |
| Rollback restores position but not timer | 🔵 By design | Time rollback under consideration |

---

## 🗺 Roadmap

- [ ] Sync game timer on rollback
- [ ] Clickable teammate coordinates for one-click teleport
- [ ] Deep optimization for multiplayer functionality
- [ ] GUI performance optimization to reduce frame impact
- [ ] Multiple save slots

---

## 🔧 Troubleshooting

### MOD not loading?

```
1. Verify MelonLoader is installed correctly (you should see the MelonLoader splash on launch)
2. Verify AnimalTransferMod.dll is in the Mods folder
3. Try deleting all MelonLoader-generated files and reinstall the latest version
4. Restart the game
```

### Errors on first install?

Delete all MelonLoader-generated files (keep only the original game files), then re-run `MelonLoader.Installer.exe` to reinstall.

---

## 📁 Project Structure

```
Climber Animals Together\
├── Climber Animals Together.exe
├── Mods\                           # MOD directory
|   ├── AnimalTransferMod.pdb           # ← For debugging error stacks  
|   ├── AnimalTransferMod.deps          # ← JSON dependency configuration file for marking MOD dependency libraries
│   ├── AnimalTransferMod.dll       # Teleport MOD core
│   └── AnimalTransferMod_Save.txt  # Coordinate save file
├── Plugins\                        # MelonLoader plugins
├── UserData\                       # User data
└── release\                        # Optional backup
    └── AnimalTransferMod.dll
```

---

## 🤝 Contributing

Issues and PRs are welcome!

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/crosakabc">crosakabc😀</a>
</p>
