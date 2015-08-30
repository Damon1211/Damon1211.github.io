---
layout: post
title: "设置Linux终端背景色透明"
description: "设置Linux终端背景色透明"
category: 技术相关
tags: [linux]
---
{% include JB/setup %}

---


####设置Linux终端背景色透明

1.安装gconf-editor

	yum install gconf-editor后

2.执行gconf-editor

	gconf-editor后

3.在对应目录下勾选	compositing_manager

	在/apps/metacity/general/下，勾选compositing_manager

4.在gnome-terminal里设置背景透明

5.terminal 背景色修改成功
