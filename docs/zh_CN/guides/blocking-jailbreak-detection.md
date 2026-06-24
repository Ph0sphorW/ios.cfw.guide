---
lang: zh_CN
title: "阻断越狱检测"
description: 绕过并避免越狱检测
permalink: /zh_CN/blocking-jailbreak-detection
redirect_from:
  - /zh-CN/blocking
  - /zh-CN/jailbreak-detection
extra_contributors:
  - Absolucy
  - TheHacker894
---

::: danger

我们并不建议在越狱设备上使用与金融有关的应用，比如支付宝和各大银行的应用。如果有能力的话，尽量用另一台设备来使用这些应用。

:::

许多注重安全性的应用程序会有算法来检测并阻止越狱用户使用这些应用程序。这些应用包括各大银行的应用程序、一些在线游戏（例如 Pokemon Go、Mario Kart Tour）以及其他注重隐私的应用程序，如 Snapchat。

从安全角度来看，这的确是一个好的操作，毕竟越狱设备比原生 iOS 设备更容易被攻破。然而，当我们只是想使用一些必要的应用程序时，这可能会成为一个问题。

::: danger

阻断越狱检测可能会导致在某些应用中无法访问照片和其他文件。

:::

接下来，我们将逐一介绍可用于减少越狱检测的插件。但有些应用无法被绕过，无论使用什么方法，在越狱状态下都无法运行。

还有一些应用可能需要专门为其制作的绕过方案。

## 插件

