---
layout: default
title: アニメーション構造
parent: Menno
nav_order: 4
permalink: /menno/animation/
---

# Menno - アニメーション構造

このページでは、Mennoアバターのアニメーションシステムについて説明します。Mennoは、VRChatのAvatars 3.0システムを採用しており、複数のアニメーションレイヤーとパラメーターによって様々な表情や動きを実現しています。

## VRChat Avatars 3.0システムについて

VRChatのAvatars 3.0システムでは、アバターのアニメーションは以下の主要なレイヤーで構成されています：

- **Base** - 基本的な動き（歩行、走行、ジャンプなど）
- **Additive** - 基本動作に追加される動き
- **Gesture** - 手のジェスチャーを制御
- **Action** - アクションや特殊な動き
- **FX** - 表情やアイテムの表示/非表示など

Mennoでは、主に**FX**レイヤーと**Gesture**レイヤーをカスタマイズがされています。

### VRChat Avatars 3.0の構造

VRChat Avatars 3.0では、以下の3つの要素がアバターのアニメーションを制御しています：

1. **アニメーションコントローラー** - アニメーションの状態と遷移を管理
2. **Expression Parameters** - アバターのパラメーターを定義
3. **Expression Menu** - ユーザーが操作するメニュー

これらが連携して、アバターの表情や動きを制御します。

```
┌─────────────────┐       ┌──────────────────┐       ┌─────────────────┐
│ Expression Menu │──────▶│ Parameter Values │◀─────▶│ Animation       │
│ (UI操作)        │       │ (状態管理)        │       │ Controller      │
└─────────────────┘       └──────────────────┘       │ (アニメーション) │
                                  ▲                  └─────────────────┘
                                  │                          ▲
                                  │                          │
                                  ▼                          │
                          ┌──────────────────┐              │
                          │ Gesture          │──────────────┘
                          │ (ハンドジェスチャー)│
                          └──────────────────┘
```

## アニメーションフォルダ構造

Mennoのアニメーション関連ファイルは、以下のフォルダに整理されています：

```
Assets/emudotto/Menno/Animation/
├── AnimaitonLayer/ - アニメーションコントローラー
├── FX_Body/ - 体のアニメーション
├── FX_Face/ - 表情アニメーション
├── FX_ToggleProp/ - トグルアイテムアニメーション
├── Gesture/ - ジェスチャーアニメーション
├── Locomotion/ - 移動アニメーション
├── ModularAvatar/ - ModularAvatar拡張
└── Parameters/ - メニューとパラメーター設定
```

## アニメーションコントローラー

### Menno_Layer_FX.controller

Mennoアバターのメインアニメーションコントローラーは`AnimaitonLayer/Menno_Layer_FX.controller`です。このコントローラーは表情、ボディライティング、トグルアイテムなどを管理します。

FXコントローラーの主な構造は以下のようになっています：

```
Menno_Layer_FX.controller
├── 表情ステートマシン
│   ├── 初期状態_Base
│   ├── 笑顔_Smile
│   ├── 悲しみ_Sad
│   └── その他の表情...
├── ボディライティングステートマシン
│   ├── ライティング_OFF
│   └── ライティング_ON
└── トグルアイテムステートマシン
    ├── Pan_OFF / Pan_ON
    ├── Xondle_OFF / Xondle_ON
    └── Mokia_OFF / Mokia_ON
```

### Menno_Layer_Gesture.controller

`AnimaitonLayer/Menno_Layer_Gesture.controller`は、手のジェスチャーとそれに連動する表情を制御します。

ジェスチャーコントローラーの構造は以下のようになっています：

```
Menno_Layer_Gesture.controller
├── 左手ステートマシン
│   ├── Fist (グー)
│   ├── HandOpen (パー)
│   ├── FingerPoint (人差し指)
│   └── その他のジェスチャー...
└── 右手ステートマシン
    ├── Fist (グー)
    ├── HandOpen (パー)
    ├── FingerPoint (人差し指)
    └── その他のジェスチャー...
```

