---
lang: zh_CN
title: 安装 TrollStore (TrollRestore)
description: 通过 TrollRestore 安装 TrollStore
permalink: /zh_CN/installing-trollstore-trollrestore
sidebar: false
redirect_from:
extra_contributors:
  - opa334
  - JJTech
  - Dhinak
---

## 需求

- 一台正在运行 iOS/iPadOS 15.2 到 16.6.1，16.7 RC (20H18)，或者是 17.0 的设备
- 最新版的 [python3](https://www.python.org/downloads)
- 如果你正在使用 Windows，那么需要最新版本的 [iTunes](https://www.apple.com/itunes/download/win64) 
- 根据你的操作系统选择最新版的 [TrollRestore](https://github.com/JJTech0130/TrollRestore/releases)
  - Windows 用户请选择 `TrollRestore.exe`
  - 搭载了 Apple Silicon 的 Mac 用户请选择 `TrollRestore_macOS_arm64.zip`
  - 搭载了 Intel 的 Mac 用户请选择 `TrollRestore_macOS_amd64.zip`
  - Linux 用户请选择 `TrollRestore_Linux.zip`

::: warning

在继续下一步之前，如果你正在使用 *macOS* 或者 *Linux*，你需要先解压下载下来的 TrollRestore `.zip`。

:::

::: warning

由于此方法涉及到恢复修改后的备份，因此在继续下面的步骤之前你需要先禁用 “查找我的 iPhone” 。

完成这些步骤后你可以重新启用 “查找我的 iPhone” 。

:::

## 运行 TrollRestore

选择你正在运行的操作系统：

:::::: tabs

:::: tab name="macOS/Windows" :default="true"

::: warning

由于适用于 *搭载了 Intel 的 Mac* 的 TrollRestore 版本未经过公共签名，你需要按住 Control 键双击（如果你的 Mac 运行了 macOS Sonoma 或更早版本），或者尝试正常打开它，然后打开 `系统设置` -> `隐私与安全性` 并向下滚动直到看到 `仍要打开`。

如果你在操作过程中遇到问题，你也可以按照 `Linux` 标签中的步骤进行操作，因为这些步骤适用于所有平台（但比本标签中列出的正常步骤稍微复杂一些）。

:::

### 注入 TrollStore Helper

1. 把你的 iOS 设备连接到电脑上。
    - 确保你的电脑已标记为被信任的设备，并且被允许从电脑上查看手机内容
1. 打开文件资源管理器 (Windows) 或者是访达 (macOS)  
1. 定位到存储了下载 / 解压文件的文件夹
    - 大部分都会在 `下载` 文件夹里，如果你没有改过下载路径的话。
1. 双击 `TrollRestore`.
1. 当提示你输入要覆盖的系统应用名称时，输入名称并回车
    - 如果你不确定要覆盖哪个应用，可以直接选择 `提示`

::: tip

除了设备重启可以作为这些步骤顺利完成的标志之外，*设备上* 不会提示任何相关内容。

:::

TrollStore Helper 现在应该已经安装到你的设备上了。在你完成这些步骤之后，你的设备应该会重启一次。

::::

:::: tab name="Linux"

::: tip

虽然这个标签（以及相关的 zip 文件）是针对 Linux 的，但所有其他平台也可以按照这个标签的步骤操作，并使用 Linux `.zip` 文件作为正常可执行文件的替代方案。

:::

### 安装依赖项

1. 打开控制台应用程序
1. 运行 `cd <path/to/TrollRestore>`
    - 大部分情况下应该是 `cd ~/Downloads/TrollRestore_Linux`
1. 运行 `pip3 install -r requirements.txt` 然后跟随屏幕上的提示进行操作。

现在所有 TrollRestore 需要的依赖项应该都已经安装好了。

### 注入 TrollStore Helper

1. 把你的 iOS 设备连接到电脑上。
    - 确保你的电脑已标记为被信任的设备，并且被允许从电脑上查看手机内容
1. *在和前一个步骤一样的终端窗口里*，运行 `python3 trollstore.py`
1. 当提示你输入要覆盖的系统应用名称时，输入名称并回车
    - 如果你不确定要覆盖哪个应用，可以直接选择 `提示`

::: tip

除了设备重启可以作为这些步骤顺利完成的标志之外，*设备上* 不会提示任何相关内容。

:::

TrollStore Helper 现在应该已经安装到你的设备上了。在你完成这些步骤之后，你的设备应该会重启一次。

::::

::::::

## 安装 TrollStore

1. 解锁设备。
1. 打开你注入 TrollStore Helper 的应用。
1. 点击 `Install TrollStore`

你的设备应该会刷新，然后 Trollstore 就会安装在你的设备上了。

## 安装持久化助手

1. 打开 `TrollStore`
1. 点击 `Settings`，然后点击 `Install Persistence Helper`
1. 从应用列表中选择 `提示`
