---
layout: post
title: "Jekyll 使用案例"
description: ""
category: 技术相关
tags: [Jekyll]
---
{% include JB/setup %}


---

####1.服务启动，项目根目录下执行：

    jykell serve

####2.生成post文件，项目根目录下执行：

    rake post title = "how to create file"

      在_posts文件夹中生成 2015-07-21-how-to-create-file.md 文件

      目录结构如：./_posts/2015-07-21-how-to-create-file.md

####3.生成page文件，项目根目录下执行：

    1.rake page name="about.md"

      在根目录下生成 about.md 文件

      目录结构如：./about.md

    2.rake page name="pages/about.md"

      在跟目录下生成pages文件夹并在文件夹中生成about.md文件

      目录结构如：./pages/about.md

    3.rake page name="pages/about"

      在根目录下生成pages文件夹,在pages文件夹中生成about文件夹并在about文件夹中生成index.html文件

      目录结构如：./pages/about/index.html


---

## Update Author Attributes

In `_config.yml` remember to specify your own data:
    
    title : My Blog =)
    
    author :
      name : Name Lastname
      email : blah@email.test
      github : username
      twitter : username

The theme should reference these variables whenever needed.
    
## Sample Posts

This blog contains sample posts which help stage pages and blog data.
When you don't need the samples anymore just delete the `_posts/core-samples` folder.

    $ rm -rf _posts/core-samples

Here's a sample "posts list".

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>