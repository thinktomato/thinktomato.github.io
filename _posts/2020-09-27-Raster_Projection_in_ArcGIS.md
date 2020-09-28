---
title: ArcGIS中投影栅格出错的解决方法
tags:
- ArcGIS
- Raster Projection
desc: 
layout: post
---

关于地图坐标系的笔记已经写了好几篇了，包含了(1)地理坐标系和投影坐标系的基础知识，(2)栅格投影,(3)地理坐标系投影变换。     

今天遇到的问题比较奇葩，使用*Raster Project*工具投影栅格时总是出错，提示*未找到表*或*没有当前记录*，试了各种方法无法解决，简直要气炸了。最后解决方法很简单**重启电脑**。现在还觉得气，ctmd。

可能原因是(1)要保存的那个硬盘空间不足;(2)手动结束ArcGIS进程造成的。

参考文献：       
https://help.watershed.ucdavis.edu/troubleshooting-error-999999-arcmap-and-arcgis


其他关于坐标系的文章总结如下：    
1. [ArcGIS中地理坐标与投影坐标转换](https://thinktomato.github.io/thinktomato.github.io/posts/translate-CRS-in-ArcGIS/)
2. [地图中的投影](https://thinktomato.github.io/thinktomato.github.io/posts/Projection_in_maps/)
3. [地图中的投影(2)](https://thinktomato.github.io/thinktomato.github.io/posts/Projection_in_ArcGIS/)
4. [栅格像元值及其个数在投影前后的变化](https://thinktomato.github.io/thinktomato.github.io/posts/Rater_to_project/)
5. [提取栅格数据的属性值](https://thinktomato.github.io/thinktomato.github.io/posts/extract_raster_attribution_to_table/)


