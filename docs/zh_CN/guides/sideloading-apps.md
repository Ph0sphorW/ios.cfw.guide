---
lang: zh_CN
title: "侧载应用"
description: 使用或不使用电脑进行侧载和重签应用的指南
permalink: /zh_CN/sideloading-apps
redirect_from:
  - /zh-CN/resign
  - /zh-CN/resigning
  - /zh-CN/altstore
  - /zh-CN/altdaemon
  - /zh-CN/altserver
  - /zh-CN/altdeploy
  - /zh-CN/sideload
  - /zh-CN/sideloading
  - /zh-CN/reprovision
  - /zh-CN/repro
  - /zh-CN/reprovision-reborn
  - /zh-CN/sideloadly
  - /zh-CN/resigning-apps
extra_contributors:
  - ssalagginkool
  - TheHacker894
---

## 前置阅读

半完全越狱需要侧载应用来执行越狱。使用普通 Apple ID 侧载的应用将在 7 天后过期（使用开发者 Apple ID 则为 365 天）。过期后，你将无法再打开该应用来重新越狱。

::: danger

如果你正在使用 iOS 16 测试版，需要事先执行额外步骤才能打开侧载的应用：

1. 打开"设置"
1. 进入"隐私与安全性"，找到"开发者模式"选项
1. 开启"开发者模式"，然后点击"重新启动"
1. 设备重启后，解锁设备，并确认你要启用开发者模式
    - 如果你启用了锁屏密码，则需要输入密码。

:::

## 侧载应用

### 使用 Sideloadly 侧载

::: tip

Sideloadly 兼容 iOS 7 及更新版本。

:::

1. 打开 Sideloadly
1. 将 iOS 设备连接到电脑
    - 确保你的电脑已获得信任并允许查看设备内容
1. 将你选择的 `.ipa` 文件拖放到 Sideloadly 中
1. 输入你的 Apple ID
1. 输入你的密码
    - Sideloadly 需要向其服务器发送请求才能使用免费开发者帐户。如果你不希望这样做，可以使用其他的 Apple ID。

### 使用 AltStore 侧载

<!--I will add AltStore 1.5 soon don't worry-->

::: tip

AltServer 仅兼容 iOS 12.2 及更新版本。

:::

1. 下载最新版本的 [AltServer](http://altstore.io/)、Windows 版 [iTunes](https://www.apple.com/itunes/download/win32)（如使用 Windows）和 Windows 版 [iCloud](https://secure-appldnld.apple.com/windows/061-91601-20200323-974a39d0-41fc-4761-b571-318b7d9205ed/iCloudSetup.exe)（如使用 Windows）
1. 安装适用于你操作系统的 AltServer
    - 在 macOS 上，打开"邮件"应用，在菜单栏中进入 `邮件` -> `偏好设置`
    - 点击`通用`选项卡，然后点击`管理插件`，勾选 `AltPlugin` 并应用
1. 通过 USB 将 iOS 设备连接到 Mac 或 PC
1. 点击菜单栏/系统托盘中的 AltStore/AltServer
1. 点击"安装 AltStore"
    - 按照屏幕上的所有提示操作
1. 打开"设置"，进入 `通用` -> `设备管理`，验证 AltStore
1. 打开 iTunes（Windows 或 macOS Mojave 及更早版本）或 Finder（macOS Catalina 及更新版本），启用 WiFi 同步
1. 下载你想要的 IPA 文件，在 iOS 设备上的 AltStore 中打开它
    - 确保你的 iOS 设备和 Mac 或 Windows PC 连接到同一个 WiFi 网络

## 重签应用

### 使用 ReProvision Reborn 重签

::: tip

ReProvision Reborn 兼容 iOS 9 及更新版本。

:::

1. 将 Havoc 源添加到你的首选包管理器（[havoc.app](https://havoc.app/)）
1. 安装 ReProvison Reborn
1. 打开 ReProvision Reborn 并按照屏幕上的所有提示操作
    - 系统会要求你输入 Apple ID。这只会发送给 Apple，不会发送给任何其他人。

### 使用 AltDaemon 重签

::: tip

AltDaemon 基于 AltStore，仅兼容 iOS 12.2 及更新版本。

:::

AltDaemon 允许 AltStore 自动重新签名这些应用，无需通过本地网络连接到运行 AltServer 的电脑。

1. 将 Chariz 源添加到你的首选包管理器（[repo.chariz.com](https://repo.chariz.com/)）
1. 下载并安装"AltDaemon"插件
1. 关闭你的包管理器
1. 对所有即将过期的应用进行签名
