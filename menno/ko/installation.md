---
layout: custom
title: ⬇️설치 방법
parent: Menno
nav_order: 1
permalink: /menno/installation/
lang: ko
---

# Unity에서 Menno 설치 및 M Avatar Setting 사용 방법

<iframe width="560" height="315" src="https://www.youtube.com/embed/imeaf9TB4ME?si=0a-RL1EgCnXRjdrQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Menno - 설치 방법

이 페이지에서는 Menno 아바타의 설치 방법에 대해 설명합니다.

## 다운로드한 파일의 구성

BOOTH에서 다운로드한 파일을 압축 해제하면 다음과 같은 구성이 됩니다:

```
📁 License
   📄 en.pdf
   📄 ja.pdf
   📄 ko.pdf
   📄 zh.pdf
📁 Resources
   📁 Menno
      📁 FBX
      📁 Texture
   📁 ToggleProps
      📁 FBX
      📁 Texture
📄 1. liltoon and MA.unitypackage
📄 2. Menno.unitypackage
```

* **License** - 각 언어의 라이센스 정보
* **Resources** - 아바타의 FBX 및 텍스처 등의 리소스 파일
* **1. liltoon and MA.unitypackage** - 첫 번째로 임포트해야 하는 패키지 (liltoon과 Modular Avatar 포함)
* **2. Menno.unitypackage** - 두 번째로 임포트하는 Menno 아바타 본체

## 사전 요구 사항

Menno 아바타를 사용하려면 다음이 필요합니다:

* [VRChat Creator Companion (VCC)](https://vcc.docs.vrchat.com/#download-it)
* Unity 2022.3.x (VCC를 통해 설치)
* Liltoon (1. liltoon and MA.unitypackage를 통해 설치)
* Modular Avatar (1. liltoon and MA.unitypackage를 통해 설치)

## 설치 단계 (VCC 사용)

### 1. VRChat Creator Companion 설정

1. [VRChat 공식 사이트](https://vrchat.com/home/download) 또는 [VCC Download It](https://vcc.docs.vrchat.com/#download-it)에서 VRChat Creator Companion (VCC)을 다운로드하고 설치합니다
2. VCC를 실행하고 초기 설정을 완료합니다
   - 필요에 따라 Unity Hub 설치
   - Unity 2022.3.x 설치

### 2. VCC로 아바타 프로젝트 생성

1. VCC에서 "새 프로젝트 생성"을 클릭합니다
2. 프로젝트 이름과 프로젝트 저장 위치를 선택합니다
3. 템플릿으로 "Avatar"를 선택합니다
4. "프로젝트 생성" 버튼을 클릭합니다
5. 프로젝트가 생성되면 "Unity에서 열기"를 클릭합니다

### 3. 필요한 패키지 임포트

1. `1. liltoon and MA.unitypackage`를 더블 클릭하여 임포트합니다
   - 이 패키지는 liltoon과 Modular Avatar를 추가합니다
   - VCC에서 이미 Modular Avatar를 설치한 경우 이 단계는 건너뛰어도 됩니다
2. 임포트 창에서 "Import" 버튼을 클릭합니다

### 4. Menno 아바타 임포트

1. `2. Menno.unitypackage`를 더블 클릭하여 임포트합니다
2. 임포트 창에서 "Import" 버튼을 클릭합니다
3. 임포트가 완료되면 아바타가 `Assets/emudotto/Menno` 폴더에 배치됩니다
   - 이 시점에서 M. Avatar Setting도 함께 임포트됩니다. 별도로 임포트할 필요가 없습니다.

### 5. 아바타를 씬에 배치

다음 방법 중 하나로 아바타를 씬에 배치할 수 있습니다:

#### 방법 1: 샘플 씬 사용 (권장)
1. Unity의 프로젝트 뷰에서 `Assets/emudotto/Menno/MennoScene.unity`를 찾습니다
2. `MennoScene.unity`를 더블 클릭하여 엽니다
   - 이 씬에는 이미 Menno 아바타가 배치되어 있습니다
   - 환경과 조명도 설정되어 있습니다

#### 방법 2: 기존 씬에 아바타 추가
1. Unity의 프로젝트 뷰에서 `Assets/emudotto/Menno/Menno.prefab`을 찾습니다
2. Menno.prefab을 씬 뷰에 드래그 앤 드롭합니다

### 6. 아바타 설정

1. 씬에서 Menno 오브젝트를 선택합니다
2. M. Avatar Setting을 엽니다 ([자세한 내용은 여기](/avatar-setting/))
   - Unity 메뉴에서 `Window > M Avatar Setting`을 선택합니다
   - 또는 Inspector에서 Menno를 클릭하고 "M. Avatar Setting 열기" 버튼을 클릭합니다
3. 필요에 따라 아바타 설정을 합니다

### 7. VRChat에 업로드

1. 씬에서 Menno 오브젝트를 선택합니다
2. VRChat SDK 제어판을 엽니다
3. "Build & Publish" 버튼을 클릭합니다
4. 필요한 정보를 입력하고 업로드를 완료합니다 