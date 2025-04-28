---
layout: default
title: 애니메이션 구조
parent: Menno
nav_order: 4
permalink: /menno/animation/
lang: ko
---

# Menno - 애니메이션 구조

## 애니메이션 폴더 구조

Menno의 애니메이션 관련 파일은 다음 폴더에 정리되어 있습니다:

```
Assets/emudotto/Menno/Animation/
├── AnimaitonLayer/ - 애니메이션 컨트롤러
├── FX_Body/ - 신체 애니메이션
├── FX_Face/ - 표정 애니메이션
├── FX_ToggleProp/ - 토글 아이템 애니메이션
├── Gesture/ - 제스처 애니메이션
├── Locomotion/ - 이동 애니메이션
├── ModularAvatar/ - ModularAvatar 확장
└── Parameters/ - VRChatSDK 메뉴 및 파라미터 설정
```

## 애니메이션 컨트롤러

### Menno_Layer_FX.controller

Menno 아바타의 메인 애니메이션 컨트롤러는 `AnimaitonLayer/Menno_Layer_FX.controller`입니다. 이 컨트롤러는 표정, 바디 라이팅, 토글 아이템 등을 관리합니다.

FX 컨트롤러의 주요 구조는 다음과 같습니다:

```
Menno_Layer_FX.controller
├── 표정 스테이트 머신
│   ├── 기본 상태_Base
│   ├── 미소_Smile
│   ├── 슬픔_Sad
│   └── 기타 표정...
├── 바디 라이팅 스테이트 머신
│   ├── 라이팅_OFF
│   └── 라이팅_ON
└── 토글 아이템 스테이트 머신
    ├── Pan_OFF / Pan_ON
    ├── Xondle_OFF / Xondle_ON
    └── Mokia_OFF / Mokia_ON
```

### Menno_Layer_Gesture.controller

`AnimaitonLayer/Menno_Layer_Gesture.controller`는 손 제스처를 제어합니다.

### Menno_Props.controller & Menno_Props_Gesture.controller

이 컨트롤러들은 아이템 토글 조작과 관련 제스처를 제어합니다.
Modular Avatar를 통해 업로드 후 FX 레이어와 통합됩니다.

## 표정 애니메이션 (FX_Face)

기본 Menno 아바타는 다음과 같은 표정 애니메이션을 가지고 있습니다:

| 애니메이션 이름 | 설명 |
|--------------|------|
| Menno_기본 상태_Base | 기본 상태 |
| Menno_미소_Smile | 미소 표정 |
| Menno_슬픔_Sad | 슬픈 표정 |
| Menno_분노_Angry | 화난 표정 |
| Menno_놀람_surprise | 놀란 표정 |
| Menno_울음_Cry | 우는 표정 |
| Menno_하트_Heart | 눈이 하트 모양이 되는 표정 |
| Menno_혀 내밀기_Tongue | 혀를 내미는 표정 |
| Menno_평온함_Calm | 릴렉스한 표정 |
| Menno_눈 감기_Sleep | 눈을 감은 표정 |
| Menno_추위_Cold | 추운 듯한 표정 |
| Menno_조급함_Impatience | 조급한 표정 |

이 외에도 다양한 표정이 준비되어 있으며, Expression Menu에서 선택할 수 있습니다.

## 신체 애니메이션 (FX_Body)

신체 애니메이션에는 다음과 같은 것이 있습니다:

- **Menno_Body_Lighting** - 신체 라이팅 조정
- **Menno_Body_Cheek** - PhysBone에 의해 볼이 당겨집니다
- **Menno_Body_Cheek_L** - PhysBone에 의해 왼쪽 볼이 당겨집니다
- **Menno_Body_Cheek_R** - PhysBone에 의해 오른쪽 볼이 당겨집니다

## 파라미터 설정 (Parameters)

Menno 아바타에서는 다음과 같은 Expression Menu와 Parameters가 사용됩니다:

- **Menno_ExpressionParameters.asset** - 기본 파라미터 설정
- **Menno_ExpressionsMenu.asset** - 메인 메뉴
- **Menno_FaceMenu.asset** - 표정 메뉴
- **Menno_FaceMenu1.asset**, **Menno_FaceMenu2.asset**, **Menno_FaceMenu3.asset** - 추가 표정 메뉴
- **Menno_Props.asset**, **Menno_Props_SubMenu.asset** - 아이템 메뉴

### 주요 파라미터 목록

| 파라미터 이름 | 타입 | 설명 |
|--------------|------|------|
| VRCFaceBlendH | Float | 수평 방향 표정 블렌드(VRChat 표준) |
| VRCFaceBlendV | Float | 수직 방향 표정 블렌드(VRChat 표준) |
| GestureLeft | Int | 왼손 제스처(VRChat 표준) |
| GestureRight | Int | 오른손 제스처(VRChat 표준) |
| GestureLeftWeight | Float | 왼손 제스처의 강도(VRChat 표준) |
| GestureRightWeight | Float | 오른손 제스처의 강도(VRChat 표준) |
| FacialExpression | Int | 표정 선택 |
| BodyLighting | Float | 신체 라이팅 조정 |
| Cheek | Bool | 볼 당기기 ON/OFF |
| CheekLeft | Bool | 왼쪽 볼 당기기 ON/OFF |
| CheekRight | Bool | 오른쪽 볼 당기기 ON/OFF |
| TogglePan | Bool | 프라이팬 표시/숨김 |
| ToggleXondle | Bool | Xondle/Xontra 표시/숨김 |
| ToggleMokia | Bool | 휴대전화 표시/숨김 |

## 표정 사용 방법

Menno 아바타의 표정은 다음 방법으로 사용할 수 있습니다:

### 1. 액션 메뉴에서 선택

VRChat의 액션 메뉴(PC에서는 R키, VR에서는 액션 메뉴 버튼)를 열고, Menno의 표정 메뉴에서 표정을 선택합니다.

표정 메뉴는 다음과 같이 계층화되어 있습니다:

```
메인 메뉴
├── 표정
│   ├── 기본 표정
│   │   ├── 미소
│   │   ├── 슬픔
│   │   └── ...
│   ├── 특수 표정
│   │   ├── 하트 눈
│   │   ├── 불타는 눈
│   │   └── ...
│   └── 감정 표현
│       ├── 조급함
│       ├── 추위
│       └── ...
└── 아이템
    ├── 프라이팬
    ├── 캔들
    └── 휴대전화
``` 