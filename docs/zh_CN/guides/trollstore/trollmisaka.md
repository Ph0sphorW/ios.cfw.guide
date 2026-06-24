---
lang: zh_CN
title: 安装 TrollStore (TrollMisaka)
description: 通过 TrollMisaka 安装 TrollStore
permalink: /zh_CN/installing-trollstore-trollmisaka
sidebar: false
redirect_from:
extra_contributors:
  - opa334
  - Alriceee
---

::: danger

这种方法极不可靠，在大多数情况下都应该避免使用。

如果你用的**不是** 15.7.2 到 15.8.3 版本的 A8(X) iPad 设备，你应该查看 <router-link to="/installing-trollstore">安装 TrollStore</router-link> 图表以查找更好的方法来安装 TrollStore。

如果你**正在使用**搭载了 A8(X) 的 iPad，且系统版本在 15.7.2 到 15.8.3 之间，你也可以这么做：
- <router-link to="/installing-trollstore-trollrestore">通过 TrollRestore 安装 TrollStore</router-link> （这需要一台电脑， 并且 “查找我的 iPhone” 功能也必须禁用）
- <router-link to="/installing-dopamine-sideloadly">通过 Sideloadly 安装 Dopamine</router-link> （如果你最终是为了越狱，那么更推荐这种方法）
- 继续跟随本指南（如果你不想越狱*并且*你也不想禁用你的 “查找我的 iPhone” 的话）

:::

## 需求

- 一台正在运行 iOS/iPadOS 14.0 到 15.8.3 的设备
- 你的设备上已经安装了 “提示” 应用
- 最新版本的 [Sideloadly](https://sideloadly.io/)
- 如果你正在使用 Windows，那么需要最新版本的 [iTunes](https://www.apple.com/itunes/download/win64) 
- 最新版本的 [TrollMisaka](https://github.com/straight-tamago/TrollMisaka/releases/latest)

## 安装应用

1. 打开 Sideloadly
1. 把你的 iOS 设备连接到电脑上
    - 确保你的电脑已标记为被信任的设备，并且被允许从电脑上查看手机内容
1. 把 TrollMisaka `.ipa` 拖进 Sideloadly
1. 输入你的 Apple ID
1. 输入你的密码

然后软件就会安装到你的 iOS 设备上了。

## 信任软件

1. 打开 `设置` -> `通用` -> `设备管理` -> `<你的 Apple ID>`
    - 鉴于使用不同，`设备管理` 也有可能叫做 `描述文件与设备管理`。
1. 点击 `信任 "<你的 Apple ID>"`

然后 TrollInstallerX 就可以从桌面上打开了。

## 添加一个键盘

1. 打开 TrollMisaka，然后正常退出，*将其保留在后台*
1. 打开 `设置` -> `通用` -> `键盘` -> `键盘` -> `添加新键盘...`
1. 选择 `TrollMisaka`
1. 点击 `TrollMisaka`，然后打开 `Allow Full Access`, 然后点击 `Allow`
1. 重新打开 TrollMisaka

重新打开 TrollMisaka，打开应用切换器并重启设备。

::: danger

在成功安装 TrollStore 之前不要完全关闭 TrollMisaka。否则的话你需要重新操作上述步骤。

:::

## 注入 TrollStore Helper

::: warning

这种方法可能需要好几次才可以成功。

:::

1. 解锁设备
1. 马上打开 `Spotlight 搜索` （在桌面中部向下滑动时跳出来的那个搜索栏）
1. 点击键盘上的地球图标
    - 如果有必要可以从键盘列表里面选择 `TrollMisaka`
1. 点击 `kopen`
    - 如果设备重启就再试一次吧。
1. 点击 `Install TrollStore`
    - 如果键盘看起来马上就刷新了，那么就再试一次。实在不行可以在 Safari 中重试上述步骤。

当它提示成功时，就可以进入下一环节了。

## 安装 TrollStore

1. 重新打开应用切换器
1. *从应用切换器里* 打开 TrollMisaka=
1. 点击 `Install TrollStore`

你的设备应该会刷新，然后 TrollStore 应该就会安装在你的设备上了。

## 安装持久化助手

1. 从桌面上打开 `TrollStore`
1. 点击 `Settings`，然后点击 `Install Persistence Helper`
1. 从应用列表里选择 `提示`
