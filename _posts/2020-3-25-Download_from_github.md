---
title: 如何迅速的下载github资源
tags:
- skill
- github
desc: 
layout: post
---
直接下载GitHub的资源，其速度慢到让人砸电脑，于是网上搜可以快速下载的方法，这个是自己亲试的，效果很好。使用***wget*** 走代理。

> wget /**文件链接**/ -e use_proxy=yes -e  http_proxy=127.0.0.1:1087

转载自知乎用户Arthur的回答：https://www.zhihu.com/question/276143842