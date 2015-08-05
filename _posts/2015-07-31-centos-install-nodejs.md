---
layout: post
title: "Centos 安装 NodeJs"
description: ""
category:集成篇 
tags: [NodeJs]
---
{% include JB/setup %}



准备命令：

	yum -y install gcc make gcc-c++ openssl-devel wget

下载源码及解压：

	wget http://nodejs.org/dist/v0.10.26/node-v0.10.26.tar.gz

	tar -zvxf node-v0.10.26.tar.gz

编译及安装：

	make && make install

验证是否安装配置成功：

	node -v


参考链接：

	[Centos 安装 NodeJS](http://www.cnblogs.com/hamy/p/3632574.html)
