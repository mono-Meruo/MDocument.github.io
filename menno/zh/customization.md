---
layout: custom
title: 自定义
parent: Menno
nav_order: 2
permalink: /menno/customization/
lang: zh
---

# Menno - 自定义

本页说明如何自定义Menno虚拟形象。

## 纹理自定义

### 1. 纹理文件位置

Menno的主要纹理文件存储在以下位置：

```
Assets/emudotto/Menno/Materials/Tex_Main/
```

### 2. 编辑纹理

1. 在Photoshop、Gimp或其他图像编辑软件中打开纹理文件（PSD）
2. 进行必要的编辑并保存
3. 当您返回Unity项目时，更改将自动应用

## 材质自定义

### 1. 材质位置

Menno的材质存储在以下位置：

```
Assets/emudotto/Menno/Materials/
```

### 2. 编辑材质

1. 在项目窗口中选择材质文件，或在层级中选择对象
2. 在Inspector窗口中[调整liltoon材质参数](https://lilxyzw.github.io/lilToon/en_us/first.html)

## 添加服装

### 1. 创建新服装

1. 创建或购买服装
2. 点击Unity包并将其导入Unity

### 2. 使用ModularAvatar添加服装

ModularAvatar使您可以轻松地将新服装添加到Menno虚拟形象中。

#### 2.1 简单服装设置

1. 将新服装模型作为Menno的子对象放置
2. 右键点击服装对象并选择`[ModularAvatar] Setup Outfit`
   - Modular Avatar将自动检测服装的骨骼并添加Merge Armature组件
3. 服装现在将自动跟随Menno虚拟形象的骨骼

#### 2.2 设置服装切换

要使服装可以从Expression Menu切换：

1. 选择服装对象
2. 从Add Component添加MA Toggle Object组件
3. 设置"Default State"（开启或关闭）
4. 在"Menu Item Name"中输入您想要显示的名称
5. 可选地，设置图标和菜单层级

完成这些设置后，新服装将正确添加到Menno虚拟形象中，并可以从Expression Menu切换。

## 更改动画

### 1. 动画文件位置

Menno的动画文件存储在以下位置：

```
Assets/emudotto/Menno/Animation/
```

### 2. 编辑动画

1. 在项目窗口中选择动画文件
2. 打开Animation Window
3. 添加或编辑关键帧
4. 保存更改

## 添加表情

### 1. 使用Blend Shapes

1. 在场景中选择Menno虚拟形象
2. 选择Body网格的skinned mesh renderer
3. 在Inspector的Blend Shapes部分调整表情
4. 在Animation窗口中记录调整后的表情作为关键帧

## 重要注意事项

* 进行重大修改时，建议创建原始文件的备份 