---
title: 地图中的投影
tags:
- map
- projection
desc: it introduces various projections in map
layout: post
---

在计算各国家土地面积的时候发现计算结果和实际面积有很大的出入，肯定是地图中投影设置错误了，于是求助万能的互联网，发现了各种有趣的投影，可以参考这个[网站](http://zhihu.geoscene.cn/article/419)，挺有趣的心形的，五角星等等。

主要还是介绍一下古蒂**等面积**投影(Goode homolosine projection)，这个投影是不连续的投影，适用与全球小比例尺栅格地图，可以有效减少面积的变形。其参数由国地质勘探局 (USGS) 的地球资源观测和科学中心 (EROS) 提供。其他应用广泛的全球投影有伪墨卡托投影(WGS 84/Pseudo Mercator),其WKID为3857，各互联网公司使用的就是这个坐标系，ArcGIS中对应的WKID为102100。

参考：
1. https://desktop.arcgis.com/zh-cn/arcmap/latest/map/projections/goode-homolosine.htm
2. https://www.jianshu.com/p/8deac5e002da
3. http://zhihu.geoscene.cn/question/35058#!answer_form
