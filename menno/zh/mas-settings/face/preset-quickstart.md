---
layout: custom
title: 🎭面部混合形状预设（快速入门）
parent: ⚙️面部设置
grand_parent: ⚙️M. Avatar Setting
great_grand_parent: Menno
nav_order: 2
permalink: /menno/mas-settings/face/preset-quickstart/
lang: zh

---

# 面部形状键预设功能 - 快速入门

使用 M. Avatar Setting 的混合形状预设功能，您可以保存喜欢的混合形状，并随时轻松调用。

![预设功能界面]({{ site.baseurl }}/assets/images/preset_ui.png)

## 保存预设的方法

### 1. 调整混合形状
首先，在面部设置中创建您喜欢的混合形状。

### 2. 输入预设名称
在"形状键预设"部分，输入预设名称。
- 默认会自动输入类似 `Menno_Face_Preset_01` 的名称
- 您可以更改为更易理解的名称（例如："儿童"、"成人"、"娃娃脸"等）

### 3. 点击保存按钮
点击"保存"按钮，当前的混合形状设置将被保存为预设。

## 使用预设的方法

### 1. 从已保存的预设中选择
您保存的预设会显示在"已保存的预设"部分。

### 2. 使用强度滑块应用
每个预设都有一个"强度"滑块：
- **0%**: 不应用预设
- **50%**: 以一半强度应用预设
- **100%**: 完全应用预设
![assets]({{ site.baseurl }}/assets/images/preset_assets_slider2.gif)

### 3. 实时预览
移动滑块时，混合形状会实时变化。

## 便利功能

### 预设混合
您可以同时应用多个预设来创建新的混合形状。
- 例如：应用"儿童"50%、"成人"30%，创建您喜欢的混合形状设置。

### 访问预设文件夹
点击"已保存的预设："旁边的📁按钮，可以在项目窗口中打开预设文件夹。

### 删除预设
点击每个预设的"X"按钮，确认后即可删除预设。

## 注意事项

- 预设按项目保存
- 重启 Unity 后预设仍会保留
- 预设文件保存在 `Assets/emudotto/Menno/Resources/Face_Presets` 