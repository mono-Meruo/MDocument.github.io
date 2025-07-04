---
layout: custom
title: 🎭얼굴 블렌드 셰이프 프리셋 (빠른 시작)
parent: ⚙️얼굴 설정
grand_parent: ⚙️M. Avatar Setting
great_grand_parent: Menno
nav_order: 2
permalink: /menno/mas-settings/face/preset-quickstart/
lang: ko

---

# 얼굴 셰이프 키 프리셋 기능 - 빠른 시작

M. Avatar Setting의 블렌드 셰이프 프리셋 기능을 사용하면 좋아하는 블렌드 셰이프를 저장하고 언제든지 쉽게 불러올 수 있습니다.

![프리셋 기능 UI]({{ site.baseurl }}/assets/images/preset_ui.png)

## 프리셋 저장 방법

### 1. 블렌드 셰이프 조정
먼저 얼굴 설정에서 좋아하는 블렌드 셰이프를 만듭니다.

### 2. 프리셋 이름 입력
"셰이프 키 프리셋" 섹션에서 프리셋 이름을 입력합니다.
- 기본적으로 `Menno_Face_Preset_01` 같은 이름이 자동으로 입력됩니다
- 알기 쉬운 이름으로 변경할 수 있습니다 (예: "아이", "어른", "동안" 등)

### 3. 저장 버튼 클릭
"저장" 버튼을 클릭하면 현재 블렌드 셰이프 설정이 프리셋으로 저장됩니다.

## 프리셋 사용 방법

### 1. 저장된 프리셋에서 선택
저장된 프리셋이 "저장된 프리셋" 섹션에 표시됩니다.

### 2. 강도 슬라이더로 적용
각 프리셋에는 "강도" 슬라이더가 있습니다:
- **0%**: 프리셋을 적용하지 않음
- **50%**: 프리셋을 절반 강도로 적용
- **100%**: 프리셋을 완전히 적용
![assets]({{ site.baseurl }}/assets/images/preset_assets_slider2.gif)

### 3. 실시간 미리보기
슬라이더를 움직이면 실시간으로 블렌드 쉐이프가 변경됩니다.

## 편리한 기능

### 프리셋 합성
여러 프리셋을 동시에 적용하여 새로운 블렌드 쉐이프를 만들 수 있습니다.
- 예: "어린이"를 50%, "어른"을 30% 적용하여 원하는 블렌드 쉐이프를 설정합니다.
![assets]({{ site.baseurl }}/assets/images/preset_assets_slider.gif)

### 프리셋 폴더에 접근
"저장된 프리셋:" 옆의 📁 버튼을 클릭하면 프리셋이 저장된 폴더가 프로젝트 창에서 열립니다.

### 프리셋 삭제
각 프리셋의 "X" 버튼을 클릭하면 확인 후 프리셋을 삭제할 수 있습니다.

## 주의사항

- 프리셋은 프로젝트별로 저장됩니다
- Unity를 재시작해도 프리셋은 유지됩니다
- 프리셋 파일은 `Assets/emudotto/Menno/Resources/Face_Presets`에 저장됩니다 