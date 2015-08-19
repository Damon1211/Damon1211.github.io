---
layout: post
title: "mysql 案例集合"
description: ""
category: 技术相关
tags: [Mysql]
---
{% include JB/setup %}


####1.Mysql反向解析导致连接慢


	Mysql禁用DNS解析，连接速度会快很多

	linux下 修改 /etc/my.cnf(如果my.cnf不存在，可以复制/usr/share/mysql/my-medium.cnf 到etc下面)

	在my.cnf文件种[mysqld]下面添加
		
	skip-name-resolve

