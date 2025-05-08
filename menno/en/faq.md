---
layout: custom
title: ❓Frequently Asked Questions (FAQ)
parent: Menno
nav_order: 7
permalink: /menno/faq/
lang: en
---

# Menno Avatar - Frequently Asked Questions (FAQ)

This page answers common questions and issues related to the Menno avatar.

## Contents

1. [EyePointer not working properly](#eyepointer-issues)
2. [Issues with specific outfits](#outfit-issues)

## EyePointer Issues

### Symptoms
[Siromori Eye Pointer](https://booth.pm/ja/items/4742883) doesn't move the eyes or doesn't function correctly for eye tracking.

### Cause
The Menno avatar has an `UpperChest` bone in its hierarchy, which isn't compatible with the standard EyePointer animations.

### Solutions

#### If you have M Avatar Setting v1.2.8 or later

1. Download [Menno_v1.01_M.AvatarSetting_v1.2.8.zip](https://emudotto.booth.pm/items/6504220)
2. **Important**: When importing, only check the Scripts folder (importing other folders may overwrite Menno's textures and materials)
3. Open M Avatar Setting from Unity's top menu: `Window > M Avatar Setting`
4. Expand the Debug section at the bottom of the window and click the "fixEyePointer" button
5. This will apply EyePointer animations compatible with Menno's UpperChest bone structure

#### Manual Fix

You can manually modify the animation paths:

1. Locate these animation files:
   - Assets/Siromori/EyePointer/Animations/Toggle_Off.anim
   - Assets/Siromori/EyePointer/Animations/Toggle_On.anim
   - Assets/Siromori/EyePointer/Animations/Toggle_On_NoLook.anim
2. Modify the eye bone paths from `Armature/Hips/Spine/Chest/Neck/Head/LeftEye` to
   `Armature/Hips/Spine/Chest/UpperChest/Neck/Head/LeftEye` (and similar for other paths)

## Outfit Issues

### Symptoms
When wearing certain outfits, the avatar may not return to normal posture after crouching with the Z button, or may exhibit other strange behaviors.

### Affected Outfits
- "[Arcane Attire](https://booth.pm/ja/items/6151859)" by Pirouette: A wizard-themed outfit set
- "[Theologica](https://booth.pm/ja/items/6350299)" by ISHTAR LIBERALIS: A nun-themed outfit set

### Cause
These outfits have collider objects with Shape Type set to Plane directly under the Armature, with their X-axis rotation set to 90 degrees, which causes issues with the avatar's movement.

### Solutions

#### For "Arcane Attire"
1. Follow the instructions in the "plusheadのルェルツ_Rwerutu_に着せる方へ.png" image included in the BOOTH download page for Arcane Attire
2. Specifically, change the collider object's X-axis rotation from 90 degrees to 0 degrees

#### For "Theologica"
Similarly, check the collider object of the outfit and change its X-axis rotation from 90 degrees to 0 degrees to resolve the issue.

## Other Questions

If you have any other questions or issues, please contact us via [X(Twitter)](https://x.com/_emudotto). 