- [A-Bypass](cydia://url/https://cydia.saurik.com/api/share#?source=https://repo.co.kr/&package=com.rpgfarm.a-bypass) (<a href="cydia://url/https://cydia.saurik.com/api/share#?source=https://repo.co.kr/">repo.co.kr</a>)
- [Liberty Lite (Beta)](cydia://url/https://cydia.saurik.com/api/share#?source=https://ryleyangus.com/repo/&package=com.ryleyangus.libertylite.beta) (<a href="cydia://url/https://cydia.saurik.com/api/share#?source=https://ryleyangus.com/repo/">ryleyangus.com/repo</a>)
- [Choicy](cydia://url/https://cydia.saurik.com/api/share#?source=https://opa334.github.io/&package=com.opa334.choicy) (<a href="cydia://url/https://cydia.saurik.com/api/share#?source=https://opa334.github.io/">opa334.github.io</a>)
- Libhooker Configurator (可以在 Odyssey repo 中获取)
- [KernBypass](cydia://url/https://cydia.saurik.com/api/share#?source=https://cydia.ichitaso.com/&package=jp.akusio.kernbypass-unofficial) (<a href="cydia://url/https://cydia.saurik.com/api/share#?source=https://cydia.ichitaso.com/">cydia.ichitaso.com</a>)
- [vnodebypass](cydia://url/https://cydia.saurik.com/api/share#?source=https://repo.xsf1re.kr/&package=kr.xsf1re.vnodebypass) (<a href="cydia://url/https://cydia.saurik.com/api/share#?source=https://repo.xsf1re.kr/">repo.xsf1re.kr</a>)

::: tip

Choicy 在默认的 BigBoss 源中即可下载，但我们建议添加开发者自有源以确保你能够下载到最新的版本。

:::

还有其他可用于隐藏越狱的软件，例如 [Shadow](sileo://package/me.jjolano.shadow)（<a href="sileo://source/https://ios.jjolano.me/">ios.jjolano.me</a>），但本指南仅介绍上述插件。

## 安装

1. 打开你的包管理器应用（例如 Cydia、Sileo、Zebra）
1. 添加上面链接的三个软件源
1. 搜索并安装这三个软件包
1. 出现提示时重新加载桌面

## A-Bypass

::: tip

据插件作者所述，A-Bypass 在基于 libhooker 的越狱工具上表现更好，例如 <router-link to="/installing-chimera">Chimera</router-link>、<router-link to="installing-odyssey">Odyssey</router-link>、<router-link to="/installing-odysseyra1n">odysseyra1n</router-link> 和 <router-link to="/installing-taurine">Taurine</router-link>。不过它在基于 Substrate/Substitute 的越狱工具（如 checkra1n 和 unc0ver）上也能正常使用。

:::

1. 打开"设置"应用
2. 向下滚动到 `A-Bypass`
3. 点击 `检查更新`
    - 如果某个新应用无法与 A-Bypass 配合使用，你应返回 A-Bypass 设置再次尝试检查更新。
4. 向下滚动并启用你希望阻断越狱检测的应用。

## Liberty Lite

1. 打开"设置"应用
1. 向下滚动到 `Liberty Lite`
1. 开启 `启用 Liberty`
1. 点击 `阻断越狱检测`
1. 启用所有你想要阻断越狱检测的应用

## Choicy

::: tip

这是希望在越狱设备上使用 Snapchat 的用户的最佳选择。

:::

::: tip

如果你使用基于 libhooker 的越狱工具，例如 <router-link to="/installing-chimera">Chimera</router-link>、<router-link to="installing-odyssey">Odyssey</router-link>、<router-link to="/installing-odysseyra1n">odysseyra1n</router-link> 或 <router-link to="/installing-taurine">Taurine</router-link>，那么 [libhooker configurator](#libhooker-configurator) 与 Choicy 功能相同，且原生集成在 libhooker 中。

:::

1. 打开"设置"应用
1. 向下滚动到 `Choicy`
1. 点击 `应用`
1. 点击一个你通过 Liberty Lite 选择的应用
1. 开启 `自定义插件配置`
    - 对于 Snapchat，开启 `禁用插件注入` 并跳过后续步骤
1. 确保选择了 `白名单`
1. 启用你正在使用的绕过插件——Liberty Lite 对应的是 `zzzzzLiberty`，A-Bypass 对应的是 `!ABypass2`
1. 对你选择使用绕过插件的每个应用重复此操作

## libhooker configurator

::: warning

此功能仅适用于基于 libhooker 的越狱工具。如果你使用基于 Substrate 或 Substitute 的越狱工具，例如 checkra1n 或 unc0ver，则此方法*无法使用*，你应该改用 [Choicy](#choicy)。

:::

1. 打开 `libhooker` 应用
1. 点击"应用"
1. 向下滚动到你希望配置的应用，并点击它
1. 在这里，你可以选择完全禁用该应用中的插件，或配置单独的插件。
   - 要配置单独的插件，开启"覆盖配置"，这将打开允许或拒绝特定插件的选项。
   - 例如，要仅允许 Liberty Lite，你可以选择`允许`，然后选择 `zzzzzLiberty`。
   - 如果你使用 A-Bypass，则应启用 `!ABypass2`。

## KernBypass（iOS 12.0 - 14.2）

::: tip

这是希望在越狱设备上使用任天堂应用（Mario Kart Tour、Animal Crossing: Pocket Camp 等）和 Pokemon GO 的用户的最佳选择。

:::

::: warning

KernBypass 在使用 unc0ver 的 iOS 14 上无法正常工作，请改用 [vnodebypass](#vnodebypass)。

:::

::: danger

KernBypass 是一个内核级插件。请勿在不支持的设备上安装，**使用风险自负**。

:::

1. 打开"设置"应用
1. 向下滚动到 `KernBypass`
1. 点击 `启用 KernBypass`
1. 启用所有你想要阻断越狱检测的应用

## vnodebypass

::: tip

vnodebypass 在可绕过的内容上与 KernBypass 类似，但请注意，在其启用期间，你将无法使用所有插件。

:::

::: danger

vnodebypass 是一个内核级插件。请勿在不支持的设备上安装，使用风险自负。

:::

1. 如果你在 iOS 14 上，请确保已安装 `libkrw` 1.1.0 或更新版本。如果你使用 unc0ver 或 checkra1n，该包在默认的 Elucubratus 源中即可获取。
2. 打开 `vnodebypass` 应用
3. 点击 `启用` 按钮
4. 当使用完需要绕过越狱检测的应用后，返回 `vnodebypass` 应用并点击 `禁用`
