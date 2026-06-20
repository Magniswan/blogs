---
layout: post
title: "iFlyCompassGUI：让iFlyCompass管理更轻松"
date: 2026-06-16
tags: [教程, iFlyCompass, WinUI3, 桌面应用]
---

# iFlyCompassGUI：让iFlyCompass管理更轻松

## 前言

`iFlyCompass`是一款非常强大的局域网服务器，结合了很多很多功能，但它需要在本地配置 Python 环境才能运行。基于源码安装调试的运作模式无疑给用户的使用带来了一些麻烦。于是，为了方便用户的使用，我决定开发一个桌面应用，这便是开发这个应用的初衷。

> 本程序依赖 **`iFlyCompass`** [（发布地址）](https://www.linearteam.top/make-%e8%bd%af%e7%a0%b4-great-again/)，版权归[**摸鱼真君不摸鱼**](https://moyuzj.cn/)所有。
>
> 该核心程序从 [iFlyCompass GitHub 仓库](https://github.com/MoyuZJ912/iFlyCompass) 自动下载，本启动器不对核心代码进行任何修改。
>
> 核心程序按 GPL v3 提供，**无任何担保**。完整协议文本请查看 [iFlyCompass 仓库中的 LICENSE](https://github.com/MoyuZJ912/iFlyCompass/blob/main/LICENSE)。


## 什么是 iFlyCompassGUI

`iFlyCompassGUI` 是 `iFlyCompass` 的 Windows 桌面管理工具，基于 `WinUI 3` 构建，提供图形化界面来安装、配置和管理 `iFlyCompass` 服务。

> 注意：由于 `WinUI 3` 框架的特性，该应用仅支持Windows 10 1809及以上版本。

## 功能

- 一键式下载、安装、更新、启动和关闭 `iFlyCompass` 服务
- 管理 `iFlyCompass` 的各个功能模块（用户管理、小说阅读器、视频播放器、AI对话等）
- 支持开机静默自启（没有系统托盘）
- ...

> 更多功能可能在后续版本中添加，可能不会在文章中即使更新。

## 安装教程

### 一、自动安装（推荐）

> 由于部分系统会自动禁用 Windows 更新服务，导致应用安装程序无法正常安装依赖，加上还需要手动安装证书，所以推荐使用自动安装方式。

1. 在 [GitHub release](https://github.com/Magniswan/iFlyCompassGUI/releases) 页面下载最新版本的 `iFlyCompassGUI-Setup.exe`
2. 双击运行安装程序
3. 安装程序会自动下载项目所需依赖、安装证书并安装应用

### 二、手动安装

1. 在 Release 页面下载最新版本的应用和证书文件（一般为 `iFlyCompassGUI_x.x.x.x_x64.msix` 和 `iFlyCompassGUI.cer`）
2. **安装证书**（首次安装时需要）：
   - 右键点击 `.cer` 证书文件，选择"安装证书"
   - 选择"本地计算机"，点击"下一步"
   - 选择"将所有的证书放入下列存储"，点击"浏览"，选择"受信任的根证书颁发机构"
   - 确认安全警告后，完成导入
3. 双击运行应用安装包，按照提示完成安装

## 使用教程

1. 首次安装并打开应用后你需要调用屏幕键盘，输入`iflycompass`（不区分大小写），然后就会进入安装界面。
> 至于为什么，自己品。
>
> 输入内容后续你可以在设置里面更改。
2. 安装完成后，接下来的使用就非常简单了，很多功能前端都有对应的注释，还是很好理解的。
![软件截图]({{ '/assets/images/2026-06-16-iFlyCompassGUI/image.png' | relative_url }})
3. 后续启动在开始菜单里面启动即可。可以在应用列表里面找一找，默认是不在桌面创建快捷方式的。


## Q&A

- Q: 为什么要舍弃兼容性而采用 WinUI 3 框架？

  A: 尽管 WinUI 3 框架构建的应用仅能在 Windows 10 1809及以上版本上运行，但是其性能、界面美观度都要优于一般的框架，同时，Windows的包管理机制也让应用的安装卸载更新更加方便。~~卸载的快速、无痕，也便于用户快速跑路，减少麻烦。~~

  在我看来，该应用本身也仅仅只是一层壳，用户完全可以在不使用该应用的情况下使用 `iFlyCompass` 服务。同时，我们可以看到，对于一些运行Windows 7系统的老机器，其普遍性能较差，若没有人特意优化，在日常使用中，也会经常出现卡顿现象。这种情况下，即使在追求现代美观的前提下进行了老系统的兼容，对老电脑的负载只会是火上浇油，得不偿失。

## 总结

`iFlyCompassGUI` 将繁琐的配置流程简化为直观的图形化操作，让更多用户能够轻松上手 `iFlyCompass`。无论是安装配置、服务管理还是内容维护，都变得前所未有的简单。

项目已开源，遵循 MIT 许可证，欢迎各位用户前往 [GitHub](https://github.com/Magniswan/iFlyCompassGUI) 查看项目代码，也欢迎大家在 [GitHub Issues](https://github.com/Magniswan/iFlyCompassGUI/issues) 上提出建议，帮助改进项目（顺手也可以给个 Star）。