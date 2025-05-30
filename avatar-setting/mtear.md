---
layout: custom
title: MTear涙エディター
parent: ⚙️M. Avatar Setting
nav_order: 3
lang: ja
permalink: /avatar-setting/mtear/
---

# MTear涙エディター

MTearは、VRChatアバター「Menno」用の涙エフェクトを編集するためのツールです。涙の流れる速度や形状、サイズなどを自由にカスタマイズできます。

<iframe width="560" height="315" src="https://www.youtube.com/embed/rcjnlMPjgCc?si=4v3UXY1mBSb9ByJN" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

- [概要](#概要)
- [使用方法](#使用方法)
- [涙メッシュエディター](#涙メッシュエディター)
- [シェーダー設定](#シェーダー設定)
- [プリセット](#プリセット)
- [応用例](#応用例)

## 概要

MTearは以下のコンポーネントで構成されています：

1. **MTearEditor** - アバターにアタッチするコンポーネント
2. **MTearEditorWindow** - 涙のメッシュを編集するためのウィンドウ
3. **Menno_Tear** - 涙のシェーダー
4. **MennoTearEditor** - シェーダーのカスタムインスペクター

これらのコンポーネントを組み合わせることで、涙の形状から見た目まで細かく調整できます。

## 使用方法

### 基本セットアップ

1. Mennoアバターを開きます
2. ヒエラルキーウィンドウで「Menno」オブジェクトを展開します
3. 「MTear」オブジェクトを選択します
4. インスペクターに表示される「MTearEditor」コンポーネントを確認します
5. 「涙メッシュを編集」ボタンをクリックします

![MTearインスペクター](../assets/images/mtear_inspector.jpg)

### インスペクターから編集

MTearEditorには、涙メッシュを編集するためのボタンが表示されます。
このボタンをクリックすると、専用のエディターウィンドウが開き、涙のメッシュを直接編集できるようになります。

## 涙メッシュエディター

MTearEditorWindowは、涙のメッシュ形状を編集するための専用ウィンドウです。

![涙メッシュエディター](../assets/images/mtear_editor.jpg)

### 主な機能

- **編集対象オブジェクト**: 涙メッシュを含むオブジェクトを選択
- **自動ミラーリング**: 左右のボーンを対称的に編集
- **色分け表示**: 左右のボーンを青と赤で区別
- **3D操作**: シーンビュー内で直接ボーンを移動・回転

### ボーンの操作方法

1. シーンビュー内で青または赤の球体（ボーン）をクリックして選択
2. 選択したボーンはハンドルが表示され、移動や回転が可能
3. 左右対称のボーンは自動的にミラーリングされます
4. インスペクターで位置、回転、スケールを数値で調整することも可能

※ ツールは自動的にViewツールに切り替わりますが、編集終了後は元のツールに戻ります。

## シェーダー設定

MTearは専用のシェーダー「Menno_Tear」を使用しています。このシェーダーには多数のパラメーターがあり、涙の見た目を調整できます。

![涙シェーダー設定](../assets/images/mtear_shader.jpg)

### 基本設定

- **涙の速度** (_Speed): 涙が流れる速さを調整
- **涙の位置** (_Tear_position): 涙の左右位置を調整

### 涙だまり設定

- **涙だまりの強さ** (_Tear_Puddle_intensity): 目の中の涙だまりの大きさを調整

### 涙滴設定

- **涙滴の強さ** (_Tear_Drop_intensity): 頬を流れる涙の強さ
- **涙滴のサイズ** (_Tear_Drop_Size): 涙滴の大きさ
- **追加涙滴の強さ** (_Tear_Drop_extra_intensity): 二次的な涙滴の強さ
- **追加涙滴のサイズ** (_Tear_Drop_extra_Size): 二次的な涙滴のサイズ

### 視覚効果

- **スペキュラ発光** (_Tear_Specular_Emissive): 涙の光沢の発光強度
- **スペキュラ強度** (_Tear_Specular_Strength): 涙の光沢の強さ
- **アウトライン** (_Tear_Outline): 涙の縁取りの強さ
- **アウトライン色** (_Tear_Outline_Color): 涙の縁取りの色
- **歪み** (_Tear_Distortion): 涙による背景の歪み具合

### ライティング設定

- **最小光量** (_LightMinLimit): 暗い環境での最小明るさ
- **最大光量** (_LightMaxLimit): 明るい環境での最大明るさ

## プリセット

MTearシェーダーには3つの標準プリセットが用意されています：

- **標準 (Default)**: バランスの取れた標準的な涙
- **小 (Small)**: 小さめの控えめな涙
- **大 (Big)**: 大きく目立つ涙

シェーダーエディターの下部にあるボタンからプリセットを適用できます。また、自分好みの設定をプリセットとして保存することも可能です。

## 応用例

- **悲しい表情と組み合わせる**: 泣き顔と共に使用することで感情表現を強化
- **涙の色を変える**: アウトライン色や発光設定でファンタジー風の涙を表現
- **異なる涙の大きさ**: シチュエーションに応じて涙の大きさを使い分け

---

*このドキュメントは随時更新されます。最終更新: 2025年5月* 