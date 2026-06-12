<p align="center">
  <img src="https://img.shields.io/badge/game-Climber%20Animals%20Together-blue?style=for-the-badge" alt="Game">
  <img src="https://img.shields.io/badge/melonloader-v0.7.2-green?style=for-the-badge" alt="MelonLoader">
  <img src="https://img.shields.io/badge/version-2026.03.30-orange?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/license-MIT-lightgrey?style=for-the-badge" alt="License">
</p>

<h1 align="center">🐾 AnimalTransferMod</h1>
<p align="center"><strong>Climber Animals Together 玩家传送 & 位置回溯 MOD</strong></p>

<p align="center">
  <a href="#-功能特性">功能特性</a> ·
  <a href="#-快速开始">快速开始</a> ·
  <a href="#-使用方法">使用方法</a> ·
  <a href="#-回档系统">回档系统</a> ·
  <a href="#-已知问题">已知问题</a> ·
  <a href="#-路线图">路线图</a>
</p>

---

## 📖 简介

**AnimalTransferMod** 是一款为《Climber Animals Together》开发的 MelonLoader MOD，提供玩家间传送、自定义坐标传送以及**位置存档/回档**功能。

核心亮点是实现了**稳定可用的位置回溯系统**——你可以随时保存当前位置，试错后一键回档，**不影响成就获得**。

---

## ✨ 功能特性

| 功能 | 说明 |
|------|------|
| 📍 **实时坐标显示** | 显示房间内所有在线玩家的实时坐标 |
| 🚀 **传送到目标** | 一键将自己传送到目标玩家身边 |
| 🔄 **目标传送到我** | 将目标玩家拉到自己身边 |
| 🎯 **自定义坐标传送** | 输入 X/Y/Z 坐标精确传送 |
| 💾 **位置存档/回档** | `Ctrl+S` 存档，`Ctrl+Z` 回档，无限试错 |

---

## 🚀 快速开始

### 前置条件

- [MelonLoader](https://github.com/LavaGang/MelonLoader) v0.7.2+
- [Climber Animals Together](https://store.steampowered.com/) (Steam)

### 1. 安装 MelonLoader

下载 [MelonLoader.Installer.exe](https://github.com/LavaGang/MelonLoader/releases/download/v0.7.2/MelonLoader.Installer.exe)，右键以管理员身份运行：

```
1. 点击 SELECT → 选择游戏启动文件（Climber Animals Together.exe）
2. 点击 INSTALL
3. 安装器会自动下载依赖并生成 Mods / Plugins / UserData 文件夹
```

### 2. 安装本 MOD

```bash
# 将 AnimalTransferMod.dll 放入 Mods 文件夹
D:\stream\steamapps\common\Climber Animals Together\Mods\
│
├── AnimalTransferMod.dll          # ← 本 MOD
└── AnimalTransferMod_Save.txt     # ← 坐标存档文件（自动生成）
```

### 3. 启动游戏

启动游戏后 MOD 自动加载，按下 **F4** 即可打开传送菜单。

---

## 🎮 使用方法

### 传送菜单

```
F4  →  打开/关闭传送 GUI
```

### 传送功能

1. **查看坐标** — 菜单中会实时显示房间内所有玩家坐标
2. **传送到目标** — 选择目标玩家，点击传送到TA身边
3. **拉人到身边** — 选择目标玩家，将TA传送到你身边
4. **自定义坐标** — 手动输入 X/Y/Z，精确传送到任意位置

---

## 💾 回档系统

> ⭐ **这是本 MOD 最核心的功能**：稳定可用的位置回溯，无限试错，不影响成就获得。

### 存档 (Save)

```
Ctrl + S
```

将当前角色位置坐标保存到 `AnimalTransferMod_Save.txt`。

### 回档 (Load/Restore)

```
Ctrl + Z
```

读取上次保存的坐标，将角色传送回存档位置。

### 典型使用场景

```
你要挑战一个高难度跳跃
    ↓
Ctrl+S  存档当前位置
    ↓
去尝试（摔死了也没关系）
    ↓
Ctrl+Z  回到存档位置
    ↓
重新挑战，直到成功 ✨
```

### ⚠️ 注意事项

| 场景 | 处理方式 |
|------|---------|
| 回档后角色卡住 | 按空格跳一下即可恢复 |
| 传送后立即闪回 | 网络延迟导致，多试几次 |
| GUI 窗口开着卡顿 | 关闭 GUI（F4），因为坐标读写会占用帧数 |

---

## 🐛 已知问题

| 问题 | 状态 | 解决方案 |
|------|------|---------|
| 传送后网络波动导致闪回 | 🟡 观察中 | 多次尝试传送 |
| 回档时角色偶尔卡在地形中 | 🟡 观察中 | 跳一下解决 |
| 长时间开 GUI 导致轻微掉帧 | 🟡 持续优化 | 用完即关 |
| 回档只恢复位置不恢复时间 | 🔵 设计如此 | 后续考虑增加时间回溯 |

---

## 🗺 路线图

- [ ] 回档时同步恢复游戏内计时
- [ ] 队友坐标支持点击一键跳转
- [ ] 联机功能的深度适配与优化
- [ ] GUI 性能优化，减少帧率影响
- [ ] 多存档槽位支持

---

## 🔧 故障排除

### MOD 不加载？

```
1. 确认 MelonLoader 安装正确（启动游戏应出现 MelonLoader 启动画面）
2. 确认 AnimalTransferMod.dll 在 Mods 文件夹中
3. 尝试删除 MelonLoader 生成的所有文件，重新安装最新版
4. 重新启动游戏
```

### 首次安装后报错？

删除 MelonLoader 生成的所有文件（保留游戏原始文件），重新运行 `MelonLoader.Installer.exe` 安装即可。

---

## 📁 项目结构

```
Climber Animals Together\
├── Climber Animals Together.exe
├── Mods\                           # MOD 目录
│   ├── AnimalTransferMod.dll       # 传送 MOD 主体
│   └── AnimalTransferMod_Save.txt  # 坐标存档
├── Plugins\                        # MelonLoader 插件
├── UserData\                       # 用户数据
└── release\                        # 备份（可选）
    └── AnimalTransferMod.dll
```

---

## 🤝 贡献

欢迎提 Issue 和 PR！

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/crosakabc">crosakabc</a>
</p>
