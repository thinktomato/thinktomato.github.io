---
Title: 使用R进行数据处理，常用的小工具汇总
tags:
- R
- data processing
desc:
layout: post 
---

数据处理会遇到很多细节需要调整，R中的一些函数可以很方便的实现。

#### 1. 向量数据反向

rev()

#### 2. 绘图时调整实体x轴次序

使用ggplot绘图，可以调整实体的因子(facor)来绘图顺序

> ggplot(data[order(data$y, decreasing = T),],
>           aes(z, x, fill= factor(y, levels=("color1", "color2")))) +
>       geom_bar(stat="identity")

参考：https://stackoverflow.com/questions/32345923/how-to-control-ordering-of-stacked-bar-chart-using-identity-on-ggplot2

#### 3. 分列

`tidyr`包， `seperate`函数

#### 4. 排序

- `sort`对向量排序；
- `order` 利用某一列，可以对数据框排序；
- `dplyr`中`arrange`函数，可以利用几列，对数据框排序。

参考：https://www.cnblogs.com/hider/p/10019536.html

#### 5. 逻辑运算

- 交集：`intersect`
- 并集：`union`
- 找不同：`setdiff`
- 判断相同：`setequal`

参考：https://blog.csdn.net/woodcorpse/article/details/80494605