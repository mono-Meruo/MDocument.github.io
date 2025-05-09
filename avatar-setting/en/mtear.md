---
layout: custom
title: MTear Tear Editor
parent: ⚙️M. Avatar Setting
nav_order: 3
lang: en
permalink: /avatar-setting/mtear/
---

<div style="text-align: right; margin-bottom: 20px;">
  <a href="../mtear.html" style="margin-right: 5px;">日本語</a>
  <a href="../ko/mtear.html" style="margin-right: 5px;">한국어</a>
  <a href="../zh/mtear.html">中文</a>
</div>

# MTear Tear Editor

MTear is a tool for editing tear effects for the VRChat avatar "Menno". You can freely customize the speed, shape, and size of tears.

- [Overview](#overview)
- [How to Use](#how-to-use)
- [Tear Mesh Editor](#tear-mesh-editor)
- [Shader Settings](#shader-settings)
- [Presets](#presets)
- [Application Examples](#application-examples)

## Overview

MTear consists of the following components:

1. **MTearEditor** - Component attached to the avatar
2. **MTearEditorWindow** - Window for editing tear mesh
3. **Menno_Tear** - Tear shader
4. **MennoTearEditor** - Custom inspector for the shader

By combining these components, you can adjust everything from the shape to the appearance of tears.

## How to Use

### Basic Setup

1. Open the Menno avatar
2. If there is no MTear component, add it to the "MTear" object
3. Select the MTearEditor component in the inspector
4. Click the "Edit Tear Mesh" button

![MTear Inspector](../../assets/images/mtear_inspector.jpg)

### Editing from the Inspector

The MTearEditor displays a button to edit the tear mesh.
Clicking the button will open a dedicated editor window.

## Tear Mesh Editor

MTearEditorWindow is a dedicated window for editing the tear mesh shape.

![Tear Mesh Editor](../../assets/images/mtear_editor.jpg)

### Main Features

- **Target Object**: Select the object containing the tear mesh
- **Auto Mirroring**: Edit left and right bones symmetrically
- **Color-Coded Display**: Distinguish left and right bones with blue and red colors
- **3D Manipulation**: Directly move and rotate bones in the scene view

### How to Manipulate Bones

1. Click on blue or red spheres (bones) in the scene view to select them
2. Selected bones display handles for movement and rotation
3. Left-right symmetrical bones are automatically mirrored
4. You can also adjust position, rotation, and scale numerically in the inspector

Note: The tool automatically switches to View Tool but returns to the original tool after editing.

## Shader Settings

MTear uses a dedicated shader "Menno_Tear". This shader has numerous parameters for adjusting the appearance of tears.

![Tear Shader Settings](../../assets/images/mtear_shader.jpg)

### Basic Settings

- **Speed** (_Speed): Adjust how fast tears flow
- **Position** (_Tear_position): Adjust the left-right position of tears

### Puddle Settings

- **Puddle Intensity** (_Tear_Puddle_intensity): Adjust the size of tear puddles in the eyes

### Drop Settings

- **Drop Intensity** (_Tear_Drop_intensity): Strength of tears flowing down the cheeks
- **Drop Size** (_Tear_Drop_Size): Size of tear drops
- **Extra Drop Intensity** (_Tear_Drop_extra_intensity): Strength of secondary tear drops
- **Extra Drop Size** (_Tear_Drop_extra_Size): Size of secondary tear drops

### Visual Effects

- **Specular Emissive** (_Tear_Specular_Emissive): Emission intensity of tear gloss
- **Specular Strength** (_Tear_Specular_Strength): Strength of tear gloss
- **Outline** (_Tear_Outline): Strength of tear outline
- **Outline Color** (_Tear_Outline_Color): Color of tear outline
- **Distortion** (_Tear_Distortion): Amount of background distortion caused by tears

### Lighting Settings

- **Min Light** (_LightMinLimit): Minimum brightness in dark environments
- **Max Light** (_LightMaxLimit): Maximum brightness in bright environments

## Presets

The MTear shader comes with three standard presets:

- **Default**: Balanced standard tears
- **Small**: Small, subtle tears
- **Big**: Large, prominent tears

You can apply presets from the buttons at the bottom of the shader editor. You can also save your preferred settings as a preset.

## Application Examples

- **Combine with sad expressions**: Enhance emotional expression by using with crying faces
- **Change tear color**: Express fantasy-style tears with outline color and emission settings
- **Different tear sizes**: Use different tear sizes depending on the situation

---

*This document is updated regularly. Last update: May 2025* 