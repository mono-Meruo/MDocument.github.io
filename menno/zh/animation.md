---
layout: default
title: 动画结构
parent: Menno
nav_order: 4
permalink: /menno/animation/
lang: zh
---

# Menno - 动画结构

## 动画文件夹结构

Menno的动画相关文件整理在以下文件夹中：

```
Assets/emudotto/Menno/Animation/
├── AnimaitonLayer/ - 动画控制器
├── FX_Body/ - 身体动画
├── FX_Face/ - 表情动画
├── FX_ToggleProp/ - 切换道具动画
├── Gesture/ - 手势动画
├── Locomotion/ - 移动动画
├── ModularAvatar/ - ModularAvatar扩展
└── Parameters/ - VRChatSDK菜单和参数设置
```

## 动画控制器

### Menno_Layer_FX.controller

Menno虚拟形象的主要动画控制器是`AnimaitonLayer/Menno_Layer_FX.controller`。该控制器管理表情、身体光照、切换道具等。

FX控制器的主要结构如下：

```
Menno_Layer_FX.controller
├── 表情状态机
│   ├── 初始状态_Base
│   ├── 微笑_Smile
│   ├── 悲伤_Sad
│   └── 其他表情...
├── 身体光照状态机
│   ├── 光照_OFF
│   └── 光照_ON
└── 切换道具状态机
    ├── Pan_OFF / Pan_ON
    ├── Xondle_OFF / Xondle_ON
    └── Mokia_OFF / Mokia_ON
```

### Menno_Layer_Gesture.controller

`AnimaitonLayer/Menno_Layer_Gesture.controller`控制手部手势。

### Menno_Props.controller & Menno_Props_Gesture.controller

这些控制器管理道具的切换操作和相关手势。
通过Modular Avatar上传后，它们会与FX层集成。

## 表情动画 (FX_Face)

默认的Menno虚拟形象包含以下表情动画：

| 动画名称 | 说明 |
|--------------|------|
| Menno_初始状态_Base | 初始状态 |
| Menno_微笑_Smile | 微笑表情 |
| Menno_悲伤_Sad | 悲伤表情 |
| Menno_愤怒_Angry | 愤怒表情 |
| Menno_惊讶_surprise | 惊讶表情 |
| Menno_哭泣_Cry | 哭泣表情 |
| Menno_爱心_Heart | 眼睛变成心形的表情 |
| Menno_吐舌_Tongue | 吐舌头表情 |
| Menno_平静_Calm | 放松的表情 |
| Menno_闭眼_Sleep | 闭眼表情 |
| Menno_寒冷_Cold | 感到寒冷的表情 |
| Menno_焦急_Impatience | 焦急表情 |

此外还准备了许多其他表情，可以从ExpressionMenu中选择。

## 身体动画 (FX_Body)

身体动画包括以下内容：

- **Menno_Body_Lighting** - 身体光照调整
- **Menno_Body_Cheek** - 通过PhysBone拉动脸颊
- **Menno_Body_Cheek_L** - 通过PhysBone拉动左脸颊
- **Menno_Body_Cheek_R** - 通过PhysBone拉动右脸颊

## 参数设置 (Parameters)

Menno虚拟形象使用以下ExpressionMenu和Parameters：

- **Menno_ExpressionParameters.asset** - 基本参数设置
- **Menno_ExpressionsMenu.asset** - 主菜单
- **Menno_FaceMenu.asset** - 表情菜单
- **Menno_FaceMenu1.asset**, **Menno_FaceMenu2.asset**, **Menno_FaceMenu3.asset** - 附加表情菜单
- **Menno_Props.asset**, **Menno_Props_SubMenu.asset** - 道具菜单

### 主要参数列表

| 参数名称 | 类型 | 说明 |
|--------------|------|------|
| VRCFaceBlendH | Float | 水平方向表情混合（VRChat标准） |
| VRCFaceBlendV | Float | 垂直方向表情混合（VRChat标准） |
| GestureLeft | Int | 左手手势（VRChat标准） |
| GestureRight | Int | 右手手势（VRChat标准） |
| GestureLeftWeight | Float | 左手手势强度（VRChat标准） |
| GestureRightWeight | Float | 右手手势强度（VRChat标准） |
| FacialExpression | Int | 表情选择 |
| BodyLighting | Float | 身体光照调整 |
| Cheek | Bool | 脸颊拉动ON/OFF |
| CheekLeft | Bool | 左脸颊拉动ON/OFF |
| CheekRight | Bool | 右脸颊拉动ON/OFF |
| TogglePan | Bool | 平底锅显示/隐藏 |
| ToggleXondle | Bool | Xondle/Xontra显示/隐藏 |
| ToggleMokia | Bool | 手机显示/隐藏 |

## 表情使用方法

Menno虚拟形象的表情可以通过以下方式使用：

### 1. 从动作菜单选择

打开VRChat的动作菜单（PC上是R键，VR中是动作菜单按钮），从Menno的表情菜单中选择表情。

表情菜单的层次结构如下：

```
主菜单
├── 表情
│   ├── 基本表情
│   │   ├── 微笑
│   │   ├── 悲伤
│   │   └── ...
│   ├── 特殊表情
│   │   ├── 爱心眼
│   │   ├── 火焰眼
│   │   └── ...
│   └── 情感表达
│       ├── 焦急
│       ├── 寒冷
│       └── ...
└── 道具
    ├── 平底锅
    ├── 蜡烛
    └── 手机
``` 