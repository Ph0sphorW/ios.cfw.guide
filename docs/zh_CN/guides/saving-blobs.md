---
lang: zh_CN
title: "保存令牌"
excerpt: 保存令牌指南，确保你将来能够降级 iOS。
permalink: /zh_CN/saving-令牌s
redirect_from:
  - /zh-CN/blobs
  - /zh-CN/blob
  - /zh-CN/save-令牌s
  - /zh-CN/save-令牌
  - /zh-CN/saving-令牌
extra_contributors:
  - TheHacker894
  - airsquared
  - hopolapopola
  - wr3nch3000
  - Tanbeer191
  - itsnebulalol
---

本文将为你介绍保存令牌的完整流程，如果你想降级到旧的、已关闭签名的 iOS 或 iPadOS 版本，则需要用到令牌。下面有多种方法供你尝试。对于未越狱的设备，你需要使用"电脑端"方法。

## 使用 shshd 保存令牌

shshd 是一个用于自动保存令牌的插件。安装后，你无需担心手动保存令牌，因为它会在后台自动处理。你需要已越狱才能使用 shshd。如果尚未越狱，请参考[使用 TSS Saver 网站保存 Blob](#使用-tss-saver-网站保存-令牌)。

::: warning

shshd 仅兼容基于 Procursus 的越狱工具，例如 Taurine、Odyssey、Chimera 和 Odysseyra1n。如果你使用的是 unc0ver 或 checkra1n，请参考[使用 TSS Saver 应用保存令牌](#使用-tss-saver-应用保存-令牌)。

:::

1. 打开你的包管理器
1. 搜索 `shshd` 软件包
1. 下载并安装该软件包
1. 出现提示时，点击"完成"

当你下载 shshd 后，每次重新越狱时以及之后的每周，令牌都会自动保存。令牌可以在 [TSS saver 网站](https://tsssaver.1conan.com/v2/)获取。要检索它们，请前往"retrieve"并输入你的 ECID。

### 手动运行 shshd

通常情况下你不需要手动运行 shshd，但也可以通过终端来运行。

1. SSH 连接到你的设备，或下载 NewTerm 2
1. 在终端中输入 ```sudo /usr/sbin/shshd```
    - 如果提示输入密码，请输入你的 root 密码（默认设置为 `alpine`）

## 使用 TSS Saver 应用保存令牌

TSS Saver 应用可以安装在已越狱的设备上，让你只需轻点一下即可轻松保存令牌。如果尚未越狱，请参考[使用 TSS Saver 网站保存令牌](#使用 TSS Saver 网站保存令牌)。

1. 将 [repo.1conan.com](https://repo.1conan.com/) 添加到你的首选<router-link to="/package-managers">包管理器</router-link>的软件源中
1. 下载并安装 TSS Saver
    - 如果你在 iOS 14 上使用 unc0ver，还需下载并安装 `libkrw`
    - 如果你在 iOS 14 上使用 Taurine，还需下载并安装 `libkernrw`
1. 点击"Save Blobs"
1. 收到确认信息后，点击"Open"

## 使用 TSS Saver 网站保存令牌

TSS Saver 网站允许你通过输入一些设备特定信息来保存设备的令牌。保存后，你可以再次输入这些信息来访问令牌。

A12 及以上芯片的用户必须已越狱才能使用 TSS Saver 网站，因为它需要获取 ApNonce 和 Generator 配对信息。如果你尚未越狱，请参考[使用 blobsaver 保存令牌](#使用-blobsaver-保存令牌)

### 获取 Generator 和 ApNonce（仅限已越狱的 A12+ 设备）

::: tip

如果你在 iOS 14 上使用 unc0ver 或 Taurine，请分别安装 libkrw 或 libkernrw。

:::

1. 打开终端应用并运行 `sudo dimentio > dimentio.txt`
    - 或者，你也可以从 TSS Saver 应用中的 Generator 选项卡获取 Generator 和 ApNonce
1. 在 Filza 中进入 /var/mobile，打开 dimentio.txt
1. 复制文本文件底部 `Current nonce is` 后面的 0x 数字，以及 `entangled nonce:` 后面的数字。0x 数字是你的 Generator，entangled nonce 数字是你的 ApNonce。请妥善保管这些信息，稍后会用到
1. 按照本指南的其余步骤操作

### 保存令牌（所有设备）

1. 将 iOS 设备连接到 Mac 或 PC
1. 打开 iTunes 或访达
    - Windows 用户必须下载[普通版本](https://www.apple.com/itunes/)的 iTunes，而非 Windows 商店版本
1. 导航到设备摘要页面
1. 点击序列号字段两次
    - 这将切换显示你的 ECID 号码
1. 将这个 ECID 号码记录在你能稍后读取的地方
1. 打开 [TSS Saver 网站](https://tsssaver.1conan.com/v2/)
1. 输入你的设备 ECID
1. 选择你的设备
    - iPhone 6S、6S Plus 和 iPhone SE 用户需要通过从 App Store 下载 [AX-CPU](https://itunes.apple.com/us/app/ax-cpu/id1048174418?mt=8) 来获取主板配置信息
    - A12+ 用户需要输入 ApNonce 和 Generator 配对信息
1. 点击提交

## 使用 blobsaver 保存令牌

blobsaver 是一个跨平台的 PC 程序，兼容 Windows、macOS 和 Linux，让你可以在任何设备（无论是否越狱）上轻松保存令牌。它不像其他选项那么方便，但兼容最多的设备。

### blobsaver

1. 下载、安装并启动最新版本的 [blobsaver](https://github.com/airsquared/blobsaver/releases)
1. 将 iOS 设备连接到电脑，并确保设备已解锁
1. 点击第一个"Read from device"按钮，它将自动填入你的 ECID 和设备信息
1. 如果你的 iOS 设备不是 A12 或更高版本，则无需获取 APNonce，可以跳过下一步

### 获取你设备专属的 APNonce 和 Generator

在此过程中，请确保你的设备已解锁并连接到电脑。

1. 点击 APNonce 字段旁边的第二个"Read from device"按钮
1. 如果你已越狱，或者你的设备上已设置好你想保留的 generator/apnonce 配对，请选择"Jailbroken"。否则，选择"Unjailbroken"

你的设备将多次重启进入恢复模式。当你重启进入正常操作系统模式时，请解锁你的 iOS 设备。

::: danger

如果卡在恢复模式，请尝试使用 blobsaver"帮助"菜单中的"Exit Recovery Mode"选项。

:::

::: tip

这些值可以在任何时候重复使用来保存令牌，无论你是否已越狱。

:::

### 保存令牌

1. 填写完所有信息后，点击"Go"保存令牌
1. 你也可以点击"Save Device"保存当前设备的信息，以便日后再次为其保存令牌

### 在后台自动保存令牌

1. 你还可以选择设置 blobsaver 在后台自动保存令牌，无需手动打开 blobsaver
1. 保存一个或多个设备后，点击"Background Settings"开始设置
1. 选择你希望在后台自动保存哪些设备的令牌，blobsaver 会先进行测试以确保设备信息正确
1. 然后你可以使用"Change Frequency"按钮更改保存令牌的时间间隔
1. 准备就绪后，点击"Start Background"启用它
1. 现在你可以关闭 blobsaver，令牌将按照你设定的时间间隔在后台自动保存

## 保存恢复点令牌

保存恢复点令牌是指保存你上次更新时的签名，并将其转换为可用的令牌。因为你在该版本仍开放签名时进行了更新，所以可以重复使用这些令牌，它们仍然是有效的。但你保存的令牌类型取决于你升级到当前版本的方式。

### OTA 恢复点令牌

如果你是通过"设置"应用以无线（OTA）方式升级到当前版本，保存的将是"OTA 恢复点令牌"。这些令牌需要使用 **bootrom 漏洞**才能使用，并且**只能**与 FutureRestore 的 `--use-pwndfu` 参数配合使用。

### iTunes 恢复点令牌

如果你通过 iTunes/Finder 升级或恢复了当前版本，那么恢复点令牌将像普通令牌一样保存，你可以正常使用它们。但是，它们会因你是通过电脑恢复还是升级而有所不同。

如果你通过电脑进行了*恢复*，你的令牌将是"擦除"类型，**不能**与 FutureRestore 的"更新 (-u)"选项一起使用。

如果你通过电脑进行了*升级*，你的令牌将是"更新"类型，并且**只能**与 FutureRestore 的"更新 (-u)"选项一起使用。

### 保存恢复点令牌

### 使用 Deverser

::: danger

此方法需要 Linux 或 macOS 机器，以及已越狱并安装了 OpenSSH 的设备。

在 checkra1n/odysseyra1n 上，你不需要 OpenSSH，但对初学者来说还是建议安装。

:::

1. 在 Linux 或 macOS 机器上，运行 `git clone https://github.com/joshuah345/deverser.git && cd deverser` 从 GitHub 获取 Deverser 源码
    - 如果你已经完成此操作，请运行 `cd deverser` 和 `git pull` 获取最新更改
2. 运行 `chmod +x deverser.sh` 使其可执行，然后运行 `./deverser.sh` 启动脚本
3. 如果提示安装 img4tool，请回答 `Yes`
    - img4tool 将原始文件转换为可用的 SHSH 令牌
4. 输入设备的 IP 地址
    - 在 checkra1n/odysseyra1n 上，你也可以运行 iproxy。
        - 在 macOS 上，在另一个终端窗口中运行 `brew install libimobiledevice libirecovery` 安装 libimobiledevice，然后运行 `sudo iproxy 22 44`
        - 在 Linux 上，我们建议在 iDevice 上使用 OpenSSH，但如果你想手动安装 libimobiledevice，二进制文件链接在[此处](https://cadoth.net/~nyuszika7h/ios-builds/libimobiledevice-static-linux.tar.gz)
    - 要使用 OpenSSH，请在设备上安装它，并从 WiFi 设置中获取设备的 IP 地址
5. 脚本将要求你输入设备的 root 密码两次
    - 如果不确定，密码通常为 `alpine`

你可以在运行 Deverser 的目录（通常是 ~/deverser）中找到名为 `(YOUR ECID).dumped.shsh` 的令牌。

### 使用 SSH Ramdisk

::: danger

此方法需要 Linux 或 macOS 机器，以及一台运行 iOS 12+ 的 checkm8 设备。

这是一个更高级的方法，不建议初学者使用。

:::

1. 前往[此链接](https://github.com/verygenericname/SSHRD_Script)设置 ramdisk
    - 建议使用 `14.8` 作为 ramdisk 版本，但你可以自行选择
2. 运行 `./sshrd.sh dump-令牌s`
3. 最后，运行 `./sshrd.sh ssh`，然后在 SSH 会话中运行 `reboot`
    - 强制重启也可以

你可以在克隆仓库的目录（通常是 ~/SSHRD_Script）中找到名为 `dumped.shsh` 的令牌。

### 使用 System Info

::: danger

此方法目前无法正常工作，将无法获取你的恢复点令牌。

:::

1. 将 [https://apt.arx8x.net](https://apt.arx8x.net) 源添加到你的首选<router-link to="/package-managers">包管理器</router-link>中
2. 下载名为 `System Info` 的插件
![图片](https://imgur.com/a/g8XZPrM)
3. 下载 System Info 后，打开"设置"并进入 `通用 > 关于本机`
4. 向下滚动到 `ECID`
5. 在 `ECID` 上向左滑动，然后点击 `APTicket`
6. 点击 `Submit`

完成后将弹出一个显示"APTicket Submitted"的提示。你现在可以在 [shsh.host](https://shsh.host) 上访问你的令牌。

### 检查令牌类型

要检查你的令牌类型，请使用 [img4tool](https://github.com/tihmstar/img4tool)

1. 从互联网下载 IPSW 和 OTA zip 文件，然后从两个 IPSW 中提取 BuildManifest.plist
    - 善用搜索引擎
2. 运行 `img4tool -v IPSW_BuildManifest.plist -s blob.shsh2` 和 `img4tool -v OTA_BuildManifest.plist -s blob.shsh2`
3. 仔细查看输出内容，检查 img4tool 报告哪个 BuildManifest 成功了
