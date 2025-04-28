---
layout: custom
title: ⬇️Installation
parent: Menno
nav_order: 1
permalink: /menno/installation/
lang: en
---

# Menno - Installation

This page explains how to install the Menno avatar.

## Structure of Downloaded Files

When you extract the files downloaded from BOOTH, you will see the following structure:

```
📁 License
   📄 en.pdf
   📄 ja.pdf
   📄 ko.pdf
   📄 zh.pdf
📁 Resources
   📁 Menno
      📁 FBX
      📁 Texture
   📁 ToggleProps
      📁 FBX
      📁 Texture
📄 1. liltoon and MA.unitypackage
📄 2. Menno.unitypackage
```

* **License** - License information in various languages
* **Resources** - Resource files including FBX and textures for the avatar
* **1. liltoon and MA.unitypackage** - The first package to import (includes liltoon and Modular Avatar)
* **2. Menno.unitypackage** - The second package to import containing the Menno avatar

## Prerequisites

To use the Menno avatar, you will need:

* [VRChat Creator Companion (VCC)](https://vcc.docs.vrchat.com/#download-it)
* Unity 2022.3.x (installed through VCC)
* Liltoon
  (installed through 1. liltoon and MA.unitypackage)
* Modular Avatar
  (installed through 1. liltoon and MA.unitypackage)

## Installation Steps (Using VCC)

### 1. Set up VRChat Creator Companion

1. Download and install VRChat Creator Companion (VCC) from the [VRChat official site](https://vrchat.com/home/download) or [VCC Download It](https://vcc.docs.vrchat.com/#download-it)
2. Launch VCC and complete the initial setup
   - Install Unity Hub if needed
   - Install Unity 2022.3.x

### 2. Create an Avatar Project with VCC

1. Click "Create New Project" in VCC
2. Choose a project name and location
3. Select "Avatar" as the template
4. Click the "Create Project" button
5. Once the project is created, click "Open in Unity"

### 3. Import Required Packages

1. Double-click `1. liltoon and MA.unitypackage` to import
   - This package adds liltoon and Modular Avatar
   - If you have already installed Modular Avatar through VCC, you can skip this step
2. Click the "Import" button in the import window

### 4. Import Menno Avatar

1. Double-click `2. Menno.unitypackage` to import
2. Click the "Import" button in the import window
3. After importing, the avatar will be placed in the `Assets/emudotto/Menno` folder
   - M. Avatar Setting is also imported at this point. You don't need to import it separately.

### 5. Place the Avatar in a Scene

You can place the avatar in a scene using one of the following methods:

#### Method 1: Use the Sample Scene (Recommended)
1. In the Unity Project view, find `Assets/emudotto/Menno/MennoScene.unity`
2. Double-click `MennoScene.unity` to open it
   - This scene already has the Menno avatar placed
   - Environment and lighting are already set up

#### Method 2: Add the Avatar to an Existing Scene
1. In the Unity Project view, find `Assets/emudotto/Menno/Menno.prefab`
2. Drag and drop Menno.prefab into the scene view

### 6. Configure the Avatar

1. Select the Menno object in the scene
2. Open M. Avatar Setting ([Details here](/avatar-setting/))
   - Select `Window > M Avatar Setting` from the Unity menu
   - Or click on Menno in the Inspector and click the "Open M. Avatar Setting" button
3. Configure the avatar settings as needed

### 7. Upload to VRChat

1. Select the Menno object in the scene
2. Open the VRChat SDK Control Panel
3. Click the "Build & Publish" button
4. Enter the required information and complete the upload 