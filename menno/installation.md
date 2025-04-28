---
layout: custom
title: ⬇️導入方法
parent: Menno
nav_order: 1
permalink: /menno/installation/
lang: ja
---

# Menno - 導入方法

このページでは、Mennoアバターの導入方法について説明します。

## ダウンロードしたファイルの構成

BOOTHからダウンロードしたファイルを解凍すると、以下のような構成になっています：

```
📁 License
   📄 en.pdf
   📄 ja.pdf
   📄 ko.pdf
   📄 zh.pdf
📁 Resources
   📁 Menno
      📁 FBX
      📁 Texture
   📁 ToggleProps
      📁 FBX
      📁 Texture
📄 1. liltoon and MA.unitypackage
📄 2. Menno.unitypackage
```

* **License** - 各言語のライセンス情報
* **Resources** - アバターのFBXやテクスチャなどのリソースファイル
* **1. liltoon and MA.unitypackage** - １番目にインポートするべきパッケージ（liltoonとModular Avatarが含まれています）
* **2. Menno.unitypackage** - ２番目にインポートするMennoアバター本体

## 前提条件

Mennoアバターを使用するには、以下が必要です：

* [VRChat Creator Companion (VCC)](https://vcc.docs.vrchat.com/#download-it)
* Unity 2022.3.x　（VCCを通じてインストール）
* Liltoon
　（1. liltoon and MA.unitypackageを通じてインストール）
* Modular Avatar
　（1. liltoon and MA.unitypackageを通じてインストール）

## 導入手順（VCC使用）

### 1. VRChat Creator Companionのセットアップ

1. [VRChat公式サイト](https://vrchat.com/home/download)または[VCC Donload It](https://vcc.docs.vrchat.com/#download-it)からVRChat Creator Companion (VCC)をダウンロード・インストールします
2. VCCを起動し、初回セットアップを完了させます
   - 必要に応じてUnity Hubのインストール
   - Unity 2022.3.xのインストール

### 2. VCCでAvatarプロジェクトを作成

1. VCCで「新規プロジェクト作成」をクリック
2. プロジェクト名とプロジェクトの保存先を選択
3. テンプレートとして「Avatar」を選択
4. 「プロジェクト作成」ボタンをクリック
5. プロジェクトが作成されたら「Unityで開く」をクリック

### 3. 必要なパッケージのインポート

1. `1. liltoon and MA.unitypackage`をダブルクリックしてインポート
   - これはliltoonとModular Avatarを追加するパッケージです
   - VCCからModular Avatarをすでにインストールしている場合は、このステップは不要です
2. インポートウィンドウで「Import」ボタンをクリック

### 4. Mennoアバターのインポート

1. `2. Menno.unitypackage`をダブルクリックしてインポート
2. インポートウィンドウで「Import」ボタンをクリック
3. インポートが完了したら、`Assets/emudotto/Menno`フォルダにアバターが配置されます
   - この時点でM. Avatar Settingも一緒にインポートされています。別途インポートする必要はありません。

### 5. アバターをシーンに配置

以下のいずれかの方法でアバターをシーンに配置できます：

#### 方法1: サンプルシーンを使用する（推奨）
1. Unityのプロジェクトビューで`Assets/emudotto/Menno/MennoScene.unity`を探す
2. `MennoScene.unity`をダブルクリックして開く
   - このシーンには既にMennoアバターが配置されています
   - 環境やライティングも設定済みです

#### 方法2: 既存のシーンにアバターを追加する
1. Unityのプロジェクトビューで`Assets/emudotto/Menno/Menno.prefab`を探す
2. Menno.prefabをシーンビューにドラッグ＆ドロップ

### 6. アバターの設定

1. シーン内のMennoオブジェクトを選択
2. M. Avatar Settingを開く（[詳細はこちら](/avatar-setting/)）
   - Unityのメニューから`Window > M Avatar Setting`を選択
   - または、Inspector上のMennoをクリックして、「M. Avatar Settingを開く」ボタンをクリック
3. 必要に応じてアバターの設定を行う

### 7. VRChatへのアップロード

1. シーン内のMennoオブジェクトを選択
2. VRChat SDKのコントロールパネルを開く
3. 「Build & Publish」ボタンをクリック
4. 必要な情報を入力してアップロード完了
