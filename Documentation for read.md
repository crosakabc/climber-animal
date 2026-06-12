# 说明文档 — Climber Animals Together MOD 安装与使用

> **适用游戏**: Climber Animals Together (AsianMode 版本)  
> **当前 MOD 版本**: 2026/3/30  
> **MelonLoader 版本**: v0.7.2

---

## 目录

- [1. 安装 MelonLoader](#1-安装-melonloader)
- [2. 关于 Mods 文件](#2-关于-mods-文件)
- [3. 实现的功能](#3-实现的功能)
- [4. 关于已知 Bug](#4-关于已知-bug)
- [5. 后续有待完善](#5-后续有待完善)

---

## 前置准备

将所有文件以及文件夹放到游戏根目录下：

```
D:\stream\steamapps\common\Climber Animals Together\
```

---

## 1. 安装 MelonLoader

> **注意**: 当前文件夹下已附带 MelonLoader，通常情况下无需重复安装。  
> 直接浏览本地文件地址，将 MelonLoader 程序文件夹放入游戏根目录即可。

### 兼容性说明

当前 Climber Animals Together - AsianMode 版本即使更新（当前最新：2026/3/30）后也可以使用当前 MOD 工具。

**当出现报错时的处理流程**：

1. 尝试配置 `.cs` 文件之后编译（**注意保存好原有的 release 文件**）
2. 重新启动游戏
3. 如果仍然不行，删除 MelonLoader 后重新安装最新版本
4. 重新启动游戏，一般可以解决问题

### 全新安装步骤

#### 1.1 下载 MelonLoader 官方安装器

- 下载地址：https://github.com/LavaGang/MelonLoader/releases/download/v0.7.2/MelonLoader.Installer.exe

#### 1.2 运行安装器

右键 `MelonLoader.Installer.exe` → **以管理员身份运行**

#### 1.3 选择游戏启动文件

点击 **Select**，选择游戏启动文件 — 会自动识别到 `Climber Animals Together`

#### 1.4 点击 Install

点击 **Install**，安装器会自动完成以下操作：

- 自动下载正确版本的 Cpp2IL（包含所有依赖 dll、完整 Plugins 文件夹）
- 自动生成 `Mods`、`Plugins`、`UserData` 等文件夹

### 重新安装注意事项

启动 Install 插件时会生成几个文件。后续 reinstall 时会报错，处理方式：

1. 将有报错找 AI 解决
2. 如果不行，将插件生成的所有文件全部删除
3. 重新点击 exe 程序安装，生成需要的依赖文件

#### 经典错误处理

> **关闭游戏以及插件后有以下报错 → 将插件生成的文件全部删除 → 重新点击 exe 程序安装**

- 看到 **两个标识** 说明有漏删，无法重新安装
- 看到 **一个标识** 则可以重新安装

**一般重新安装后再启动，MOD 都会正常识别。**

### 游戏原有文件参考

以下是游戏原有的文件（**不要删除这些**），其他的文件就是 MelonLoader 生成的，删除即可：

> 游戏安装目录下的原始文件保留，其余 MelonLoader 生成文件夹（Mods、Plugins、UserData 等）可删除后重新安装。

---

## 2. 关于 Mods 文件

### 2.1 文件放置

1. 确保 `AnimalTransferMod.dll` 放入游戏根目录下的 **Mods** 文件夹中
2. 在 Mods 文件夹中确保创建 `AnimalTransferMod_Save.txt` 文本文件，用于保存坐标数据（提供的文件夹中已包含此文件）

**示例路径**：

```
D:\stream\steamapps\common\Climber Animals Together\Mods\
```

### 2.2 其他 Mod 文件管理

- 其他 Mod 文件夹下的文件可以保留在 `Mods` 文件夹中
- 也可以和 `AnimalTransferMod.dll` 一起放到一个自行创建的 `release` 文件夹下作为备份

---

## 3. 实现的功能

### 传送 GUI 菜单

| 快捷键 | 功能 |
|--------|------|
| **F4** | 打开 / 关闭传送 GUI 菜单 |

### 功能列表

| 序号 | 功能 | 说明 |
|------|------|------|
| 1 | **显示房间内所有玩家实时坐标** | 实时查看所有在线玩家的位置 |
| 2 | **我传送到目标** | 将自己的角色传送到目标玩家位置 |
| 3 | **目标传送到我** | 将目标玩家传送到自己位置 |
| 4 | **自定义坐标精确传送** | 输入自定义 X/Y/Z 坐标进行精确传送 |
| 5 | **位置存档 / 回档** | `Ctrl+S` 存档 / `Ctrl+Z` 回档 |

### ⭐ 核心亮点：位置存档 / 回档

> 最终实现了**稳定可用的位置回溯功能**，理论上可以无限试错，并且**不会影响成就获得**。

- **存档**: 按下 `Ctrl+S`，将当前角色的位置坐标保存到 `AnimalTransferMod_Save.txt`
- **回档**: 按下 `Ctrl+Z`，读取上次保存的坐标并将角色传送回该位置

---

## 4. 关于已知 Bug

| 序号 | 问题描述 | 解决方案 |
|------|---------|----------|
| 1 | 受网络影响，传送后可能**立即闪回** | 请多次尝试传送功能 |
| 2 | 回档跳转时角色有时会**卡住** | 尝试跳一下就恢复正常 |
| 3 | 一直开着窗口会**卡顿** | 不要一直开着 GUI 窗口（因为读写坐标按帧数执行） |

---

## 5. 后续有待完善

- [ ] 回档到位置但秒数依然增加（目前只读写位置，不处理时间）
- [ ] 实时显示队友坐标，点击相关角色可直接跳转到队友位置
- [ ] 联机功能的完善与优化

---

## 附录：文件结构参考

```
D:\stream\steamapps\common\Climber Animals Together\
├── Climber Animals Together.exe      # 游戏主程序
├── [游戏原始文件...]                  # 不要删除
├── Mods\                             # MelonLoader 生成
│   ├── AnimalTransferMod.dll         # 传送 MOD
│   └── AnimalTransferMod_Save.txt    # 坐标存档文件
├── Plugins\                          # MelonLoader 生成
├── UserData\                         # MelonLoader 生成
└── release\                          # 可选：MOD 备份文件夹
    └── AnimalTransferMod.dll         # MOD 备份
```

---

> **最后更新**: 2026/03/30  
> **文档整理**: crosak
