---
title: youtube-dl
comments: ture
category:
  - python
tags:
  - youtube
  - python
date: 2017-06-21 22:08:54
updated:
---

最强大的视频下载器

-支持断点续传

-支持800+网站视频

<!--more-->

## 官方简介

[youtube-dl](http://rg3.github.io/youtube-dl/) is a command-line program to download videos from YouTube.com and a few [more sites](https://rg3.github.io/youtube-dl/supportedsites.html). It requires the [Python interpreter](https://www.python.org/) (2.6, 2.7, or 3.2+), and it is not platform specific. We also provide a Windows executable that includes Python. youtube-dl should work in your Unix box, in Windows or in Mac OS X. It is released to the public domain, which means you can modify it, redistribute it or use it however you like.

youtube-dl是一个命令行程序，用于从youtube.com和一些其他网站下载视频。它需要python解释器(2.6及以上版本)，但这不是必须的。我们还提供了一个包含python的windows可执行文件。youtube-dl可以在你的unix框架、windows以及max os x中运行。youtube-dl是一个开源程序，这意味着你可以按你的喜好修改、重新发布和使用它。

## 快速入门

### 版本选择

根据官方简介，youtube-dl分为命令行版本和windows安装版。

我们当然是毫不犹豫的选择前者了。

### 安装

1. 下载并安装[python](https://www.python.org/downloads/)

2. 使用以下命令安装和升级youtube-dl

   ```
   pip install --upgrade youtube_dl
   ```

3. 下载并安装[ffmpeg](https://www.ffmpeg.org)，[安装视频](https://www.youtube.com/watch?v=pHR3ttH5t-w)

### 使用

查看目标视频包含哪些格式，并显示对应格式代码

```	
youtube-dl -F URL
```

下载选定格式代码

```
youtube-dl -f code URL
```

使用SS代理下载

```
youtube-dl --proxy localhost:1080 URL
```

使用混合命令下载最高品质视频

```
youtube-dl --proxy localhost:1080 -f bestvideo+bestaudio URL
```

## 进阶使用

### 一键下载（待补充）