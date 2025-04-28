---
layout: custom
title: 结构
parent: Menno
nav_order: 3
permalink: /menno/structure/
lang: zh
---

# Menno - 结构

本页说明Menno虚拟形象的文件夹结构和文件组织。

## 文件夹结构

Menno虚拟形象文件按以下文件夹结构组织：

```
Assets/emudotto/Menno/
├── Animation/            # 动画文件
│   ├── ModularAvatar/    # ModularAvatar对象
│   │   └── Costume/      # M. Avatar Setting中使用的服装切换开关
│   └── Controllers/      # 动画控制器
├── FBX/                  # 3D模型文件
├── Materials/            # 材质文件
│   ├── Presets/          # 发色等预设
│   └── Tex_Main/         # 纹理文件
├── Materials_Props/      # 道具材质文件
│   └── Tex_Props/        # 道具纹理文件
├── Prefab/               # 预制体文件
│   └── ToggleProps.prefab # 道具预制体
├── Menno.prefab          # Menno虚拟形象的主要预制体
└── MennoScene.unity      # 场景
```

## 主要文件说明

### Menno.prefab

这是Menno虚拟形象的主要预制体文件。您可以通过将此文件拖放到场景中来使用此虚拟形象。它包含以下主要组件：

- VRC Avatar Descriptor - VRChat虚拟形象设置
- M Avatar Setup Helper - 与M. Avatar Setting集成
- Animator - 动画控制
- Modular Avatar组件组 - 虚拟形象自定义

### 虚拟形象层级结构

Menno预制体的层级结构如下：

```
Menno (根对象)
├── Armature          # 虚拟形象骨骼
├── Body              # 身体网格
├── Hair              # 头发网格
├── Hair_Bangs        # 刘海网格
├── Belt              # 腰带网格
├── Boots             # 靴子网格
├── Coat              # 外套网格
├── Jacket            # 夹克网格
├── Karada            # 身体细节网格
├── Pants             # 裤子网格
├── Shirt             # 衬衫网格
├── Tie               # 领带网格
├── AutoAnchorObject  # 锚点
├── MTear             # 眼泪效果
├── Costume           # 服装切换对象
└── ToggleProps       # 切换道具对象
```

## 自定义注意事项

- 更改材质或纹理时，建议创建原始文件的备份 