---
lang: zh_CN
title: 安装 TrollStore (TrollInstallerX)
description: 通过 TrollInstallerX 安装 TrollStore 
permalink: /zh_CN/installing-trollstore-trollinstallerx
sidebar: false
redirect_from:
extra_contributors:
  - opa334
  - alfiecg
  - Alriceee
---

::: warning

搭载了 A8(X) 的 iPad 仅支持 14.0 到 15.1 版本的系统。

:::

TrollInstallerX 支持所有运行 14.0 到 15.1.1 版本的 iOS/iPadOS 设备，和运行 15.2 到 16.6.1 版本的 A9(X) 及更高版本设备，以及运行 17.0 **beta 1** 到 17.0 **beta 4** 版本的 A10(X) 设备。

## 需求

<div class="custom-container tip" id="ifJailbreaksAppSigned"><p>
为了在没有电脑的情况下也能方便安装，TrollInstallerX 已经在 <a href="https://jailbreaks.app/" target="_blank">jailbreaks.app</a> 上签名。
</p></div>

- 最新版本的 [Sideloadly](https://sideloadly.io/)
- 如果你正在使用 Windows，那么需要最新版本的 [iTunes](https://www.apple.com/itunes/download/win64)
- 最新版本的 [TrollInstallerX](https://github.com/alfiecg24/TrollInstallerX/releases/latest/download/TrollInstallerX.ipa)
  - 如果你在用正在运行 16.3 版 iOS 的黄色 iPhone 14 或者 Plus (**20D50**)，那么你需要使用 [TrollInstallerX-20D50](https://github.com/alfiecg24/TrollInstallerX/releases/latest/download/TrollInstallerX-20D50.ipa)，而非常规的 TrollInstallerX。

## 安装应用

1. 打开 Sideloadly
1. 把你的 iOS 设备连接到电脑上
    - 确保你的电脑已标记为被信任的设备，并且被允许从电脑上查看手机内容
1. 把 TrollInstallerX `.ipa` 拖进 Sideloadly
1. 输入你的 Apple ID
1. 输入你的密码

然后软件就会安装到你的 iOS 设备上了。

## 信任软件

1. 打开 `设置` -> `通用` -> `设备管理` -> `<你的 Apple ID>`
    - 鉴于使用不同，`设备管理` 也有可能叫做 `描述文件与设备管理`。
1. 点击 `信任 "<你的 Apple ID>"`

然后 TrollInstallerX 就可以从桌面上打开了。

::: danger

如果你正在运行 iOS 16.0 或者更高版本，并且没有使用上文所提到的 jailbreaks.app 来安装 TrollInstallerX，你需要开启开发者模式。

如果要启用开发者模式，打开 `设置` -> `隐私和安全` 然后下滑直到你看见 `开发者模式`，点击进入这个设置项目并打开开发者模式并跟随屏幕上提示的操作即可。

:::

## 运行 TrollInstallerX

1. 打开 TrollInstallerX
1. 点击 `Install TrollStore`
    - 如果你的设备卡在了 "Exploiting Kernel" 这一步上， 那就重启设备
1. 当提示选择一个应用以安装 "persistence helper" （持久化助手）的时候， 尽量选择一个你 **最不经常** 使用的应用
    - 如果你不知道选哪个就选 `提示`
    - 如果在这一步*之前*你的设备就重启了的话那么你需要再试一次。耐心。

在这之后 TrollStore （一般来说）和持久化助手都会被安装到你的设备里。

::: danger

运行了 iOS 16.5.1 的 A15、A16 和 M2 设备，以及 A12 及更高版本的 iOS 16.6 到 16.6.1 设备，在完成上述步骤后，你需要通过已安装的持久化助手来安装 TrollStore，在下文的 `额外步骤` 中会提到。

其他的设备**不需要**执行下面的步骤。

:::

## 额外步骤

::: warning

如果持久化助手没有装进你选择的应用，正常关机，重新启动你的设备，打开你想要作为持久化助手的应用，然后**从应用切换器**中关掉这个应用，并运行 TrollInstallerX 再试一次。

:::

1. 打开你选择作为持久化助手的应用
1. 点击 `Install TrollStore`.

现在 TrollStore 就会被安装到你的设备上了。
