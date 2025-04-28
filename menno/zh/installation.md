---
layout: custom
title: ⬇️安装方法
parent: Menno
nav_order: 1
permalink: /menno/installation/
lang: zh
---

# Menno - 安装方法

本页面介绍了Menno虚拟形象的安装方法。

## 下载文件的结构

从BOOTH下载的文件解压后，结构如下：

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

* **License** - 各种语言的许可证信息
* **Resources** - 虚拟形象的FBX和纹理等资源文件
* **1. liltoon and MA.unitypackage** - 首先需要导入的包（包含liltoon和Modular Avatar）
* **2. Menno.unitypackage** - 第二个需要导入的Menno虚拟形象本体

## 前提条件

使用Menno虚拟形象需要以下条件：

* [VRChat Creator Companion (VCC)](https://vcc.docs.vrchat.com/#download-it)
* Unity 2022.3.x（通过VCC安装）
* Liltoon（通过1. liltoon and MA.unitypackage安装）
* Modular Avatar（通过1. liltoon and MA.unitypackage安装）

## 安装步骤（使用VCC）

### 1. 设置VRChat Creator Companion

1. 从[VRChat官方网站](https://vrchat.com/home/download)或[VCC Download It](https://vcc.docs.vrchat.com/#download-it)下载并安装VRChat Creator Companion (VCC)
2. 启动VCC并完成初始设置
   - 根据需要安装Unity Hub
   - 安装Unity 2022.3.x

### 2. 使用VCC创建虚拟形象项目

1. 在VCC中点击"创建新项目"
2. 选择项目名称和保存位置
3. 选择"Avatar"作为模板
4. 点击"创建项目"按钮
5. 项目创建后，点击"在Unity中打开"

### 3. 导入必要的包

1. 双击`1. liltoon and MA.unitypackage`进行导入
   - 这个包会添加liltoon和Modular Avatar
   - 如果已经通过VCC安装了Modular Avatar，可以跳过这一步
2. 在导入窗口中点击"Import"按钮

### 4. 导入Menno虚拟形象

1. 双击`2. Menno.unitypackage`进行导入
2. 在导入窗口中点击"Import"按钮
3. 导入完成后，虚拟形象将被放置在`Assets/emudotto/Menno`文件夹中
   - 此时M. Avatar Setting也一同导入。不需要单独导入。

### 5. 将虚拟形象放置在场景中

可以通过以下任一方法将虚拟形象放置在场景中：

#### 方法1：使用示例场景（推荐）
1. 在Unity的项目视图中找到`Assets/emudotto/Menno/MennoScene.unity`
2. 双击`MennoScene.unity`打开
   - 此场景中已经放置了Menno虚拟形象
   - 环境和灯光也已设置

#### 方法2：将虚拟形象添加到现有场景
1. 在Unity的项目视图中找到`Assets/emudotto/Menno/Menno.prefab`
2. 将Menno.prefab拖放到场景视图中

### 6. 配置虚拟形象

1. 在场景中选择Menno对象
2. 打开M. Avatar Setting（[详情请点击这里](/avatar-setting/)）
   - 从Unity菜单中选择`Window > M Avatar Setting`
   - 或者，在Inspector中点击Menno，然后点击"打开M. Avatar Setting"按钮
3. 根据需要调整虚拟形象设置

### 7. 上传到VRChat

1. 在场景中选择Menno对象
2. 打开VRChat SDK控制面板
3. 点击"Build & Publish"按钮
4. 输入必要信息并完成上传 