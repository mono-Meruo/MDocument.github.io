---
layout: custom
title: ❓よくある質問（FAQ）
parent: Menno
nav_order: 7
permalink: /menno/faq/
lang: ja
---

# Mennoアバター - よくある質問（FAQ）

このページでは、Mennoアバターに関するよくある質問と解決方法をまとめています。

## 目次

1. [EyePointerが正常に動作しない](#eyepointer問題)
2. [特定の衣装で姿勢がおかしくなる問題](#衣装の問題)

## EyePointer問題

### 症状
EyePointerを導入しても目が動かない、または正常に視線誘導が機能しない。

### 原因
Mennoアバターは`UpperChest`ボーンを持っているため、標準のEyePointerアニメーションがこのボーン構造に対応していません。

### 製品情報
[Siromori Eye Pointer](https://booth.pm/ja/items/4742883)は、アバターの視線をコントロールするためのギミックです。

### 解決方法

#### M Avatar Setting v1.2.8以降をお持ちの場合

1. [Menno_v1.01_M.AvatarSetting_v1.2.8.zip](https://emudotto.booth.pm/items/3958356)をダウンロードします
2. **重要**: インポート時にはScriptsフォルダのみをチェックしてください（他のフォルダをインポートするとMennoのテクスチャやマテリアルが上書きされる可能性があります）
3. Unityエディタ上部のメニューから`Window > M Avatar Setting`を開きます
4. ウィンドウの一番下のデバッグセクションを展開し、「fixEyePointer」ボタンをクリックします
5. これによりMennoアバターのUpperChestボーン構造に対応したEyePointerアニメーションが適用されます

#### 手動で修正する場合

EyePointerのアニメーションパスを手動で修正する必要があります：

1. 以下のアニメーションファイルを探します:
   - Assets/Siromori/EyePointer/Animations/Toggle_Off.anim
   - Assets/Siromori/EyePointer/Animations/Toggle_On.anim
   - Assets/Siromori/EyePointer/Animations/Toggle_On_NoLook.anim
2. これらのファイルにある目のボーンパス（`Armature/Hips/Spine/Chest/Neck/Head/LeftEye`など）を
   `Armature/Hips/Spine/Chest/UpperChest/Neck/Head/LeftEye`のように修正します

## 衣装の問題

### 症状
特定の衣装を着用すると、Zボタンでしゃがんだ後に姿勢が元に戻らない、または挙動がおかしくなる。

### 影響する衣装の例
- Pirouetteさんの「[Arcane Attire](https://booth.pm/ja/items/6151859)」：魔法使い風の衣装セット
- ISHTAR LIBERALISさんの「[Theologica](https://booth.pm/ja/items/6350299)」：修道女風の衣装セット

### 原因
これらの衣装には、Armature直下にShape TypeがPlaneのコライダーオブジェクトが配置されており、そのオブジェクトのX軸回転が90度に設定されていることが問題を引き起こしています。

### 解決方法

#### 「Arcane Attire」の場合
1. BOOTHのArcane Attireダウンロードページに含まれる「plusheadのルェルツ_Rwerutu_に着せる方へ.png」の手順に従ってください
2. 具体的には、コライダーオブジェクトのX軸回転を90度から0度に変更します

#### 「Theologica」の場合
同様に、衣装のコライダーオブジェクトのX軸回転を確認し、90度から0度に変更することで問題が解決します。

## その他の質問

質問や問題がある場合は、[X(Twitter)](https://x.com/_emudotto)にてご連絡ください。 