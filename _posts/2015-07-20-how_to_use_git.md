---
layout: post
title: "如何使用Git"
description: ""
category: 技术相关
tags: [Git]
---
{% include JB/setup %}


---

##新增&更新文件 提交步骤

1.缓存改动（操作后文件在本地）
	
	git add .

	备注：后面的点(.)不能省略

2.提交（操作后本地）

	git commit -m "这是一个提交注释"

3.上传（操作后文件上传到服务器）

	git push origin master  

备注：

	如果要修改文件 应该先从版本库更新文件

	git pull

---

##Git 操作方法汇总



####新建分支“feature_x”

	git checkout -b feature_x

####切换到主分支“master”

	git checkout master

####删除新建立的分支“feature_x”

	git branch -d feature_x

####提交分支到远端仓库

	git push origin <branch>

####删除远端仓库的分支

	git push origin :branch-name

	备注：冒号前面的空格不能少，原理是把一个空分支push到server上，相当于删除该分支。
	
####delete remote file

	git rm -rf <filename>
	git commit -m 'commont'
	git push origin feature-hostmanagement

####Git删除全局配置信息

	git config --global --unset user.name
	git config --global --unset user.email
	git config --global --unset credential.helper

####Git 本地忽略
	
	1.忽略跟踪

		git update-index --assume-unchanged /path/to/file

	2.恢复跟踪

		git update-index --no-assume-unchanged /path/to/file

####Git永久存储用户名密码

	git config --global credential.helper "store"

####Git删除已注册用户名

	git config --unset --global user.name

####Git 合并方式

	1.快进式合并（fast-farward merge） 直接将master分支指向dev分支 
	
	2.正常合并:在master分支上生成一个新的节点（关键参数 --no-ff）

	备注：可用gitk(Win7) 图形界面查看

####Git创建Tag
	
	1.创建Tag

		git tag -a v0.0 -m ‘version 0.0′

	2.查看Tag

		git tag

	3.查看相应标签的版本信息

		git show v0.0



> ##参考链接
>
>> [Git - 简易指南](http://www.bootcss.com/p/git-guide/)
>>
>> [Git - 使用经验与技巧总结](http://www.cnblogs.com/ToDoToTry/p/3936779.html)