---
layout: post
title: "更改Linux yum源"
description: ""
category: 技术相关
tags: [linux]
---
{% include JB/setup %}

---

###修改Linux yum源

---

####更改Linux yum源（163源）

> 1、进入yum配置文件目录
> 
> 	cd /etc/yum.repos.d/
> 
> 2、备份配置文件
> 
> 	mv CentOS-Base.repo CentOS-Base.repo.bak
> 
> 3、下载163的配置
> 
> 	wget http://mirrors.163.com/.help/CentOS6-Base-163.repo，下载下来的文件名为 CentOS6-Base-163.repo
> 
> 4、改名
> 
> 	mv CentOS6-Base-163.repo CentOS-Base.repo
> 
> 5、更新数据库
> 
> 	yum update

