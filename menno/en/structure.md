---
layout: custom
title: Structure
parent: Menno
nav_order: 3
permalink: /menno/structure/
lang: en
---

# Menno - Structure

This page explains the folder structure and file organization of the Menno avatar.

## Folder Structure

The Menno avatar files are organized in the following folder structure:

```
Assets/emudotto/Menno/
├── Animation/            # Animation files
│   ├── ModularAvatar/    # Objects for ModularAvatar
│   │   └── Costume/      # Toggles for costume switching used in M. Avatar Setting
│   └── Controllers/      # Animation controllers
├── FBX/                  # 3D model files
├── Materials/            # Material files
│   ├── Presets/          # Presets for hair color etc.
│   └── Tex_Main/         # Texture files
├── Materials_Props/      # Material files for items
│   └── Tex_Props/        # Texture files
├── Prefab/               # Prefab files
│   └── ToggleProps.prefab # Prefab for items
├── Menno.prefab          # Main prefab for Menno avatar
└── MennoScene.unity      # Scene
```

## Main Files Description

### Menno.prefab

This is the main prefab file for the Menno avatar. You can use this avatar by dragging and dropping this file into a scene. It includes the following main components:

- VRC Avatar Descriptor - Settings for VRChat avatar
- M Avatar Setup Helper - Integration with M. Avatar Setting
- Animator - Animation control
- Modular Avatar component group - Avatar customization

### Avatar Hierarchy Structure

The hierarchy structure of the Menno prefab is as follows:

```
Menno (root object)
├── Armature          # Avatar bones
├── Body              # Body mesh
├── Hair              # Hair mesh
├── Hair_Bangs        # Bangs mesh
├── Belt              # Belt mesh
├── Boots             # Boots mesh
├── Coat              # Coat mesh
├── Jacket            # Jacket mesh
├── Karada            # Body detail mesh
├── Pants             # Pants mesh
├── Shirt             # Shirt mesh
├── Tie               # Tie mesh
├── AutoAnchorObject  # Anchor point
├── MTear             # Tear effect
├── Costume           # Object for costume switching
└── ToggleProps       # Object for toggle items
```

## Notes for Customization

- When changing materials or textures, it is recommended to create backups of the original files 