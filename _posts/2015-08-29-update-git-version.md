---
layout: post
title: "Linux Centos 升级Git"
description: "Linux Centos 升级Git"
category: 技术相关
tags: [linux]
---
{% include JB/setup %}

---

1.安装rpmforge安装包库

	1) rpm -i 'http://pkgs.repoforge.org/rpmforge-release/rpmforge-release-0.5.3-1.el6.rf.x86_64.rpm'
	2) rpm --import http://apt.sw.be/RPM-GPG-KEY.dag.txt

2.启用rpmforge-extras库

	1) vi /etc/yum.repos.d/rpmforge.repo
 
	2) 找到[rpmforge-extras]，把enabled=0改成enabled=1

3.升级git

	1) yum update git
 
	2) git --version

4.关闭rpmforge-extras库、清理

	1) vi /etc/yum.repos.d/rpmforge.repo

	2) 找到[rpmforge-extras]，把enabled=1改成enabled=0

	3) yum clean all