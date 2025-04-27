---
layout: default
title: 改変方法
parent: Menno
nav_order: 2
permalink: /menno/customization/
---

# Menno - 改変方法

このページでは、Mennoアバターの改変方法について説明します。

## テクスチャの改変

### 1. テクスチャファイルの場所

Mennoの主要なテクスチャファイルは以下の場所に保存されています：

```
Assets/emudotto/Menno/Materials/Tex_Main/
```

### 2. テクスチャの編集

1. テクスチャファイル(PSD)をPhotoshopやGimpなどの画像編集ソフトで開く
2. 必要な編集を行い保存
3. Unityプロジェクトに戻ると、変更が自動的に反映されます


## マテリアルの改変

### 1. マテリアルの場所

Mennoのマテリアルは以下の場所に保存されています：

```
Assets/emudotto/Menno/Materials/
```

### 2. マテリアルの編集

1. プロジェクトウィンドウ、またはヒエラルキーのオブジェクト選択でマテリアルファイルを選択
2. インスペクタウィンドウで[Liltoonマテリアルのパラメータを調整](https://lilxyzw.github.io/lilToon/ja_JP/first.html)


## 衣装の追加

### 1. 新しい衣装の作成

1. 衣装を作成または衣装を購入
2. Unitypackageをクリックし、Unityにインポート

### 2. ModularAvatarを使った衣装の追加

Modular Avatarを使用すると、新しい衣装を簡単にMennoアバターに追加できます。

#### 2.1 簡単な衣装のセットアップ

1. 新しい衣装モデルをMennoの子オブジェクトとして配置します
2. 衣装オブジェクトを右クリックし、`[ModularAvatar] Setup Outfit`を選択します
   - Modular Avatarが自動的に衣装のアーマチュアを検出し、Merge Armatureコンポーネントを追加します
3. これで衣装が自動的にMennoアバターのボーンに追従するようになります

#### 2.2 衣装のトグル設定

Expression Menuから衣装を切り替えられるようにするには：

1. 衣装オブジェクトを選択
2. Add ComponentからMA Toggle Objectコンポーネントを追加
3. 「デフォルト状態」を設定（オンまたはオフ）
4. 「メニュー項目名」に表示したい名前を入力
5. 必要に応じて、アイコンやメニュー階層を設定

これらの設定が完了すると、Mennoアバターに新しい衣装が適切に追加され、Expression Menuから切り替えられるようになります。

## アニメーションの変更

### 1. アニメーションファイルの場所

Mennoのアニメーションファイルは以下の場所に保存されています：

```
Assets/emudotto/Menno/Animation/
```

### 2. アニメーションの編集

1. プロジェクトウィンドウでアニメーションファイルを選択
2. Animation Windowを開く
3. キーフレームを追加・編集
4. 変更を保存

## 表情の追加

### 1. ブレンドシェイプの使用

1. シーンでMennoアバターを選択
2. Bodyメッシュのスキンメッシュレンダラーを選択
3. インスペクタのBlend Shapesセクションで表情を調整
4. Animationウィンドウで調整した表情をキーフレームとして記録

## 注意事項

* 大幅な改変を行う場合は、元のファイルのバックアップを作成してください
