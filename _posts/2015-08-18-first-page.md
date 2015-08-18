---
layout: post
title: 在github上的第一篇博客
---
拿了本上周买的github书籍去沙发上躺着看，突然想研究在github上建博客了。

#1.在github上建博客#

其实很简单，建个库，库的名字叫username.github.io，其中username和你的用户名一样就可以。

然后上传一个index.html，访问username.github.io应该就可以看得到了。

如果看不到，看看是不是没进行邮箱校验。

具体参考[官网的教程](https://pages.github.com/)，非常简单。

#2.使用jekyll#

因为只能上传html的静态文件，而我们希望写一篇博客只需要写内容，这就需要模板渲染。github支持jekyll。

如果写博文时想要在本地看效果，就要安jekyll，具体参考[官网教程](https://help.github.com/articles/using-jekyll-with-pages/)。

不算难，但有两点——

##1)在使用gem之前要为gem换源，因为官方源被墙：##

>gem sources -l
gem sources --remove https://rubygems.org/
gem sources -a http://ruby.taobao.org/

##2)在安装jekyll之前需要先安装devkits##

>在[官网](http://rubyinstaller.org/downloads)下载devkits
解压
执行ruby dk.rb init及ruby dk.rb install，在install之前可能需要改下config.yml，配置ruby安装地址。

之后可以找找jekyll模板，因为全手动来累死人，模板解压到username.github.io这个库的文件夹下，jekyll serve，如果可以在localhost:4000上看到页面，就成功了。

然后就折腾_posts文件夹里的文件，每个文件就是一篇博文，随时写随时在浏览器看效果，ok之后提交到github，即可在username.github.io中看到了。

#3.markdown#

markdown语法说明可以看[这里](http://wowubuntu.com/markdown/)，本质是用一些简洁的标记，生成html的标签，但不影响html标签的样式。

所以我们写博客的时候实际是内容和结构一起写的。

比如[我的第一篇博客](http://qidafang.github.io/2015/08/18/first-page/)，源码在[这里](https://github.com/qidafang/qidafang.github.io/blob/master/_posts/2015-08-18-first-page.md)。

因为github能识别markdown语法，所以直接显示了内容。