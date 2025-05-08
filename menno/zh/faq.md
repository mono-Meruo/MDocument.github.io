---
layout: custom
title: ❓常见问题（FAQ）
parent: Menno
nav_order: 7
permalink: /menno/zh/faq/
lang: zh
---

# Menno 角色 - 常见问题（FAQ）

本页面汇总了关于Menno角色的常见问题及解决方法。

## 目录

1. [EyePointer不能正常工作](#eyepointer问题)
2. [特定服装导致姿势异常的问题](#服装问题)

## EyePointer问题

### 症状
使用EyePointer后眼睛不动，或者视线引导功能无法正常工作。

### 原因
Menno角色拥有`UpperChest`骨骼，而标准的EyePointer动画不兼容这种骨骼结构。

### 产品信息
[Siromori Eye Pointer](https://booth.pm/ja/items/4742883)是一个用于控制角色视线的工具。

### 解决方法

#### 如果您使用M Avatar Setting v1.2.8或更高版本

1. 下载[Menno_v1.01_M.AvatarSetting_v1.2.8.zip](https://emudotto.booth.pm/items/3958356)
2. **重要**：导入时仅勾选Scripts文件夹（导入其他文件夹可能会覆盖Menno的纹理和材质）
3. 从Unity编辑器顶部菜单打开`Window > M Avatar Setting`
4. 展开窗口底部的Debug部分，点击"fixEyePointer"按钮
5. 这将应用兼容Menno角色UpperChest骨骼结构的EyePointer动画

#### 手动修复

您需要手动修改动画路径：

1. 找到以下动画文件：
   - Assets/Siromori/EyePointer/Animations/Toggle_Off.anim
   - Assets/Siromori/EyePointer/Animations/Toggle_On.anim
   - Assets/Siromori/EyePointer/Animations/Toggle_On_NoLook.anim
2. 将这些文件中的眼睛骨骼路径（如`Armature/Hips/Spine/Chest/Neck/Head/LeftEye`）
   修改为`Armature/Hips/Spine/Chest/UpperChest/Neck/Head/LeftEye`

## 服装问题

### 症状
当使用特定服装时，按Z键蹲下后姿势无法恢复正常，或行为异常。

### 受影响的服装示例
- Pirouette的"[Arcane Attire](https://booth.pm/ja/items/6151859)"：魔法师风格服装套装
- ISHTAR LIBERALIS的"[Theologica](https://booth.pm/ja/items/6350299)"：修女风格服装套装

### 原因
这些服装在Armature下直接放置了Shape Type为Plane的碰撞器对象，且该对象的X轴旋转设置为90度，这导致了移动问题。

### 解决方法

#### 对于"Arcane Attire"
1. 按照BOOTH上Arcane Attire下载页面中包含的"plusheadのルェルツ_Rwerutu_に着せる方へ.png"图片指示操作
2. 具体来说，将碰撞器对象的X轴旋转从90度改为0度

#### 对于"Theologica"
同样，检查服装的碰撞器对象并将其X轴旋转从90度改为0度，即可解决问题。

## 其他问题

如有其他问题，请通过[X(Twitter)](https://x.com/_emudotto)联系我们。 