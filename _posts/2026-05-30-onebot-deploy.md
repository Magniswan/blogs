---
layout: post
title: "笔上QQ（局域网内）使用教程"
date: 2026-05-30
tags: [教程, NapCat, QQ, 词典笔]
---

# 笔上QQ（局域网内）使用教程

#### 一、安装NapCatQQ

1. 前往 NapCatQQ 的 Releases 页面 下载 NapCat.Shell.Windows.OneKey.zip 无头绿色版本解压（注意解压的目录位置，我这里以 `C:\Program Files\NapCat` 为例）
2. 点击 `NapCatInstaller.exe` 等待自动化配置
3. 进入 `NapCat.XXXX.Shell` 目录
4. 启动 `napcat.bat`

## 配置NapCatQQ

1. 打开弹出的命令行窗口，按提示完成相应步骤

![命令行窗口]({{ '/assets/images/2026-05-30-onebot-deploy/image4.png' | relative_url }})

此时你在浏览器上有概率看到如下界面，只需要将上面提到的网页 Token 输入进去即可。

![浏览器 Token 输入界面]({{ '/assets/images/2026-05-30-onebot-deploy/image3.png' | relative_url }})

2. 网络配置

![网络配置 1]({{ '/assets/images/2026-05-30-onebot-deploy/image2.png' | relative_url }})

![网络配置 2]({{ '/assets/images/2026-05-30-onebot-deploy/image1.png' | relative_url }})

至此，电脑端配置就已经完成了。

## 配置笔上QQ（注意词典笔与电脑需要连接同一网络）

> 由于版本更新可能导致界面发生改变，故不提供图片教程。

1. 打开笔上QQ，点击设置
2. 上面会出现几个需要填写的参数，点击连接即可（还有其他选项自行勾选）

| 参数 | 解释（引号内替换为你自己的） | 实例（与前文实例保持一致） |
| --- | --- | --- |
| WebSocket地址 | `ws://"ipv4地址":"端口（默认3001）"/ws` | `ws://192.168.40.104:3001/ws` |
| Access Token | 自己改的 | `123456` |
