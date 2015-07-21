---
layout: post
title: "Jekyll 环境准备"
description: ""
category: 技术相关
tags: [Jekyll]
---
{% include JB/setup %}


jekyll 搭建个人博客（静态网站）

1.jekyll是基于ruby的，首先安装ruby环境
	
	ruby下载连接：http://rubyinstaller.org/downloads/

	备注：下载ruby和Development Kit,ruby 安装完成，添加ruby到path中

2.安装完ruby后需要安装development kit

	在ruby的安装目录中，执行 ruby dk.rb init

3.由于有部分的组件还会依赖到python，所以这里建议也安装上python（可选）

4.安装jekyll，通过ruby的包管理器进行安装
	
	gem install jekyll

5.新建网站

	jekyll new xxx

6.查看新建网站，在新建的jekyll文件夹执行以下命令，启动jekyll服务

	jekyll serve --watch

	备注:浏览器端输入http://localhost:4000 查看个人网站


> ##参考链接
>
>> [jekyll博客搭建](http://cxshun.iteye.com/blog/1924153)
>>
>> [如何在CentOS上搭建ruby on rails环境](http://jingyan.baidu.com/article/642c9d34c0e6bc644a46f7f1.html)