---
title: 记录Hexo搭建的全流程和一些小问题
date: 2017/5/18
category: [hexo]
tag: [hexo]
---



# 记录Hexo-NexT搭建的全流程和一些小问题

[Hexo](https://hexo.io/zh-cn/)作为当前流行的静态博客搭建程序，网上有太多的教程，本片仅作为个人整理以方便大家查阅。

<!--more-->

## 安装

### 安装前提

> [Node.js](https://nodejs.org/en/)
>
> [git](https://git-scm.com/)

### 安装Hexo

确认电脑中已经安装以上两个软件后，使用npm安装hexo

```
$ npm install -g hexo-cli
```
安装 Hexo 完成后，我们首先需要为我们的项目创建一个**指定文件夹**（例如我在 D 盘目录下创建了一个文件夹 blog 。`D:\blog` ），在指定文件夹中执行下列命令， Hexo 将会在指定文件夹中新建所需要的文件。

``` bash
$ hexo init
```
等待安装，安装完成后，<span id="inline-green">指定文件夹</span> 的目录如下：
``` 
.
├── _config.yml
├── package.json
├── scaffolds
├── source
|   ├── _drafts
|   └── _posts
└──
```

我们继续执行命令
``` bash
$ hexo g
$ hexo s --debug
```
Hexo 将 `source` 文件夹中除 `_posts` 文件夹之外，开头命名为 `_`（下划线）的文件 / 文件夹和隐藏的文件将会被忽略。Markdown 和 HTML 文件会被解析并放到 `public` 文件夹，而其他文件夹会被拷贝过去。
这个时候，我们在浏览器中访问 `http://localhost:4000/` ，就可以看到基于 Hexo 的默认主题的原型：
![hexo-next-one-1](http://p1.bqimg.com/567571/27324b740c9e91e2.png)

### 安装NexT主题

#### 下载 NexT 主题

依旧是在当前目录下，使用 Git checkout 代码下载next主题文件：
``` bash
$ git clone https://github.com/iissnan/hexo-theme-next themes/next
```
等待下载完成。

<p id="div-border-left-yellow">在 Hexo 中有两份主要的配置文件，其名称都是 _config.yml 。其中，一份位于站点根目录下，主要包含 Hexo 本身的配置；另一份位于主题目录下，这份配置由主题作者提供，主要用于配置主题相关的选项。
  我们约定，将前者称为 <span id="inline-blue">站点配置文件</span>，后者称为 <span id="inline-purple">主题配置文件</span></p>

#### 启用 NexT 主题
打开 <span id="inline-blue">站点配置文件</span> ，找到 `theme` 字段，并将其值更改为 `next` 。
到此， NexT 主题安装完成。下一步我们将验证主题是否正确启用。在切换主题之后、验证之前，我们最好使用 `hexo clean` 来清除 Hexo 的缓存。

#### 验证主题
首先启动 Hexo 本地站点，并开启调试模式（即加上 `--debug`），整个命令是 `hexo s --debug`。在服务启动的过程，注意观察命令行输出是否有任何异常信息。当命令行输出中提示：
`INFO  Hexo is running at http://0.0.0.0:4000/. Press Ctrl+C to stop.`
此时即可使用浏览器访问 `http://localhost:4000/` ，检查站点是否正确运行。
<p id="div-border-left-green">当你看到站点的外观与下图所示类似时即说明你已成功安装 NexT 主题。这是 NexT 默认的 Scheme —— Muse</p>
![hexo-next-one-1](http://p1.bqimg.com/567571/8333728b5eaab526.png)
现在，我们已经成功安装并启用了 NexT 主题。

<p id="div-border-top-blue">关于更多基本操作和基础知识，请查阅 [Hexo](https://hexo.io/zh-cn/) 与 [NexT](http://theme-next.iissnan.com/) 官方文档.</p>


### 总结：本地调试步骤
三部曲：
``` bash
$ hexo clean
$ hexo g
$ hexo s --debug
```
这种带debug的运行，如果出现错误，可以在命令行中看到错误提示信息。

### 总结：部署步骤
三部曲：
``` bash
$ hexo clean
$ hexo g
$ hexo d
```
当然在部署之前，需要先配置好配置文件中的deploy。


### 常用命令
``` bash
$ hexo new "postName"  #新建文章
$ hexo new page "pageName" # 新建页面
$ hexo generate # 生成静态页面至public目录
$ hexo server # 开启预览访问端口(默认端口4000，'ctrl+c'关闭server)
$ hexo deploy # 项目部署
$ hexo help # 查看帮助
$ hexo version # 查看Hexo的版本
```

### 简写命令
``` bash
$ hexo new == hexo n
$ hexo generate == hexo g
$ hexo server == hexo s
$ hexo deploy == hexo d
```


### 常见问题1
在hexo的配置和设置文件中，在冒号后面没留空格会导致出问题：
错误的设置：
```
author:Neveryu
email:react.dong.yu@gmail.com
language:zh-CN
```
正确的设置：
```
author: Neveryu
email: react.dong.yu@gmail.com
language: zh-CN
```

### 常见问题2
关于Git提交中用户名和Email的设置
```
git config --global user.name "Your name"
git config --global user.email "Your email"
```

### 常见问题3

Hexo 中的图标使用的是 [Font Awesome](http://fontawesome.io/) ，所以，我们的博客已经自带了 Font Awesome 中的所有图标，基本可以满足我们的所有需求，我们可以去 Font Awesome 中查找我们想要使用的图标。
<i class="fa fa-github"></i> `<i class="fa fa-github"></i>`
<i class="fa fa-github fa-lg"></i> `<i class="fa fa-github fa-lg"></i>`
<i class="fa fa-github fa-2x"></i> `<i class="fa fa-github fa-2x"></i>`