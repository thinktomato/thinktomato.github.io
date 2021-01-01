---
title: latex插入图片报错"Cannot determine size of graphic"
tag:
- latex; figure
desc:
layout
---

latex插入图片是报错“Cannot determine size of graphic”， 原因是latex无法获取图片尺寸，解决方法就是手动设置图片大小。以pdf图片为例：

1. 打开pdf属性查看尺寸
2. 利用naheight和nawidth设置图片尺寸，如pdf尺寸为13cm*13cm，则\includegraphic[width = 5cm, naheight = 13cm, nawidth = 13cm]{fig.pdf}

参考：    
https://oldtang.com/2929.html

https://www.cnblogs.com/little-YTMM/p/6627194.html