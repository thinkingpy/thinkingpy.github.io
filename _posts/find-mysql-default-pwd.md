---
layout: post
title: "如何找到（重新设置）deepin 中的 mysql 默认密码"
author: thinkingpy
createdate: 2019-01-29 15:56:01 +0800
changedate: 2019-01-29 15:56:07 +0800
categories: tutorial
tags: ["deepin","mysql",“密码”]
keywords: deepin,mysql,默认密码
description: deepin 上装上 mysql 死活找不到默认密码，最后只能重新设置搞定。
---

https://www.digitalocean.com/community/questions/mysql-stopped-and-it-can-t-be-restart
https://stackoverflow.com/questions/11990708/error-cant-connect-to-local-mysql-server-through-socket-var-run-mysqld-mysql

UPDATE mysql.user SET authentication_string = PASSWORD('root') WHERE User = 'root' AND Host = 'localhost';