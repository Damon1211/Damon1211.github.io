---
layout: post
title: "在linux下使用sqllite"
description: ""
category: 技术相关
tags: [sqllite]
---
{% include JB/setup %}

【Sqlite 使用总结】


说明：使用前需先安装sqlite3，CentOS6.5 默认安装

1.查看sqllite文件
	
	命令：

	sqlite3 db文件名

	例如：

	sqlite3 db.sqllite

2.查看当前所有的数据库

	.databases

3.查看数据库表（表list）

	.tables

4.查看表结构

	命令：

	.schema 表名

	例如：

	.schema host



> ##参考链接
>
>> [在linux下使用sqlite](http://www.cnblogs.com/gzggyy/archive/2012/07/19/2599645.html)
>>
>>