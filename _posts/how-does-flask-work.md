---
layout: post
title: "Flask 简介&安装-《带你进入 Flask Web 开发》"
author: thinkingpy
createdate: 2019-02-02 15:06:52 +0800
changedate: 2019-02-02 15:06:52 +0800
categories: tutorial
category-title: 教程
tags: ["flask web","flask",“工作原理“,"教程"]
keywords: flask,flask简介,工作原理
description: 写一个 flask 程序真简单，那它是怎么运行的呢？
---

* auto-gen TOC:
{:toc}

> 前言：《带你进入 Flask Web 开发》是一个系列学习教程。之所以起心动念的做这样一个教程，有两点原因：一是源于自身对 python 的喜爱，爱屋及乌；二是自己时常有一些 Web 开发的项目，想多掌握一把趁手的工具。最后将教程分享出来，目的也是促进自身学习和提高，因为教是最好的学习方式。

上篇文章 [Flask 简介&安装](/tutorial/2019/01/22/setup-flask-venv.html) 我们介绍 flask 以及在虚拟 python 环境如何安装 flask，这篇文章我们将通过一个例子讲解 flask 的工作流程和基本原理。

## 先上例子
之前我们已经创建了 flasky 目录，现在我们在目录下创建一个 hello.py 文件，编写如下代码。

```python
from flask import Flask

app=Flask(__name__)

@app.route('/hello')
def hello_world():
    return 'hello,world.'
```

app.run()

好了，五行代码，大功告成！你可能会着急运行这个程序看看是啥效果，小码迫不及待的敲下如下命令：

    python hello.py

纳尼？咋什么也没发生。这里就要说说 Web 程序是怎么运行的。运行Web程序需要三个东西：

1.浏览器：就是我们这个网页所用的程序，比如我一般用 Google Chrome。
2.Web 服务器：你打开这个网页的时候，浏览器要把网页内容从一个地方拿过来，这个地方就是服务器，而且上面会有处理 Web 请求的程序，就是 Web 服务器。
3.Web 程序：你打开的网页包含写什么内容，这个是就是由 Web 程序控制的。比如我们刚才写的 Web 程序，可以返回”hello world.“。

知道这三个东西，那上面写 Web 程序实际运很明显还差 Web 服务器。但是开发阶段当然不用那么麻烦搞一个正式的服务器，这点 flask 已经为你想好了，为我们准备了一个简单的内置 Web 服务器。现在我们看看怎么跑起来：

Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/70.0.3538.77 Safari/537.36