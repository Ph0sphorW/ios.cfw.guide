---
lang: zh_CN
title: 安装 TrollStore (TrollInstallerMDC)
description: 通过 TrollInstallerMDC 安装 TrollStore
permalink: /zh_CN/installing-trollstore-trollinstallermdc
sidebar: false
redirect_from:
extra_contributors:
  - opa334
  - Alriceee
---

## 需求

- 一台正在运行 iOS/iPadOS 15.0 到 15.7.1 或 16.0 到 16.1.2 的设备
- 你的设备上已经安装了 “提示” 应用
- 最新版本的 [Sideloadly](https://sideloadly.io/)
- 如果你正在使用 Windows，那么需要最新版本的 [iTunes](https://www.apple.com/itunes/download/win64) 
- 最新版本的 [TrollInstallerMDC](https://dhinakg.github.io/apps.html)

## 安装应用

1. 打开 Sideloadly
1. 把你的 iOS 设备连接到电脑上
    - 确保你的电脑已标记为被信任的设备，并且被允许从电脑上查看手机内容
1. 把 TrollInstallerMDC `.ipa` 拖进 Sideloadly
1. 输入你的 Apple ID
1. 输入你的密码

然后软件就会安装到你的 iOS 设备上了。

## 信任软件

1. 打开 `设置` -> `通用` -> `设备管理` -> `<你的 Apple ID>`
    - 鉴于使用不同，`设备管理` 也有可能叫做 `描述文件与设备管理`。
1. 点击 `信任 "<你的 Apple ID>"`

然后 TrollInstallerMDC 就可以从桌面上打开了。

::: danger

如果你的设备正在运行 iOS 16.0 到 16.1.2，你还需要启用开发者模式。

如果要启用开发者模式，打开 `设置` -> `隐私和安全` 然后下滑直到你看见 `开发者模式`，点击进入这个设置项目并打开开发者模式并跟随屏幕上提示的操作即可。

:::

## 注入 TrollStore Helper

::: warning

如果你已经打开了 “提示”，那么在执行这些步骤之前你还需要重启设备。

:::

1. 打开 TrollInstallerMDC
1. 当提示 "Successfully replaced Tips binary"时， 关掉 `TrollInstallerMDC` 即可。
    - 如果提示错误那么就重新打开 TrollInstallerMDC

## 安装 TrollStore

1. 打开 `提示`  
1. 点击 `Install TrollStore`

你的设备应该会刷新，然后 TrollStorre 就安装在你的设备上了。

## 安装持久化助手

1. 从桌面上打开 `TrollStore`
1. 点击 `Settings`，然后点击 `Install Persistence Helper`
1. 从应用列表里选择 `提示`
