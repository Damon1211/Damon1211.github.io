---
layout: post
title: "Git错误列表"
description: ""
category: 技术相关
tags: [Git]
---
{% include JB/setup %}


常见问题

####1.git提交时备注中文时报错

问题描述：

	warning: Your console font probably doesn't support Unicode. If you experience strange characters in the output, consider switching to a TrueType font such as Lucida Console!

问题解决：

	git config --global core.autocrlf true


####2.解决github push错误The requested URL returned error: 403 Forbidden while accessing 

github push错误：

	git push error: The requested URL returned error: 403 Forbidden while accessing https://github.com/wangz/future.git/info/refs  

git version 1.7.1


解决方案：

	vim .git/config

修改:
	
    [remote "origin"]  
    url = https://github.com/wangz/example.git  

为：

	[remote "origin"]  
    url = https://wangz@github.com/wangz/example.git

再次git push，弹出框输入密码，即可提交