### Menno_Props.controller & Menno_Props_Gesture.controller

これらのコントローラーは、アイテムのトグル操作と関連するジェスチャーを制御します。

## 表情アニメーション (FX_Face)

Mennoアバターは、以下のような豊富な表情アニメーションを持っています：

| アニメーション名 | 説明 |
|--------------|------|
| Menno_初期状態_Base | 基本表情 |
| Menno_笑顔_Smile | 笑顔 |
| Menno_悲しみ_Sad | 悲しい表情 |
| Menno_怒り_Angry | 怒った表情 |
| Menno_驚愕_surprise | 驚いた表情 |
| Menno_泣く_Cry | 泣いている表情 |
| Menno_ハート_Heart | 目がハート形になる表情 |
| Menno_舌出し_Tongue | 舌を出す表情 |
| Menno_和み_Calm | リラックスした表情 |
| Menno_目閉じ_Sleep | 目を閉じた表情 |
| Menno_冷え_Cold | 寒そうな表情 |
| Menno_焦り_Impatience | 焦った表情 |

その他多数の表情が用意されており、ExpressionMenuから選択できます。

## ボディアニメーション (FX_Body)

体のアニメーションには以下のようなものがあります：

- **Menno_Body_Lighting** - 体のライティング調整
- **Menno_Body_Cheek** - 頬の赤みの調整
- **Menno_Body_Cheek_L** - 左頬の赤み
- **Menno_Body_Cheek_R** - 右頬の赤み

## パラメーター設定 (Parameters)

Mennoアバターでは、以下のExpressionMenuとParametersが使用されています：

- **Menno_ExpressionParameters.asset** - 基本パラメーター設定
- **Menno_ExpressionsMenu.asset** - メインメニュー
- **Menno_FaceMenu.asset** - 表情メニュー
- **Menno_FaceMenu1.asset**, **Menno_FaceMenu2.asset**, **Menno_FaceMenu3.asset** - 追加表情メニュー
- **Menno_Props.asset**, **Menno_Props_SubMenu.asset** - アイテムメニュー

### 主要パラメーター一覧

| パラメーター名 | タイプ | 説明 |
|--------------|------|------|
| VRCFaceBlendH | Float | 水平方向の表情ブレンド（VRChat標準） |
| VRCFaceBlendV | Float | 垂直方向の表情ブレンド（VRChat標準） |
| GestureLeft | Int | 左手のジェスチャー（VRChat標準） |
| GestureRight | Int | 右手のジェスチャー（VRChat標準） |
| GestureLeftWeight | Float | 左手のジェスチャーの強さ |
| GestureRightWeight | Float | 右手のジェスチャーの強さ |
| FacialExpression | Int | 表情の選択 |
| BodyLighting | Float | 体のライティング調整 |
| Cheek | Bool | 頬の赤みの表示/非表示 |
| CheekLeft | Bool | 左頬の赤みの表示/非表示 |
| CheekRight | Bool | 右頬の赤みの表示/非表示 |
| TogglePan | Bool | フライパンの表示/非表示 |
| ToggleXondle | Bool | キャンドルの表示/非表示 |
| ToggleMokia | Bool | 携帯電話の表示/非表示 |

## 表情の使い方

Mennoアバターの表情は以下の方法で使用できます：

### 1. アクションメニューから選択

VRChatのアクションメニュー（PCではRキー、VRではアクションメニューボタン）を開き、Mennoの表情メニューから表情を選択します。

表情メニューは以下のように階層化されています：

```
メインメニュー
├── 表情
│   ├── 基本表情
│   │   ├── 笑顔
│   │   ├── 悲しみ
│   │   └── ...
│   ├── 特殊表情
│   │   ├── ハート目
│   │   ├── 燃える目
│   │   └── ...
│   └── 感情表現
│       ├── 焦り
│       ├── 冷え
│       └── ...
└── アイテム
    ├── フライパン
    ├── キャンドル
    └── 携帯電話
```