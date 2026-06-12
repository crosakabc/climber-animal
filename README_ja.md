# 🐾 AnimalTransferMod

<!-- MULTILANG_NAV_START -->
[🇨🇳 中文](./README.md) | [🇬🇧 English](./README_en.md) | **🇯🇵 日本語**
<!-- MULTILANG_NAV_END -->

---

<p align="center">
  <img src="https://img.shields.io/badge/game-Climber%20Animals%20Together-blue?style=for-the-badge" alt="Game">
  <img src="https://img.shields.io/badge/melonloader-v0.7.2-green?style=for-the-badge" alt="MelonLoader">
  <img src="https://img.shields.io/badge/version-2026.03.30-orange?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/license-MIT-lightgrey?style=for-the-badge" alt="License">
</p>

<h1 align="center">🐾 AnimalTransferMod</h1>
<p align="center"><strong>Climber Animals Together — プレイヤーテレポート & 位置ロールバック MOD</strong></p>

---

## 📖 概要

**AnimalTransferMod** は、『Climber Animals Together』向けの MelonLoader MOD で、プレイヤー間テレポート、カスタム座標テレポート、**位置セーブ/ロールバック**機能を提供します。

最大の特徴は**安定した位置ロールバックシステム**です。現在位置をいつでも保存し、失敗を恐れずに挑戦して、ワンキーで元の位置に戻れます。**実績解除にも影響しません**。

---

## ✨ 機能

| 機能 | 説明 |
|------|------|
| 📍 **リアルタイム座標表示** | ルーム内の全オンラインプレイヤーの座標をリアルタイム表示 |
| 🚀 **ターゲットへテレポート** | ワンクリックでターゲットプレイヤーの近くにテレポート |
| 🔄 **ターゲットを自分にテレポート** | ターゲットプレイヤーを自分の位置に引き寄せ |
| 🎯 **カスタム座標テレポート** | X/Y/Z 座標を入力して正確にテレポート |
| 💾 **位置セーブ/ロールバック** | `Ctrl+S` でセーブ、`Ctrl+Z` でロールバック — 無限リトライ |

---

## 🚀 クイックスタート

### 前提条件

- [MelonLoader](https://github.com/LavaGang/MelonLoader) v0.7.2+
- [Climber Animals Together](https://store.steampowered.com/) (Steam)

### 1. MelonLoader のインストール

[MelonLoader.Installer.exe](https://github.com/LavaGang/MelonLoader/releases/download/v0.7.2/MelonLoader.Installer.exe) をダウンロードし、管理者として実行：

```
1. SELECT をクリック → ゲーム実行ファイル（Climber Animals Together.exe）を選択
2. INSTALL をクリック
3. インストーラーが自動的に依存関係をダウンロードし、Mods / Plugins / UserData フォルダを生成
```

### 2. MOD のインストール

```bash
# AnimalTransferMod.dll を Mods フォルダに配置
D:\steam\steamapps\common\Climber Animals Together\Mods\
│
├── AnimalTransferMod.dll          # ← 本 MOD
└── AnimalTransferMod_Save.txt     # ← 座標セーブファイル（自動生成）
```

### 3. ゲームを起動

ゲーム起動時に MOD が自動的に読み込まれます。**F4** を押してテレポートメニューを開きます。

---

## 🎮 使用方法

### テレポートメニュー

```
F4  →  テレポート GUI を開く / 閉じる
```

### テレポート機能

1. **座標の表示** — メニューにルーム内の全プレイヤーのリアルタイム座標が表示されます
2. **ターゲットへテレポート** — ターゲットプレイヤーを選択し、クリックでその近くに移動
3. **ターゲットを引き寄せ** — ターゲットプレイヤーを自分の位置にテレポート
4. **カスタム座標** — X/Y/Z を手動入力して任意の位置に正確にテレポート

---

## 💾 ロールバックシステム

> ⭐ **本 MOD の中核機能**：安定した位置ロールバック、無限リトライ、実績に影響なし。

### セーブ

```
Ctrl + S
```

現在のキャラクター位置座標を `AnimalTransferMod_Save.txt` に保存します。

### ロード / 復元

```
Ctrl + Z
```

最後に保存した座標を読み取り、キャラクターをその位置にテレポートします。

### 典型的な使用例

```
高難易度のジャンプに挑戦しようとしている
    ↓
Ctrl+S   現在位置をセーブ
    ↓
挑戦する（落下しても大丈夫）
    ↓
Ctrl+Z   セーブした位置に戻る
    ↓
成功するまで再挑戦 ✨
```

---

## 🐛 既知の問題

| 問題 | 状態 | 解決策 |
|------|------|--------|
| テレポート後のネットワーク変動によるフラッシュバック | 🟡 監視中 | テレポートを再試行 |
| ロールバック後にキャラクターが地形にはまることがある | 🟡 監視中 | ジャンプで回復 |
| GUI を長時間開いているとわずかにフレーム低下 | 🟡 最適化中 | 使用後は閉じる |

---

## 🗺 ロードマップ

- [ ] ロールバック時にゲーム内タイマーも同期復元
- [ ] チームメイト座標のクリック可能化でワンクリックテレポート
- [ ] マルチプレイ機能の深度最適化
- [ ] GUI パフォーマンス最適化によるフレーム影響の低減
- [ ] 複数セーブスロット対応

---

## 🤝 コントリビューション

Issue や PR を歓迎します！

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/crosakabc">crosakabc😀</a>
</p>
