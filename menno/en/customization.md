---
layout: custom
title: Customization
parent: Menno
nav_order: 2
permalink: /menno/customization/
lang: en
---

# Menno - Customization

This page explains how to customize the Menno avatar.

## Texture Customization

### 1. Texture File Location

Menno's main texture files are stored in the following location:

```
Assets/emudotto/Menno/Materials/Tex_Main/
```

### 2. Editing Textures

1. Open the texture files (PSD) in Photoshop, Gimp, or other image editing software
2. Make the necessary edits and save
3. When you return to the Unity project, the changes will be applied automatically


## Material Customization

### 1. Material Location

Menno's materials are stored in the following location:

```
Assets/emudotto/Menno/Materials/
```

### 2. Editing Materials

1. Select the material file in the Project window or by selecting an object in the hierarchy
2. [Adjust the liltoon material parameters](https://lilxyzw.github.io/lilToon/en_us/first.html) in the Inspector window


## Adding Costumes

### 1. Creating New Costumes

1. Create or purchase a costume
2. Click on the Unity package and import it into Unity

### 2. Adding Costumes Using ModularAvatar

ModularAvatar makes it easy to add new costumes to the Menno avatar.

#### 2.1 Simple Costume Setup

1. Place the new costume model as a child object of Menno
2. Right-click on the costume object and select `[ModularAvatar] Setup Outfit`
   - Modular Avatar will automatically detect the costume's armature and add the Merge Armature component
3. The costume will now automatically follow Menno avatar's bones

#### 2.2 Setting Up Costume Toggle

To make the costume switchable from the Expression Menu:

1. Select the costume object
2. Add the MA Toggle Object component from Add Component
3. Set the "Default State" (on or off)
4. Enter the name you want to display in "Menu Item Name"
5. Optionally, set an icon and menu hierarchy

Once these settings are complete, the new costume will be properly added to the Menno avatar and can be toggled from the Expression Menu.

## Changing Animations

### 1. Animation File Location

Menno's animation files are stored in the following location:

```
Assets/emudotto/Menno/Animation/
```

### 2. Editing Animations

1. Select the animation file in the Project window
2. Open the Animation Window
3. Add or edit keyframes
4. Save your changes

## Adding Expressions

### 1. Using Blend Shapes

1. Select the Menno avatar in the scene
2. Select the Body mesh's skinned mesh renderer
3. Adjust expressions in the Blend Shapes section of the Inspector
4. Record the adjusted expressions as keyframes in the Animation window

## Important Notes

* When making significant modifications, it's recommended to create backups of the original files 