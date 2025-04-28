---
layout: default
title: Animation Structure
parent: Menno
nav_order: 4
permalink: /menno/animation/
lang: en
---

# Menno - Animation Structure

## Animation Folder Structure

The animation-related files for Menno are organized in the following folders:

```
Assets/emudotto/Menno/Animation/
├── AnimaitonLayer/ - Animation controllers
├── FX_Body/ - Body animations
├── FX_Face/ - Facial expressions
├── FX_ToggleProp/ - Toggle item animations
├── Gesture/ - Gesture animations
├── Locomotion/ - Movement animations
├── ModularAvatar/ - ModularAvatar extensions
└── Parameters/ - VRChat SDK menu and parameter settings
```

## Animation Controllers

### Menno_Layer_FX.controller

The main animation controller for the Menno avatar is `AnimaitonLayer/Menno_Layer_FX.controller`. This controller manages expressions, body lighting, toggle items, and more.

The main structure of the FX controller is as follows:

```
Menno_Layer_FX.controller
├── Expression state machine
│   ├── Base
│   ├── Smile
│   ├── Sad
│   └── Other expressions...
├── Body lighting state machine
│   ├── Lighting_OFF
│   └── Lighting_ON
└── Toggle item state machine
    ├── Pan_OFF / Pan_ON
    ├── Xondle_OFF / Xondle_ON
    └── Mokia_OFF / Mokia_ON
```

### Menno_Layer_Gesture.controller

`AnimaitonLayer/Menno_Layer_Gesture.controller` controls hand gestures.

### Menno_Props.controller & Menno_Props_Gesture.controller

These controllers manage toggle operations for items and related gestures.
They are integrated with the FX layer after upload via Modular Avatar.

## Facial Expressions (FX_Face)

The default Menno avatar includes the following facial expressions:

| Animation Name | Description |
|--------------|------|
| Menno_Base | Default state |
| Menno_Smile | Smiling expression |
| Menno_Sad | Sad expression |
| Menno_Angry | Angry expression |
| Menno_Surprise | Surprised expression |
| Menno_Cry | Crying expression |
| Menno_Heart | Eyes in heart shape |
| Menno_Tongue | Sticking out tongue |
| Menno_Calm | Relaxed expression |
| Menno_Sleep | Closed eyes |
| Menno_Cold | Cold expression |
| Menno_Impatience | Impatient expression |

Many other expressions are available and can be selected from the Expression Menu.

## Body Animations (FX_Body)

Body animations include:

- **Menno_Body_Lighting** - Body lighting adjustment
- **Menno_Body_Cheek** - Cheeks that can be pulled using PhysBones
- **Menno_Body_Cheek_L** - Left cheek that can be pulled using PhysBones
- **Menno_Body_Cheek_R** - Right cheek that can be pulled using PhysBones

## Parameter Settings (Parameters)

The Menno avatar uses the following Expression Menus and Parameters:

- **Menno_ExpressionParameters.asset** - Basic parameter settings
- **Menno_ExpressionsMenu.asset** - Main menu
- **Menno_FaceMenu.asset** - Expression menu
- **Menno_FaceMenu1.asset**, **Menno_FaceMenu2.asset**, **Menno_FaceMenu3.asset** - Additional expression menus
- **Menno_Props.asset**, **Menno_Props_SubMenu.asset** - Item menus

### Main Parameter List

| Parameter Name | Type | Description |
|--------------|------|------|
| VRCFaceBlendH | Float | Horizontal expression blend (VRChat standard) |
| VRCFaceBlendV | Float | Vertical expression blend (VRChat standard) |
| GestureLeft | Int | Left hand gesture (VRChat standard) |
| GestureRight | Int | Right hand gesture (VRChat standard) |
| GestureLeftWeight | Float | Left hand gesture strength (VRChat standard) |
| GestureRightWeight | Float | Right hand gesture strength (VRChat standard) |
| FacialExpression | Int | Expression selection |
| BodyLighting | Float | Body lighting adjustment |
| Cheek | Bool | Cheek pull ON/OFF |
| CheekLeft | Bool | Left cheek pull ON/OFF |
| CheekRight | Bool | Right cheek pull ON/OFF |
| TogglePan | Bool | Frying pan display/hide |
| ToggleXondle | Bool | Xondle/Xontra display/hide |
| ToggleMokia | Bool | Mobile phone display/hide |

## How to Use Expressions

The expressions for the Menno avatar can be used in the following ways:

### 1. Selection from the Action Menu

Open the VRChat action menu (R key on PC, Action Menu button in VR) and select expressions from the Menno expression menu.

The expression menu is hierarchically organized as follows:

```
Main Menu
├── Expressions
│   ├── Basic Expressions
│   │   ├── Smile
│   │   ├── Sad
│   │   └── ...
│   ├── Special Expressions
│   │   ├── Heart Eyes
│   │   ├── Flaming Eyes
│   │   └── ...
│   └── Emotional Expressions
│       ├── Impatience
│       ├── Cold
│       └── ...
└── Items
    ├── Frying Pan
    ├── Xondle
    └── Mokia
``` 