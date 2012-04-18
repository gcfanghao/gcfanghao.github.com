--- 
layout: post
title: rails学习笔记：安装（基于mac）
date: 2012-04-18 09:16:46
categories:
    - ruby on rails
tags:
    - ruby
    - rails 
---
最近看了关于rails和python的一些文章，觉得这两种语言确实有独到之处，其中有一篇文章比较客观的介绍了两者的[特点](http://robbin.iteye.com/blog/444015),文章作者也是老前辈了，他的评价是值得参考的。

既然有兴趣，我想深入了解和学习，不过目前我更感兴趣的是web领域的编程开发，所以想先了解下在web应用编程方面效率更高的rails，因为没有时间和精力同时接触两种语言，python只好往后放一放了。

以下是我的一些学习心得。
首先从安装开始。

+ 操作系统:  `Mac OS X Lion 10.7`
+ Ruby版本:  `ruby 1.8.7 (2012-02-08 patchlevel 358)`
+ Rails版本: `Rails 3.2.3`
+ 数据库版本: `sqlite3 3.7.3`

##安装前准备
先安装以下三款软件：

1. Xcode
2. Command line tools
3. Macports

<span class="label label-info">Xcode</span> 是Apple的开发人员工具，它是免费的，可以在`Mac Store`中下载，共1.43G，如果网速不快，需要等待一段时间；安装完成后，还需要注册Apple Developer ID 才能使用，这一步很简单。

<span class="label label-info">Command line tools</span> 的安装：打开`xcode`>`Preference`>`Download`，可以看到`Command line tools`，大约180M。

<span class="label label-info">Macports</span> 是一个软件包管理系统，用来简化Mac OS X和Darwin操作系统上软件的安装,它可以让用户在终端中简单的输入port install 软件包名称来安装软件包，软件的下载、编译、安装以及它依赖的所有其他软件包的安装都会自动完成。
<a class="btn" href="http://www.macports.org/install.php">点击下载</a>

<span class="label label-important">注意</span> `Xcode`和`Command line tools`必须安装，否则在安装`ruby`过程中会出现错误。

##Mac OS X 上安装rails
打开Apple`终端`：

**升级SQLite3
<pre class="prettyprint">
sudo port upgrade sqlite3
</pre>

**安装Ruby
<pre class="prettyprint linenums">
sudo port install ruby
sudo port install ruby-rubygems
</pre>

**安装Rails
<pre class="prettyprint linenums">
sudo gem update --system
sudo gem uninstall rubygems-update
sudo gem install rails
sudo gem install sqlite3
</pre>
<span class="label label-important">注意</span> 这样安装之后，操作系统上可能会有两个版本的Ruby，需要检验运行相关工具的版本的正确性。通过以下命令检验每个工具是否已经安装在同一目录：
<pre>
which ruby irb gem rake
</pre>
显示结果：
<pre>
/opt/local/bin/ruby
/opt/local/bin/irb
/opt/local/bin/gem
/opt/local/bin/rake
</pre>

>Mac本身自带了Ruby，但版本比较老，而我们开发所需要的一般都是最新的Ruby。由于Mac相关环境可能会用到Ruby的旧版本，直接删除旧版本会影响系统相关特性。



>待续