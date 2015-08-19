---
layout: post
title: "tomcat error list"
description: ""
category: 技术相关
tags: [Tomcat]
---
{% include JB/setup %}



####1.Tomcat version 6.0 only supports J2EE 1.2, 1.3, 1.4, and Java EE 5 Web modules


	修改project的.setting folder下面org.eclipse.wst.common.project.facet.core.xml文件，里面配置有各种版本信息。

	把<installed facet="jst.web" version="3.0"/> 改成低些的版本version="2.5" 




---
