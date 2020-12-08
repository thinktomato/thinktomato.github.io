---
title: 在R中使用ggplot绘图，控制x轴标签显示
tag:
- R
- x axis
desc:
---

1. 使用ggplot绘图，x轴显示的不是数据框(data.frame)定义的x，而是自动标注的，将x转换成 *factor* 就可以了;这时若绘制曲线，同时需要设置*group=1*.
   *ggplot(data, aes(x=factor(x), y= y, group = 1))*

2. 若x轴标签太多，拥挤到一起，可以使用scale_x_discrete(breaks = (your breaks))来手动标注。