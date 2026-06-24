---
lang: zh_CN
title: 通过 TrollHelper 安装 TrollStore
description: 通过 TrollStore Helper 包安装 TrollStore
permalink: /zh_CN/installing-trollstore-trollhelper
sidebar: false
redirect_from:
  - /zh-CN/installing-trollstorehelper
  - /zh-CN/trollhelper
  - /zh-CN/trollstorehelper
extra_contributors:
  - opa334
---

## 需求

- 一台正在运行 iOS 14.0 beta 2 至 16.6.1， 16.7 RC (20H18) 或 iPadOS 17.0 的**已越狱**设备
- 一个能工作的包管理器

::: tip

如果还没添加 `havoc.app` 软件源，你需要先去添加一下它。

:::

## 安装 TrollStore

1. 在你的包管里搜索 `TrollStore Helper` 包
1. 安装之后关闭包管，可以在桌面上找到 `TrollHelper`
1. 打开 `TrollHelper`  
1. 点击 `Install TrollStore`

你的设备应该会刷新，之后 TrollStore 就会安装在你的设备上了。

::: danger

如果你的设备正在运行 iOS 15.0 或更高版本，你必须执行以下步骤，否则设备重启到原生 iOS 之后你将无法启动 TrollStore。

如果你正在使用 iOS 14.0 至 14.8.1，可以忽略以下步骤。

:::

## 安装持久化助手

1. 打开主屏幕上的 `TrollStore`
1. 点击 `Settings`，然后点击 `Install Persistence Helper`
1. 从应用列表中选择 `提示`

重启设备之后，打开 `提示` 应用（或者其他任何你设置为持久化助手的应用）并点击 `Refresh App Registrations`。