---
layout: custom
title: 구조 설명
parent: Menno
nav_order: 3
permalink: /menno/structure/
lang: ko
---

# Menno - 구조 설명

이 페이지에서는 Menno 아바타의 폴더 구조와 파일 구성에 대해 설명합니다.

## 폴더 구조

Menno 아바타 파일은 다음과 같은 폴더 구조로 구성되어 있습니다:

```
Assets/emudotto/Menno/
├── Animation/            # 애니메이션 파일
│   ├── ModularAvatar/    # ModularAvatar용 오브젝트
│   │   └── Costume/      # M. Avatar Setting에서 사용하는 의상 전환용 토글
│   └── Controllers/      # 애니메이션 컨트롤러
├── FBX/                  # 3D 모델 파일
├── Materials/            # 머티리얼 파일
│   ├── Presets/          # 머리 색상 등의 프리셋
│   └── Tex_Main/         # 텍스처 파일
├── Materials_Props/      # 아이템 머티리얼 파일
│   └── Tex_Props/        # 텍스처 파일
├── Prefab/               # 프리팹 파일
│   └── ToggleProps.prefab # 아이템용 프리팹
├── Menno.prefab          # Menno 아바타의 메인 프리팹
└── MennoScene.unity      # 씬
```

## 주요 파일 설명

### Menno.prefab

Menno 아바타의 메인 프리팹 파일입니다. 이 파일을 씬에 드래그 앤 드롭하여 아바타를 사용할 수 있습니다. 다음과 같은 주요 컴포넌트가 포함되어 있습니다:

- VRC Avatar Descriptor - VRChat 아바타 설정
- M Avatar Setup Helper - M. Avatar Setting과의 연동
- Animator - 애니메이션 제어
- Modular Avatar 컴포넌트 그룹 - 아바타 커스터마이징

### 아바타 계층 구조

Menno 프리팹의 계층 구조는 다음과 같습니다:

```
Menno (루트 오브젝트)
├── Armature          # 아바타 본
├── Body              # 바디 메시
├── Hair              # 머리카락 메시
├── Hair_Bangs        # 앞머리 메시
├── Belt              # 벨트 메시
├── Boots             # 부츠 메시
├── Coat              # 코트 메시
├── Jacket            # 재킷 메시
├── Karada            # 바디 디테일 메시
├── Pants             # 바지 메시
├── Shirt             # 셔츠 메시
├── Tie               # 넥타이 메시
├── AutoAnchorObject  # 앵커 포인트
├── MTear             # 눈물 이펙트
├── Costume           # 의상 전환용 오브젝트
└── ToggleProps       # 토글 아이템용 오브젝트
```

## 커스터마이징 시 주의사항

- 머티리얼이나 텍스처를 변경할 때는 원본 파일의 백업을 만드는 것이 좋습니다 