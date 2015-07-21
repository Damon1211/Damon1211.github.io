---
layout: post
title: "swhy ops 异常列表"
description: ""
category: 项目
tags: [swhy-ops]
---
{% include JB/setup %}

---

【异常汇总】


1.swhy-ops app 启动报销（python run.py）

	异常描述：ImportError: No module named flask.ext.sqlalchemy

	产生原因：python 环境依赖包没有安装

	解决方案，方法步骤：

		安装依赖包

		pip install Flask-SQLAlchemy



2.swhy-ops web 启动报错（grunt serve）

	操作系统：CentOS6.5

	异常描述：Warning: watch ENOSPC

	产生原因：系统限制一个用户可以watch文件的数量

	产生原因(en)：The system has a limit to how many files can be watched by a user. You can run out of watches pretty quickly if you have Grunt running with other programs like Dropbox. This command increases the maximum amount of watches a user can have.

	解决方案一,方法步骤：

		1. vi /etc/sysctl.conf

		2. 在文件最后一行添加如下参数信息（顶满格添加）

		fs.inotify.max_user_watches=524288

		3.执行 sysctl -p 使修改立即生效

	解决方案二，方法步骤：
		
		直接执行以下命令

		echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p




3.初始化前台静态文件报错（yo angular:route host/list）

	异常描述：Error: EACCES, permission denied '/root/.config/configstore/insight-yo.yml'

	产生原因：用户权限不够

	解决方案： chmod g+rwx /root /root/.config /root/.config/configstore