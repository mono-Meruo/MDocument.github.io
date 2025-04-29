---
layout: custom
title: Shape Keys List
parent: Menno
nav_order: 7
permalink: /menno/shapekeys/
lang: en
---

# Shape Keys List and Description

Shape keys are functions that transform the shape of a 3D model. The Menno model has a total of 884 shape keys implemented, allowing for detailed adjustments to the character's facial expressions and body shape.

## Shape Keys Overview

### Facial Shape Keys (Total 697 functional shape keys, excluding empty and divider shape keys)

| Category | Count | Description |
|---------|------|-------------|
| VRC | 18 | VRChat shape keys (v_aa, v_ch, v_dd, etc. for voice recognition and gaze control) |
| MMD | 47 | MikuMikuDance compatible expressions (a-i-u-e-o, smile, wink, etc.) |
| Perfect-Sync | 52 | Experimental shape keys for expression synchronization |
| EYE | 51 | Eye expression control (closing, smiling, raised, lowered, half-closed, etc.) |
| EYE_EX | 3 | Eye shader effects (Shader_ON, Shader_Big, Grabpass_ON, etc.) |
| EYE_Action | 7 | Eye special effects (tears, hearts, spinning, shock, stars, etc.) |
| EYE_Option | 67 | Detailed eye adjustments (light, dark circles, position, size, spacing, etc.) |
| PUPIL_Option | 35 | Pupil adjustments (white pupils, convergence, divergence, size, forward/backward movement, etc.) |
| IRIS_Option | 18 | Sclera adjustments (blur, size, forward/backward movement, etc.) |
| EYELID_Option | 74 | Eyelid adjustments (ends, starts, detailed up/down/left/right movements, etc.) |
| EYELASH | 12 | Eyelash expressions (thin eyes, sleepy eyes, soft eyes, etc.) |
| EYELASH_Option | 48 | Eyelash adjustments (thickness, length, position of upper/lower lashes, etc.) |
| EYEBROW | 48 | Eyebrow expressions (raising/lowering, smiling, angry, worried, movement by specific areas, etc.) |
| EYEBROW_Option | 10 | Eyebrow adjustments (thickness, shape, position, etc.) |
| MOUTH | 53 | Mouth expressions (a-i-u-e-o, smile, grin, triangle, ω, various shapes) |
| MOUTH_Option | 8 | Mouth adjustments (fangs, forward/backward position, cheeks, etc.) |
| TONGUE | 12 | Tongue expressions (sticking out, bending, forward/backward/up/down movement, etc.) |
| TONGUE_Option | 6 | Tongue adjustments (thin, thick, flat, length, etc.) |
| TEETH_Option | 15 | Teeth adjustments (fangs, jagged, upper/lower position, etc.) |
| FACE | 6 | Full face effects (blush, shock, wrinkles, etc.) |
| NOSE_Option | 7 | Nose adjustments (up/down/left/right, forward/backward position, etc.) |
| EAR_Option | 6 | Ear adjustments (elf ears, size, etc.) |
| JAW_Option | 14 | Jaw adjustments (roundness, jaw shape, length, sharpness, etc.) |
| SHRINK_Option | 2 | Face part shrinking (neck, ears) |
| Empty for Updates | 183 | Reserved shape keys for updates |
| Divider Shape Keys | 16 | Section dividers |

Each category includes shape keys not only for both eyes but also for the left eye (_L) and right eye (_R), allowing for asymmetrical expressions.

### Body Shape Keys (30)

Mainly used for shrinking various body parts. Neck, shoulders, arms, hands, fingers, chest, back, waist, legs, feet, etc., can all have their reduction rate adjusted individually.

### Hair Shape Keys (Total 50)

The Hair_Bangs object includes the following functional shape keys (excluding Empty shape keys):

#### BANGS_Option (Front Bangs) - 31
- Basic Styles:
  - BANGS_OP_短く_Short: Shortens the bangs
  - BANGS_OP_長く_Long: Lengthens the bangs
  - BANGS_OP_ずらす_Shift: Shifts the bangs sideways
  - BANGS_OP_ねぐせ_Bedhair: Creates a bed hair style
  - BANGS_OP_ぱっつん_Straight: Creates straight-cut bangs
  - BANGS_OP_ぱっつん短い_StraightShort: Creates short straight-cut bangs
  - BANGS_OP_ぱっつん長め_StraightLong: Creates long straight-cut bangs
- Individual Adjustments:
  - BANGS_OP_01_Long to BANGS_OP_12_Long: Shape keys that adjust individual strands of the bangs one by one. Each number corresponds to a specific strand of the bangs, allowing them to be moved or shaped independently.
  - BANGS_OP_01_Short to BANGS_OP_12_Short: Shape keys that adjust individual strands of the bangs one by one. Each number corresponds to a specific strand of the bangs, allowing them to be moved or shaped independently.

