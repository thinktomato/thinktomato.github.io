---
title: ArcGIS中图例显示缺失值
tags:
- ArcGIS
- NULL VALUE
- 缺失值
- 图例标注
- desc:
- layout: post
---

整理好的数据连接到ArcGIS中，有些值是缺失的，在属性表中为*空*；在设置属性为*数量显示*时，默认将空值忽略。这样出图的时候不太容易在图例中标注*缺失值*。解决方法有两个：

1. 将缺失值标记为999等其他不易混肴的数据；注意不要写成0，很容易和有意义的其他值混肴。
2. 在设置好图形属性后，重新导入另一份相同的图形文件，缺失值在第二个文件中标注即可。

参考：https://gis.stackexchange.com/questions/147728/how-to-symbolize-null-values-in-arcgis-using-quantities-symbology/147730