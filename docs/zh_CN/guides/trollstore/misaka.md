---
lang: zh_CN
title: 安装 TrollStore (Misaka)
description: 通过 Misaka 安装 Trollstore
permalink: /zh_CN/installing-trollstore-misaka
sidebar: false
redirect_from:
extra_contributors:
  - opa334
  - Alriceee
---

## 需求

- 一台正在运行 iOS/iPadOS 16.0 到 16.6.1 的 iOS/iPadOS 的设备
- 你的设备上已经安装了 “提示” 应用
- 最新版本的 [Sideloadly](https://sideloadly.io/)
- 如果你正在使用 Windows，那么需要最新版本的 [iTunes](https://www.apple.com/itunes/download/win64) 
- 最新版本的 [Misaka](https://github.com/straight-tamago/misaka/releases/latest)

## 安装程序

1. 打开 Sideloadly
1. 把你的 iOS 设备连接到电脑上
    - 确保你的电脑已标记为被信任的设备，并且被允许从电脑上查看手机内容
1. 把 Misaka `.ipa` 拖进 Sideloadly
1. 输入你的 Apple ID
1. 输入你的密码

然后软件就会安装到你的 iOS 设备上了。

## 信任软件

1. 打开 `设置` -> `通用` -> `设备管理` -> `<你的 Apple ID>`
    - 鉴于使用不同，`设备管理` 也有可能叫做 `描述文件与设备管理`。
1. 点击 `信任 "<你的 Apple ID>"`

然后 Misaka 就可以从桌面上打开了。

::: danger

如果你还没有启用开发者模式，你还需要启用它。

如果要启用开发者模式，打开 `设置` -> `隐私和安全` 然后下滑直到你看见 `开发者模式`，点击进入这个设置项目并打开开发者模式并跟随屏幕上提示的操作即可。

:::

## 注入 TrollStore Helper

::: warning

这种方法可能要尝试好几次才能成功，耐心。

:::

1. 打开 Misaka
1. 点开 "Packages [Emu/Var]" 选项栏
1. 点击左下角的按钮（称为 "ToolBox" 的按钮），然后点击 `Install TrollStore`，接着点击 `Tips`

当你点击 `Tips` 之后你的设备就会进行一次刷新。

## 安装 TrollStore

1. 解锁设备
1. 打开 “提示”
1. 点击 `Install TrollStore`

你的设备应该会刷新，然后 Trollstore 就会安装在你的设备上了。

## 安装持久化助手

1. 打开 `TrollStore`
1. 点击 `Settings`，然后点击 `Install Persistence Helper`
1. 从应用列表中选择 `提示`
