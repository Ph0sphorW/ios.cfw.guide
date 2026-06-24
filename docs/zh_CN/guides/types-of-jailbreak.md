---
lang: zh_CN
title: "越狱的种类"
description: 对于不同越狱种类的介绍
permalink: /zh_CN/types-of-jailbreak
redirect_from:
  - /zh-CN/zh-CN/jailbreaks
extra_contributors:
  - Tanbeer191
---

所有的越狱并不是以同一种方式工作的。本文将会介绍几种常见的越狱种类，并介绍它们是怎么工作的。

## 这几种不同类型是什么？

这里有四种主要的越狱类型：

- 完美越狱（Untethered）
- 半完全越狱（Semi-Untethered）
- 半连接越狱（Semi-Tethered）
- 连接越狱（Tethered）

和电脑联系程度的高低决定了不同越狱的越狱类型。

### 完美越狱

---

完美越狱可以被认为是所有越狱中的顶峰。它们只需要通过网站、应用程序或计算机运行一次漏洞利用就可以做到永久越狱。

![一张 p0sixspwn 越狱的截图](/assets/images/p0sixpwn.png)

如果你的设备进行了完美越狱，那么你不需要任何进一步的操作来维持这种越狱状态。即使在重启设备后，你的设备也仍旧也是越狱的。

但是不幸的是，已经很久没有新的完美越狱发布给大众了，而且很可能在更长时间内也不会有。

完美越狱的唯一缺点是，如果出现了某些问题，设备可能会进入无限启动循环。这时候需要通过 iTunes 或访达（macOS Catalina 或更新版本）恢复设备。虽然这种情况发生的可能性很低，但确实有可能发生。

这里有两个完美越狱的例子： <router-link to="/installing-p0sixspwn">p0sixspwn</router-link> 和 Pangu9。

### 半完全越狱

---

半完全越狱是最近几年里较为受欢迎的越狱类型。半完全，意味着每次重启或关闭设备时都需要重新进行一次越狱。

<img src="/assets/images/odysseymain.png" width="180" alt="一张 Odyssey 越狱的截图" class="align-right"/>

半完全越狱通过利用设备本身的应用程序或网站运行漏洞来工作。鉴于利用漏洞的运行方式，这些越狱可以通过各自对应的应用程序相当轻松地移除。

这里有几个半完全越狱的例子： <router-link to="/installing-taurine">Taurine</router-link>、<router-link to="/installing-dopamine">Dopamine</router-link> 和 <router-link to="/installing-odyssey">Odyssey</router-link>。

### 半连接越狱

---

半连接越狱与半完全越狱非常相似。区别之处在于利用漏洞的过程必须通过计算机运行，而不是通过侧载的应用程序。

![一张 checkra1n 越狱的截图](/assets/images/checkra1n.png)

由于每次重启后都需要计算机协助重新越狱，大多数人都会选择使用半完全越狱而不是半连接越狱。

这里有几个半连接越狱的例子：<router-link to="/installing-palera1n">palera1n</router-link> 和 <router-link to="/installing-odysseyra1n">Odysseyra1n</router-link>。

### 连接越狱

---

连接越狱并不适合普通用户使用。为了利用潜藏的漏洞，这些设备可能一开始根本不能越狱，甚至有可能连启动都需要电脑的帮助。

因此，这些越狱通常只被越狱开发者用来为更新版本的 iOS 越狱做半完全越狱 / 半连接越狱的准备。
