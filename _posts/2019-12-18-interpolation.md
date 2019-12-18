---
title: 反距离加权插值
tags:
- R
- IDW
- geodistance
desc: interpolation via R
layout: post
---

利用反距离加权算法(IDW)对离散点进行插值，用的是R语言。自己对R是懵懵懂懂的，这次也算是一个练习吧。

这个过程中遇到的第一个难题就是距离问题。原始数据坐标是经纬度坐标，因此在进行插值前需要利用经纬度计算插值点与已知点之间的投影距离。还好遇到一个好心博主，对这一问题解释的很清楚([点这里](http://blog.sciencenet.cn/blog-255662-365318.html))。我使用的是“***geosphere***”包的 ***distm()*** 方法，很方便，给博主点赞。不过大名鼎鼎的 ***sp*** 包没有用过还，以后肯定有机会研究的

解决了这个难题剩下的就是插值喽， ***反距离加权算法*** 的原理还是很简单的，需要注意的是，通常选择距离的 ***幂*** 通常选择 ***2***，网上讲解很多，这里就不罗嗦啦。懒得搜索的[点这里](https://malagis.com/inverse-distance-weighting-interpolation-algorithm.html)，或[这里](http://blog.sina.com.cn/s/blog_816800900101f2lk.html)。
