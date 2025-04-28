---
layout: custom
title: ⚙️아이템 설정
parent: ⚙️M. Avatar Setting 설정
grand_parent: Menno
nav_order: 3
permalink: /menno/mas-settings/items/
lang: ko
---

# Menno - 아이템 설정

M. Avatar Setting을 사용하면 Menno 아바타의 의상, 액세서리 및 기타 아이템을 구성할 수 있습니다.

![아이템 설정 UI]({{ site.baseurl }}/assets/images/item_settings.png)

## 의상 설정

Menno 아바타에서는 여러 의상을 전환하여 사용할 수 있습니다.

### 의상 선택

1. M. Avatar Setting 창을 엽니다
2. Menno 아바타를 선택합니다
3. "의상 설정" 섹션을 확장합니다
4. 사용하려는 의상 옆에 있는 체크박스를 선택합니다

### 의상의 초기 상태

각 의상에는 "초기 상태" 설정이 있습니다. 이를 활성화하면 아바타가 로드될 때 해당 의상이 표시됩니다. 여러 의상의 초기 상태를 활성화할 수 있습니다.

### 의상 색상 변경

의상 색상을 변경하는 버튼도 제공됩니다:

* **표준 색상** - 기본 의상 색상
* **흰색** - 흰색 버전의 의상

버튼을 클릭하면 모든 의상의 색상이 변경됩니다.

## 토글 아이템 설정

Menno 아바타에는 VRChat에서 전환 가능한 특별한 아이템(토글 프롭)이 포함되어 있습니다.

### 사용 가능한 토글 아이템

* **Pan** - 프라이팬
* **Xondle** - 존들
* **Mokia** - 휴대폰

### 토글 아이템 설정

각 토글 아이템에는 다음 설정이 있습니다:

1. **활성화/비활성화** - 아이템을 사용할지 여부
2. **사운드 이펙트** - 아이템을 전환할 때 사운드 이펙트를 재생할지 여부
3. **초기 상태** - 아바타 로드 시 아이템을 표시할지 여부

## 설정 초기화

모든 의상 및 토글 아이템 설정을 초기 상태로 되돌리려면 "초기화" 버튼을 클릭합니다. 확인 대화 상자가 표시되고 "예"를 선택하면 설정이 초기화됩니다.

## 기술적 세부 사항

* 의상 프리팹은 `Assets/emudotto/Menno/Animation/ModularAvatar/Costume`에서 로드됩니다
* 토글 프롭 프리팹은 `Assets/emudotto/Menno/Prefab/ToggleProps.prefab`에서 로드됩니다
* 의상 머티리얼은 `Assets/emudotto/Menno/Materials/Menno_Wear.mat`에서 관리됩니다

## 언어 설정

M. Avatar Setting의 오른쪽 상단에 있는 언어 전환 버튼으로 일본어/영어를 전환할 수 있습니다. 아이템 이름과 설명도 그에 따라 전환됩니다. 