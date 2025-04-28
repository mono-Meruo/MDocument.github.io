---
layout: default
title: アニメーション構造
parent: Menno
nav_order: 4
permalink: /menno/animation/
lang: ja
---

# Menno - アニメーション構造

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
└── Parameters/ - VRChatSDKのメニューとパラメーター設定
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

`AnimaitonLayer/Menno_Layer_Gesture.controller`は、手のジェスチャーを制御します。

### Menno_Props.controller & Menno_Props_Gesture.controller

これらのコントローラーは、アイテムのトグル操作と関連するジェスチャーを制御します。
Modular Avatarによりアップロード後、FXレイヤーと統合されます。

## 表情アニメーション (FX_Face)

デフォルトのMennoアバターは、以下のような表情アニメーションを持っています：

| アニメーション名 | 説明 |
|--------------|------|
| Menno_初期状態_Base | 初期状態 |
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
- **Menno_Body_Cheek** - PhysBoneによって頬が引っ張られます
- **Menno_Body_Cheek_L** - PhysBoneによって左頬が引っ張られます
- **Menno_Body_Cheek_R** - PhysBoneによって右頬が引っ張られます

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
| GestureLeftWeight | Float | 左手のジェスチャーの強さ（VRChat標準）  |
| GestureRightWeight | Float | 右手のジェスチャーの強さ（VRChat標準）  |
| FacialExpression | Int | 表情の選択 |
| BodyLighting | Float | 体のライティング調整 |
| Cheek | Bool | 頬のひっぱりON/OFF |
| CheekLeft | Bool | 左頬のひっぱりON/OFF |
| CheekRight | Bool | 左頬のひっぱりON/OFF |
| TogglePan | Bool | フライパンの表示/非表示 |
| ToggleXondle | Bool | Xondle・Xontraの表示/非表示 |
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
    ├── Xondle
    └── Mokia
```