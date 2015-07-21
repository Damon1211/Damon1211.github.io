---
layout: post
title: "swhy ops 环境准备"
description: ""
category: 项目
tags: [swhy-ops]
---
{% include JB/setup %}


---

以下环境需在内网访问

---

【项目地址】

http://50.2.62.201/dongxin/swhy-ops

1.clone项目到本地
	git clone http://50.2.62.201/dongxin/swhy-ops

2.在develop分支基础上新建开发分支

	1）先切换到develop分支

		git checkout develop

	2）新建自己的开发分支(XXXXX 自己定义)

		git checkout -b feature-XXXXX

3.环境准备
	
	1）安装 npm

		yum install npm

	2）全局安装工具

		npm install -g yo grunt-cli grunt bower generator-angular

	3）安装virtualenv(在安装好pip的前提下执行)

		pip install virtualenv

4.初始化

	1）进入工程目录

		cd $Pro_ROOT/swhy-ops/
	
	2）启动python虚拟环境

		virtualenv venv

	3）安装python 依赖库

		pip install -r app/requirements.txt

	4）进入web目录

		cd $Pro_ROOT/swhy-ops/web

	5）执行以下命令

		npm install
		bower install

	6）启动前端

		cd $Pro_ROOT/swhy-ops/web
		grunt serve

	7)启动后端

		cd $Pro_ROOT/swhy-ops/app
		python run.py



备注：在项目地址页面最下面有原始文档