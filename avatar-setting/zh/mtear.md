---
layout: custom
title: MTear 泪水编辑器
parent: ⚙️M. Avatar Setting
nav_order: 3
lang: zh
permalink: /avatar-setting/mtear/
---

<div style="text-align: right; margin-bottom: 20px;">
  <a href="../mtear.html" style="margin-right: 5px;">日本語</a>
  <a href="../en/mtear.html" style="margin-right: 5px;">English</a>
  <a href="../ko/mtear.html">한국어</a>
</div>

# MTear 泪水编辑器

MTear 是一个为 VRChat 虚拟形象"Menno"设计的泪水效果编辑工具。您可以自由自定义泪水流动的速度、形状和大小等。

- [概述](#概述)
- [使用方法](#使用方法)
- [泪水网格编辑器](#泪水网格编辑器)
- [着色器设置](#着色器设置)
- [预设](#预设)
- [应用示例](#应用示例)

## 概述

MTear 由以下组件组成：

1. **MTearEditor** - 附加到虚拟形象的组件
2. **MTearEditorWindow** - 编辑泪水网格的窗口
3. **Menno_Tear** - 泪水着色器
4. **MennoTearEditor** - 着色器的自定义检查器

通过组合这些组件，您可以从泪水的形状到外观进行细致调整。

## 使用方法

### 基本设置

1. 打开 Menno 虚拟形象
2. 如果没有 MTear 组件，请将其添加到"MTear"对象
3. 在检查器中选择 MTearEditor 组件
4. 点击"编辑泪水网格"按钮

![MTear 检查器](../../assets/images/mtear_inspector.jpg)

### 从检查器编辑

MTearEditor 显示用于编辑泪水网格的按钮。
点击按钮将打开专用的编辑器窗口。

## 泪水网格编辑器

MTearEditorWindow 是一个用于编辑泪水网格形状的专用窗口。

![泪水网格编辑器](../../assets/images/mtear_editor.jpg)

### 主要功能

- **编辑目标对象**: 选择包含泪水网格的对象
- **自动镜像**: 对称编辑左右骨骼
- **颜色区分显示**: 用蓝色和红色区分左右骨骼
- **3D 操作**: 在场景视图中直接移动和旋转骨骼

### 骨骼操作方法

1. 在场景视图中点击蓝色或红色球体（骨骼）进行选择
2. 选中的骨骼会显示手柄，可以进行移动和旋转
3. 左右对称的骨骼会自动镜像
4. 也可以在检查器中通过数值调整位置、旋转和缩放

注意：工具会自动切换到查看工具，但编辑结束后会返回到原来的工具。

## 着色器设置

MTear 使用专用的"Menno_Tear"着色器。这个着色器有许多参数，可以调整泪水的外观。

![泪水着色器设置](../../assets/images/mtear_shader.jpg)

### 基本设置

- **泪水速度** (_Speed): 调整泪水流动的速度
- **泪水位置** (_Tear_position): 调整泪水的左右位置

### 泪水积聚设置

- **泪水积聚强度** (_Tear_Puddle_intensity): 调整眼睛内泪水积聚的大小

### 泪滴设置

- **泪滴强度** (_Tear_Drop_intensity): 流过脸颊的泪水强度
- **泪滴大小** (_Tear_Drop_Size): 泪滴的大小
- **额外泪滴强度** (_Tear_Drop_extra_intensity): 次要泪滴的强度
- **额外泪滴大小** (_Tear_Drop_extra_Size): 次要泪滴的大小

### 视觉效果

- **高光发光** (_Tear_Specular_Emissive): 泪水光泽的发光强度
- **高光强度** (_Tear_Specular_Strength): 泪水光泽的强度
- **轮廓** (_Tear_Outline): 泪水轮廓的强度
- **轮廓颜色** (_Tear_Outline_Color): 泪水轮廓的颜色
- **扭曲** (_Tear_Distortion): 泪水引起的背景扭曲程度

### 光照设置

- **最小光照** (_LightMinLimit): 暗环境中的最小亮度
- **最大光照** (_LightMaxLimit): 明亮环境中的最大亮度

## 预设

MTear 着色器提供了三种标准预设：

- **标准 (Default)**: 平衡的标准泪水
- **小型 (Small)**: 小而微妙的泪水
- **大型 (Big)**: 大而明显的泪水

您可以从着色器编辑器底部的按钮应用预设。您也可以将自己喜欢的设置保存为预设。

## 应用示例

- **与悲伤表情结合**: 与哭泣表情一起使用增强情感表达
- **更改泪水颜色**: 通过轮廓颜色和发光设置表达奇幻风格的泪水
- **不同泪水大小**: 根据情况使用不同大小的泪水

---

*本文档会定期更新。最后更新：2025年5月* 