#### FRONT_Option (Front Hair) - 5
- Individual Adjustments:
  - FRONT_OP_01_Long: Shape key for adjusting a specific strand of front hair individually.
  - FRONT_OP_02_Long: Shape key for adjusting another strand of front hair individually.
  - FRONT_OP_01_Short: Shape key for adjusting a specific strand of front hair individually.
  - FRONT_OP_02_Short: Shape key for adjusting another strand of front hair individually.
  - FRONT_OP_Empty: Empty adjustment item

#### SIDES_Option (Side Hair) - 14
- Basic Styles:
  - SIDES_OP_短く_Short: Shortens the side hair
  - SIDES_OP_長く_Long: Lengthens the side hair
  - SIDES_OP_ぱっつん_Straight: Creates straight-cut side hair
- Individual Adjustments:
  - SIDES_OP_01_Long to SIDES_OP_05_Long: Shape keys that adjust individual strands of the side hair one by one. Each number corresponds to a specific strand of side hair, allowing them to be moved or shaped independently.
  - SIDES_OP_01_Short to SIDES_OP_05_Short: Shape keys that adjust individual strands of the side hair one by one. Each number corresponds to a specific strand of side hair, allowing them to be moved or shaped independently.
  - SIDES_OP_Empty: Empty adjustment item

By using these numbered shape keys (01, 02, etc.), you can freely adjust specific strands of hair one by one, rather than the entire hairstyle. For example, you can move only a specific strand on the left side of the bangs, or change the shape of only a specific strand of the side hair. This allows you to customize the details of the hairstyle to your liking.

## About Empty Shape Keys

When updating in Unity, inserting new shape keys can shift the order of existing shape keys, causing inconsistencies with previously set values. To prevent this, many empty shape keys (Empty) are placed in advance. During updates, these Empty shape keys are used to add new features.

## About Perfect-Sync Shape Keys (Experimental)

Perfect-Sync is an experimental set of shape keys designed for more natural expression synchronization. It enables fine control over various facial movements:

- Eyebrow movements (inner up, outer up, down, etc.)
- Eye movements (up/down/left/right, blinking, squinting, etc.)
- Cheek movements (puffing, tightening, etc.)
- Nose movements (wrinkles, etc.)
- Jaw movements (opening/closing, forward/backward/left/right, etc.)
- Mouth movements (various shapes and expressions)

These shape keys are in the experimental stage and may be subject to changes in future updates.

## How to Use Shape Keys

1. Select the model in the Unity Inspector
2. Select the SkinnedMeshRenderer component
3. Adjust each shape key slider in the "Blend Shapes" section
4. Set values between 0 and 100 (0 = no effect, 100 = maximum effect)

By combining shape keys, you can create your own expressions and body shapes.

## Notes on Shape Key Adjustments

### Impact on Animations

Making significant changes to parts related to expressions, such as eyes and mouth, may cause default expression animations to not work properly. This is because the animations are created based on the original shape.

For example:
- Greatly changing the size or position of the eyes can make blinking animations unnatural
- Changing the shape of the mouth can cause speech animations to become misaligned
- Changing the proportions of the face can disrupt the entire expression animation

In such cases, it is necessary to adjust the animation clips to match the new shape.

### Flexible Use of Shape Keys

In the Menno model, you can use expression shape keys (EYE, MOUTH, EYEBROW, etc.) for body shape adjustments, or conversely, use detailed adjustment shape keys (_Option categories) for expressions.

For example:
- Combine EYE_Option shape keys to create your own eye expressions
- Use MOUTH_Option to create special mouth shapes as expressions
- Incorporate JAW_Option, normally used for adjustments, into expression animations

### How to Adjust Expression Animations

If you have significantly changed shape keys, you will need to adjust the expression animations as well. You can adjust them in the Menno model using the following steps:

1. Set the Menno_Layer_FX.controller in the Animator component
   - Select the root object of the Menno avatar
   - Add "Menno_Layer_FX.controller" to the Animator component
   - This controller includes default settings for expression animations

2. Adjust default expressions in the Animation window
   - Open the Animation window from Unity's "Window" → "Animation" → "Animation"
   - Select the Menno avatar in the scene
   - Select the existing expression animation displayed in the Animation window
   - Change the keyframes corresponding to the adjusted shape keys
     - Click on keyframes to edit values

3. Test the adjusted expressions
   - Check the movement of expressions using VRChat Gesture Manager, etc.
   - Make fine adjustments as needed

With this method, you can properly adjust existing expression animations to match your customized shape key settings. 