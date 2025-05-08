---
layout: custom
title: ❓자주 묻는 질문(FAQ)
parent: Menno
nav_order: 7
permalink: /menno/faq/
lang: ko
---

# Menno 아바타 - 자주 묻는 질문(FAQ)

이 페이지에서는 Menno 아바타에 관한 자주 묻는 질문과 해결 방법을 정리했습니다.

## 목차

1. [EyePointer가 제대로 작동하지 않음](#eyepointer-문제)
2. [특정 의상에서 자세가 이상해지는 문제](#의상-문제)

## EyePointer 문제

### 증상
[Siromori Eye Pointer](https://booth.pm/ja/items/4742883)를 도입해도 눈이 움직이지 않거나 시선 유도가 정상적으로 작동하지 않습니다.

### 원인
Menno 아바타는 `UpperChest` 본을 가지고 있어 표준 EyePointer 애니메이션이 이 본 구조에 대응하지 않습니다.

### 해결 방법

#### M Avatar Setting v1.2.8 이상을 사용하는 경우

1. [Menno_v1.01_M.AvatarSetting_v1.2.8.zip](https://emudotto.booth.pm/items/6504220)을 다운로드합니다
2. **중요**: 임포트 시 Scripts 폴더만 체크하세요(다른 폴더를 임포트하면 Menno의 텍스처나 머티리얼이 덮어쓰여질 수 있습니다)
3. Unity 에디터 상단 메뉴에서 `Window > M Avatar Setting`을 엽니다
4. 창 맨 아래에 있는 디버그 섹션을 펼치고 "fixEyePointer" 버튼을 클릭합니다
5. 이렇게 하면 Menno 아바타의 UpperChest 본 구조에 대응하는 EyePointer 애니메이션이 적용됩니다

#### 수동으로 수정하는 경우

EyePointer의 애니메이션 경로를 수동으로 수정해야 합니다:

1. 다음 애니메이션 파일을 찾습니다:
   - Assets/Siromori/EyePointer/Animations/Toggle_Off.anim
   - Assets/Siromori/EyePointer/Animations/Toggle_On.anim
   - Assets/Siromori/EyePointer/Animations/Toggle_On_NoLook.anim
2. 이 파일들에 있는 눈의 본 경로(`Armature/Hips/Spine/Chest/Neck/Head/LeftEye` 등)를
   `Armature/Hips/Spine/Chest/UpperChest/Neck/Head/LeftEye`와 같이 수정합니다

## 의상 문제

### 증상
특정 의상을 착용하면 Z 버튼으로 쪼그려 앉은 후에 자세가 원래대로 돌아오지 않거나 동작이 이상해집니다.

### 영향을 받는 의상 예시
- Pirouette의 "[Arcane Attire](https://booth.pm/ja/items/6151859)": 마법사 스타일의 의상 세트
- ISHTAR LIBERALIS의 "[Theologica](https://booth.pm/ja/items/6350299)": 수녀 스타일의 의상 세트

### 원인
이러한 의상들은 Armature 바로 아래에 Shape Type이 Plane인 콜라이더 오브젝트가 배치되어 있으며, 그 오브젝트의 X축 회전이 90도로 설정되어 있어 문제를 일으킵니다.

### 해결 방법

#### "Arcane Attire"의 경우
1. BOOTH의 Arcane Attire 다운로드 페이지에 포함된 "plusheadのルェルツ_Rwerutu_に着せる方へ.png" 지침을 따르세요
2. 구체적으로는 콜라이더 오브젝트의 X축 회전을 90도에서 0도로 변경합니다

#### "Theologica"의 경우
마찬가지로 의상의 콜라이더 오브젝트의 X축 회전을 확인하고 90도에서 0도로 변경하면 문제가 해결됩니다.

## 기타 질문

질문이나 문제가 있으면 [X(Twitter)](https://x.com/_emudotto)로 연락해 주세요. 