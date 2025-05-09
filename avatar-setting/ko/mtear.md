---
layout: custom
title: MTear 눈물 편집기
parent: ⚙️M. Avatar Setting
nav_order: 3
lang: ko
permalink: /avatar-setting/mtear/
---

<div style="text-align: right; margin-bottom: 20px;">
  <a href="../mtear.html" style="margin-right: 5px;">日本語</a>
  <a href="../en/mtear.html" style="margin-right: 5px;">English</a>
  <a href="../zh/mtear.html">中文</a>
</div>

# MTear 눈물 편집기

MTear는 VRChat 아바타 "Menno"용 눈물 효과를 편집하기 위한 도구입니다. 눈물이 흐르는 속도, 형태, 크기 등을 자유롭게 커스터마이징할 수 있습니다.

- [개요](#개요)
- [사용 방법](#사용-방법)
- [눈물 메시 편집기](#눈물-메시-편집기)
- [셰이더 설정](#셰이더-설정)
- [프리셋](#프리셋)
- [응용 예](#응용-예)

## 개요

MTear는 다음 구성 요소로 이루어져 있습니다:

1. **MTearEditor** - 아바타에 부착되는 컴포넌트
2. **MTearEditorWindow** - 눈물 메시를 편집하기 위한 창
3. **Menno_Tear** - 눈물 셰이더
4. **MennoTearEditor** - 셰이더용 커스텀 인스펙터

이러한 구성 요소를 조합하여 눈물의 형태부터 외관까지 세밀하게 조정할 수 있습니다.

## 사용 방법

### 기본 설정

1. Menno 아바타를 엽니다
2. MTear 컴포넌트가 없는 경우 "MTear" 오브젝트에 추가합니다
3. 인스펙터에서 MTearEditor 컴포넌트를 선택합니다
4. "눈물 메시 편집" 버튼을 클릭합니다

![MTear 인스펙터](../../assets/images/mtear_inspector.jpg)

### 인스펙터에서 편집

MTearEditor에는 눈물 메시를 편집하기 위한 버튼이 표시됩니다.
버튼을 클릭하면 전용 편집기 창이 열립니다.

## 눈물 메시 편집기

MTearEditorWindow는 눈물 메시 형태를 편집하기 위한 전용 창입니다.

![눈물 메시 편집기](../../assets/images/mtear_editor.jpg)

### 주요 기능

- **편집 대상 오브젝트**: 눈물 메시를 포함하는 오브젝트 선택
- **자동 미러링**: 좌우 본을 대칭적으로 편집
- **색상 구분 표시**: 좌우 본을 파란색과 빨간색으로 구분
- **3D 조작**: 씬 뷰에서 직접 본을 이동 및 회전

### 본 조작 방법

1. 씬 뷰에서 파란색 또는 빨간색 구체(본)를 클릭하여 선택
2. 선택한 본은 핸들이 표시되어 이동 및 회전이 가능
3. 좌우 대칭 본은 자동으로 미러링됩니다
4. 인스펙터에서 위치, 회전, 크기를 수치로 조정할 수도 있습니다

※ 도구는 자동으로 View 도구로 전환되지만, 편집 종료 후에는 원래 도구로 돌아갑니다.

## 셰이더 설정

MTear는 전용 셰이더 "Menno_Tear"를 사용합니다. 이 셰이더에는 눈물 외관을 조정할 수 있는 다양한 매개변수가 있습니다.

![눈물 셰이더 설정](../../assets/images/mtear_shader.jpg)

### 기본 설정

- **눈물 속도** (_Speed): 눈물이 흐르는 속도 조정
- **눈물 위치** (_Tear_position): 눈물의 좌우 위치 조정

### 눈물 고임 설정

- **눈물 고임 강도** (_Tear_Puddle_intensity): 눈 안쪽 눈물 고임의 크기 조정

### 눈물방울 설정

- **눈물방울 강도** (_Tear_Drop_intensity): 뺨을 흐르는 눈물의 강도
- **눈물방울 크기** (_Tear_Drop_Size): 눈물방울 크기
- **추가 눈물방울 강도** (_Tear_Drop_extra_intensity): 보조 눈물방울의 강도
- **추가 눈물방울 크기** (_Tear_Drop_extra_Size): 보조 눈물방울의 크기

### 시각 효과

- **스페큘러 발광** (_Tear_Specular_Emissive): 눈물 광택의 발광 강도
- **스페큘러 강도** (_Tear_Specular_Strength): 눈물 광택의 강도
- **아웃라인** (_Tear_Outline): 눈물 테두리의 강도
- **아웃라인 색상** (_Tear_Outline_Color): 눈물 테두리의 색상
- **왜곡** (_Tear_Distortion): 눈물로 인한 배경 왜곡 정도

### 라이팅 설정

- **최소 광량** (_LightMinLimit): 어두운 환경에서의 최소 밝기
- **최대 광량** (_LightMaxLimit): 밝은 환경에서의 최대 밝기

## 프리셋

MTear 셰이더에는 3가지 표준 프리셋이 제공됩니다:

- **표준(Default)**: 균형 잡힌 표준 눈물
- **작음(Small)**: 작고 미묘한 눈물
- **큼(Big)**: 크고 눈에 띄는 눈물

셰이더 에디터 하단의 버튼에서 프리셋을 적용할 수 있습니다. 또한 자신의 설정을 프리셋으로 저장할 수도 있습니다.

## 응용 예

- **슬픈 표정과 조합**: 울음 표정과 함께 사용하여 감정 표현 강화
- **눈물 색상 변경**: 아웃라인 색상과 발광 설정으로 판타지 스타일의 눈물 표현
- **다양한 눈물 크기**: 상황에 따라 눈물 크기를 달리 사용

---

*이 문서는 정기적으로 업데이트됩니다. 최종 업데이트: 2025년 5월* 