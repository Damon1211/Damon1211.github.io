---
layout: post
title: "Git错误列表"
description: ""
category: IT_Tech
tags: [Git]
---
{% include JB/setup %}


常见问题

1.git提交时备注中文时报错

	问题描述：

	warning: Your console font probably doesn't support Unicode. If you experience strange characters in the output, consider switching to a TrueType font such as Lucida Console!

	问题解决：

	git config --global core.autocrlf true