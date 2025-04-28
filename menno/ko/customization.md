---
layout: custom
title: 커스터마이징
parent: Menno
nav_order: 2
permalink: /menno/customization/
lang: ko
---

# Menno - 커스터마이징

이 페이지에서는 Menno 아바타의 커스터마이징 방법에 대해 설명합니다.

## 텍스처 커스터마이징

### 1. 텍스처 파일 위치

Menno의 주요 텍스처 파일은 다음 위치에 저장되어 있습니다:

```
Assets/emudotto/Menno/Materials/Tex_Main/
```

### 2. 텍스처 편집

1. 텍스처 파일(PSD)을 Photoshop, Gimp 또는 기타 이미지 편집 소프트웨어에서 엽니다
2. 필요한 편집을 하고 저장합니다
3. Unity 프로젝트로 돌아가면 변경 사항이 자동으로 적용됩니다


## 머티리얼 커스터마이징

### 1. 머티리얼 위치

Menno의 머티리얼은 다음 위치에 저장되어 있습니다:

```
Assets/emudotto/Menno/Materials/
```

### 2. 머티리얼 편집

1. 프로젝트 창에서 또는 계층 구조에서 오브젝트를 선택하여 머티리얼 파일을 선택합니다
2. 인스펙터 창에서 [liltoon 머티리얼 파라미터를 조정](https://lilxyzw.github.io/lilToon/en_us/first.html)합니다


## 의상 추가

### 1. 새 의상 생성

1. 의상을 생성하거나 구매합니다
2. Unity 패키지를 클릭하여 Unity로 임포트합니다

### 2. ModularAvatar를 사용한 의상 추가

ModularAvatar를 사용하면 Menno 아바타에 새 의상을 쉽게 추가할 수 있습니다.

#### 2.1 간단한 의상 설정

1. 새 의상 모델을 Menno의 자식 오브젝트로 배치합니다
2. 의상 오브젝트를 우클릭하고 `[ModularAvatar] Setup Outfit`을 선택합니다
   - Modular Avatar가 자동으로 의상의 아마추어를 감지하고 Merge Armature 컴포넌트를 추가합니다
3. 이제 의상이 Menno 아바타의 본에 자동으로 따라갑니다

#### 2.2 의상 토글 설정

Expression Menu에서 의상을 전환할 수 있도록 하려면:

1. 의상 오브젝트를 선택합니다
2. Add Component에서 MA Toggle Object 컴포넌트를 추가합니다
3. "기본 상태"를 설정합니다(켜기 또는 끄기)
4. "메뉴 항목 이름"에 표시하고 싶은 이름을 입력합니다
5. 필요에 따라 아이콘과 메뉴 계층 구조를 설정합니다

이러한 설정이 완료되면 새 의상이 Menno 아바타에 적절하게 추가되고 Expression Menu에서 전환할 수 있게 됩니다.

## 애니메이션 변경

### 1. 애니메이션 파일 위치

Menno의 애니메이션 파일은 다음 위치에 저장되어 있습니다:

```
Assets/emudotto/Menno/Animation/
```

### 2. 애니메이션 편집

1. 프로젝트 창에서 애니메이션 파일을 선택합니다
2. Animation Window를 엽니다
3. 키프레임을 추가하거나 편집합니다
4. 변경 사항을 저장합니다

## 표정 추가

### 1. 블렌드 쉐이프 사용

1. 씬에서 Menno 아바타를 선택합니다
2. Body 메시의 스킨드 메시 렌더러를 선택합니다
3. 인스펙터의 Blend Shapes 섹션에서 표정을 조정합니다
4. Animation 창에서 조정된 표정을 키프레임으로 기록합니다

## 주의 사항

* 큰 변경을 할 때는 원본 파일의 백업을 만드는 것이 좋습니다 