---
layout: post
title: "Flask 简介&安装-《带你进入 Flask Web 开发》"
author: thinkingpy
createdate: 2019-01-22 15:06:52 +0800
changedate: 2019-01-22 15:06:52 +0800
categories: ["tutorial"]
tags: ["flask web","flask",“web”,"教程"]
keywords: flask,flask简介,flask安装,flask虚拟环境
description: flask 是啥？拿 flask 进行 Web 开发，环境该如何搭建? 这个教程将向你详细说明。
---

* auto-gen TOC:
{:toc}

> 前言：《带你进入 Flask Web 开发》是一个系列学习教程。之所以起心动念的做这样一个教程，有两点原因：一是源于自身对 python 的喜爱，爱屋及乌；二是自己时常有一些 Web 开发的项目，想多掌握一把趁手的工具。最后将教程分享出来，目的也是促进自身学习和提高，因为教是最好的学习方式。

## Flask 简介

Flask（<http://flask.pocoo.org/>）是用 Python 写的轻量级 Web 框架，内核支持扩展三方模块或自建模块，可按需选择。它的两个核心依赖分别是 Werkzeug (<http://werkzeug.pocoo.org/>) 和 Jinja2 (<http://jinja.pocoo.org>)。Werkzeug 提供路由、调试和 Web 服务器网关接口（Web Server Gateway Interface,WSGI）；Jinja2 提供模板系统。

## 虚拟环境中安装 Flask

安装 Flask 当然要推荐使用虚拟环境，这样不仅可以避免和全局环境的包发生冲突，而且每个项目都可以建一个独立的虚拟环境，互不影响。创建虚拟环境通常使用 virtualenv 。大部分 Linux 发行版都提供了这个包，比如我用 Ubuntu 安装：

    sudo apt-get install python-virtualenv

如果你用 Mac OS X 系统，可以使用 easy_install 安装：

    sudo easy_install virtualenv

如果你用 Windows 系统，去搜一下应该也不复杂。

虚拟环境创建工具准备好后，创建一个项目目录 flasky ，然后进到目录创建虚拟环境 venv ：

    $ virtualevn venv
    New python executable in /home/zw/flasky/venv/bin/python3
    Also creating executable in /home/zw/flasky/venv/bin/python
    Installing setuptools, pip, wheel...
    done.

这样 flasky 目录下会多一个 venv 目录，这里放的就是虚拟环境，是基于全局环境的一个副本。如果想要切入虚拟环境：

    $ source ./venv/bin/activate
    (venv)zw@zwpc:~$

进入虚拟环境后，命名提示前面会有类似（venv）提示。然后我们就可以愉快的在虚拟环境里安装 flask :

    pip install flask

好了！一个热乎的 flask 安装完成。
