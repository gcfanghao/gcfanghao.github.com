--- 
layout: post
title: 3分钟建立一个Jekyll Blog
date: 2012-01-12
categories:
    - 电脑
tags:
    - Blog
    - Jekyll
    - Git
    - GitHub
excerpt: 如何快速建立一个托管在github的blog。
---

如果你正考虑用[Jekyll](https://github.com/mojombo/jekyll)作为Blog系统，那么可以参考一下[Jekyll-Bootstrap](http://jekyllbootstrap.com/)，上面有从入门到精通的教程。如果你想快速的建一个站看看，那么下面几步可以让你在三分钟里建立一个运行在github上的blog，前提是你已经有了[github](https://github.com/)账号和[配置好了git](http://help.github.com/mac-set-up-git/)。

##一. 建立一个新的github repository

名字为*USERNAME*.github.com, *USERNAME*为你的github用户名

##二. 安装Jekyll-Bootstrap-Core

<pre class="prettyprint">
$ git clone https://github.com/plusjade/jekyll-bootstrap.git USERNAME.github.com
$ cd USERNAME.github.com
$ git remote set-url origin git@github.com:USERNAME/USERNAME.github.com.git
$ git push origin master
</pre>

##三. 额，没有三了

等一会去访问一下http://USERNAME.github.com，github已经为你生成了一个站点。
