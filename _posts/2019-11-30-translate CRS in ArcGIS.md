---
title: ArcGIS中地理坐标与投影坐标转换
tags:
- geogrophy coordinate
- project coordinate
- transform
desc: transform geogrophy coordinate to project coordinate
layout: post
---

在ArcGIS中转换地图坐标真是很让人困惑的事情，ArcGIS中预设了各种坐标系，就是没有国家最新的CGCS2000和WGS84之间的转换。在将WGS84转换为CGCS2000时，首先需要转换椭球，即进行地理坐标系之间的转换，其实两个坐标系框架差别不大，如果精度要求不高的情况下可以用WGS84替代CGCS2000参数；完成地理坐标系转换后在将地理坐标转换为投影坐标。
虽然网上都有一些转化[教程](https://blog.csdn.net/weixin_30699443/article/details/98459013)，但一般都是在WGS84和北京54或西安80之间的转换。

在利用ARCGIS进行分析时一定要转换为投影坐标系才可以，在精度要求不大的情况下，有时候我直接转换成UTM投影，这样很方便会。
