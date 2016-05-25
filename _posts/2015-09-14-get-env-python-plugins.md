---
layout: post
title: "get env python plugins"
description: ""
category: 技术相关
tags: [Python]
---
{% include JB/setup %}

windows下 pip install -r pathto/requirements.txt 


1. pip freeze > requirements.txt，导出 --site-packages 下的libs 及其版本信息，到文件requirements.txt。

2. 使用pip install -r requirements.txt 来安装依赖库。


此时，会报 ValueError: 'Missing distribution spec'。

原因： win7 将txt文件默认存在unicode编码格式。 pip install 命令 识别的是utf-8格式。

解决：使用文本编辑器，将该文件保存为utf-8文本格式。
