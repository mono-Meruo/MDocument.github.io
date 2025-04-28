---
layout: custom
title: 構造説明
parent: Menno
nav_order: 3
permalink: /menno/structure/
lang: ja
---

# Menno - 構造説明

このページでは、Mennoアバターのフォルダ構造とファイル構成について説明します。

## フォルダ構造

Mennoアバターのファイルは以下のフォルダ構造で組織されています：

```
Assets/emudotto/Menno/
├── Animation/            # アニメーションファイル
│   ├── ModularAvatar/    # ModularAvatar用のオブジェクト
│   │   └── Costume/      # M. Avatar Settingで使う衣装切り替え用Toggle
│   └── Controllers/      # アニメーションコントローラー
├── FBX/                  # 3Dモデルファイル
├── Materials/            # マテリアルファイル
│   ├── Presets/          # 髪の色などのプリセット
│   └── Tex_Main/         # テクスチャファイル
├── Materials_Props/      # アイテムのマテリアルファイル
│   └── Tex_Props/        # テクスチャファイル
├── Prefab/               # プレハブファイル
│   └── ToggleProps.prefab # アイテム用プレハブ
├── Menno.prefab          # Mennoアバターのメインプレハブ
└── MennoScene.unity      # シーン
```

## 主要ファイルの説明

### Menno.prefab

Mennoアバターのメインプレハブファイルです。このファイルをシーンにドラッグ＆ドロップすることでアバターを使用できます。以下の主要なコンポーネントが含まれています：

- VRC Avatar Descriptor - VRChatアバターの設定
- M Avatar Setup Helper - M. Avatar Settingとの連携
- Animator - アニメーションの制御
- Modular Avatar コンポーネント群 - アバターのカスタマイズ

### アバターの階層構造

Mennoプレハブの階層構造は以下のようになっています：

```
Menno (ルートオブジェクト)
├── Armature          # アバターのボーン
├── Body              # ボディメッシュ
├── Hair              # 髪の毛メッシュ
├── Hair_Bangs        # 前髪メッシュ
├── Belt              # ベルトメッシュ
├── Boots             # ブーツメッシュ
├── Coat              # コートメッシュ
├── Jacket            # ジャケットメッシュ
├── Karada            # 体のディテールメッシュ
├── Pants             # パンツメッシュ
├── Shirt             # シャツメッシュ
├── Tie               # ネクタイメッシュ
├── AutoAnchorObject  # アンカーポイント
├── MTear             # 涙のエフェクト
├── Costume           # 衣装切り替え用オブジェクト
└── ToggleProps       # トグルアイテム用オブジェクト
```

## カスタマイズ時の注意点

- マテリアルやテクスチャを変更する場合は、元のファイルのバックアップを作成することをおすすめします