---
title: R利用ggsave保存含有中文的plot
tags:
- R
- ggsave
- Chinese characters
desc: 
layout: post
---

问题：     
默认设置，利用`ggsave`保存plot，若plot中含有中文字符，保存的图片中中文字符不显示。

解决方法：     
利用R包`Cairo`设置`ggsave`中文字字体。
> ggsave(plot, file = "test.pdf", device = cairo_pdf, family = "Song")

`Cairo`包中含有的字体参见https://blog.csdn.net/hongweigg/article/details/47907555    

参考：     
https://www.douban.com/note/626007158/

