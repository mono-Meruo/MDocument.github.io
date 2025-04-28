---
layout: default
title: 構造説明
parent: Menno
nav_order: 3
permalink: /menno/structure/
---

# Menno - 構造説明

このページでは、Mennoアバターのフォルダ構造とファイル構成について説明します。

## フォルダ構造

Mennoアバターのファイルは以下のフォルダ構造で組織されています：

```
Assets/emudotto/Menno/
├── Animation/            # アニメーションファイル
│   ├── ModularAvatar/    # ModularAvatar用のアニメーション
│   │   └── Costume/      # 衣装切り替え用アニメーション
│   └── Controllers/      # アニメーションコントローラー
├── FBX/                  # 3Dモデルファイル
├── Materials/            # マテリアルファイル
│   ├── Presets/          # 髪の色などのプリセット
│   └── Tex_Main/         # テクスチャファイル
├── Prefab/               # プレハブファイル
│   └── ToggleProps.prefab # トグルアイテム用プレハブ
├── Resources/            # リソースファイル
├── Settings/             # 設定ファイル
├── Menno.prefab          # Mennoアバターのメインプレハブ
└── MennoScene.unity      # テスト用シーン
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
│   └── Hips          # ルートボーン
│       ├── Spine     # 背骨
│       └── ...       # その他のボーン
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
├── AnchorPoint       # アンカーポイント
├── MTear             # 涙のエフェクト
├── Costume           # 衣装切り替え用オブジェクト
└── ToggleProps       # トグルアイテム用オブジェクト
```

## マテリアル構成

Mennoアバターでは、以下の主要なマテリアルが使用されています：

1. **Menno_Body.mat** - 体のマテリアル
2. **Menno_Hair.mat** - 髪の毛のマテリアル
3. **Menno_Hair_Bangs.mat** - 前髪のマテリアル
4. **Menno_Eye.mat** - 目のマテリアル
5. **Menno_Wear.mat** - 衣装のマテリアル

これらのマテリアルはLiltoonシェーダーを使用しており、`_MainTex`（メインテクスチャ）、`_Color`（色調整）、`_LightMinLimit`（明るさの下限）などのプロパティを含んでいます。

## アニメーションシステム

アニメーションファイルは`Animation`フォルダに保存されています：

- **Controllers/Menno_Layer_FX.controller** - 表情やトグルアイテムを制御するアニメーションコントローラー
- **ModularAvatar/Costume/** - 衣装切り替え用のアニメーションファイル

## カスタマイズ時の注意点

- マテリアルやテクスチャを変更する場合は、元のファイルのバックアップを作成することをおすすめします