---
layout: post
title: "使用 github 搭建自己的博客 "
author: 邹伟
description: "如何使用 github 搭建自己的博客。"
date:   2019-01-20 15:06:52 +0800
categories: [tutorial]
---

### 1.注册 github 账号

进入 <https://github.com/>，剩下的事情很简单。

为什么需要一个github账号？因为这是一个免费托管的代码的地方，全世界的程序员都在用。友好的是它还支持静态网站，这对于想拥有属于自己的博客又不想买空间的人来说，就是一个非常棒的选择咯。而且他还支持独立域名，也就是你每年只需花一个域名的钱就可以拥有一个属于自己博客啦。

### 2.创建 bolg 仓库

进入 <https://pages.github.com/>，如何创建blog仓库，照着做就行。
拥有了github账号，搭建博客的第一步就是创建博客仓库。为了与普通的代码仓库区分开来，这个仓库的名称是有特殊要求的，`账号名称.github.io`，这就是说一个账号只能托管一个静态网站。

### 3.安装 jekyll 工具

进入 <https://jekyllrb.com/docs/installation/>，这里要根据你使用的操作系统来选择安装教程。

为什么需要jekyll这个工具？用过wordpress的朋友都知道，你发布内容时是有一个管理后台的，发文章除正文外有很多工作要做，比如标题、日期、作者、标签、分类等等，这些以前都是由管理后台或内容管理系统搞定的，如果你用csdn、简书等大平台，他们默认都会给你提供这样的管理系统。同样的，想要利用github的便利，你也需要一个工具来帮你管理，为你写文章提供支撑。yekyll 就是一个工具，她让你只管放心写，写完后她帮你生成静态页面，然后你只需讲内容推送到github仓库即可。

不同的是，你需要一点学习工作，因为她不像其他大平台的后台那样直观，你需要了解一下她是使用方法。相信这对你不是事，稍稍折腾一下，就能搞定。

### 4.创建运行 blog 项目

看看 <https://jekyllrb.com/docs/usage/> 这里，常用的命令熟悉一下即可。

`yekyll new testblog` 这样就在当前目录下创建了一个 `testblog` 项目。
`yekyll s` 进入项目目录后，就可以本机查看你的博客网站了。

如果觉得OK，提交推送到 github 你的博客就对外发布啦。

### 5.如何管理 blog 的内容

- 页面（pages）

放在根目录下，表示一个单独页面。比如 about.md 。这就是说基本单独页面通过特定目录搞定。

更多说明见 <https://jekyllrb.com/docs/pages/>

- 文章（Posts）

放在 `_posts`目录下，文件必须按要求命名，EAR-MONTH-DAY-title.md，比如 2019-01-20-welcome.md
文件中必须包含页头（Front Matter）

```text
    ---
    layout: post
    title: welcome
    categories: [blog, travel]
    tags: [hot, summer]
    ---
```

也就是说，`日期`通过文件名称搞定，内容标题、类别、标签通过页头搞定。

更多说明见 <https://jekyllrb.com/docs/posts/>

- 页头（Front Matter）

更多说明见 <https://jekyllrb.com/docs/front-matter/>

- 集合（Collections）

相当于全局的变量集合。

更多说明见 <https://jekyllrb.com/docs/collections/>

- 数据文件（Data Files）

相当与文件数据库。

更多说明见 <https://jekyllrb.com/docs/datafiles/>

- 资产（Assets）

主要用于管理 css 和 js ,支持 sass 和 coffescript。

更多说明见 <https://jekyllrb.com/docs/assets/>

- 静态文件（Static Files）

主要用于管理图片、pdf等文件。

更多说明见 <https://jekyllrb.com/docs/static-files/>

### 6.如何理解 blog 的结构

更多说明见 <https://jekyllrb.com/docs/structure/>

### 7.如何自定义 blog 主题

更多说明见 <https://jekyllrb.com/docs/themes/>


> 本文内容纯属个人观点，如有疏漏，欢迎指正。
