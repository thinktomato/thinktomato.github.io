---
title: 在R中绘制带平均值的分组箱线图(boxplot)
tags:
- R
- grouped boxplot
- mean value
- ggplot
desc: How to plot grouped boxplot with mean value
layout: post
---

使用`ggplot`绘制 *箱线图* ，(1) 若需要分组，使用`fill`函数来设置分组依据；(2) 控制组内因子绘制顺序，设置`fill`对应的`factor(groups, level)`中的`level`顺序即可；(3) 为每个箱体添加平均值点，使用`stat_x_discript()`函数，`position`参数设置为`position_dodged(width=0.75)`。

完整的例子如下：

```
# library
library(ggplot2)

# create a data frame
variety=rep(LETTERS[1:7], each=40)
treatment=rep(c("high","low"),each=20)
note=seq(1:280)+sample(1:150, 280, replace=T)
data=data.frame(variety, treatment ,  note)

# grouped boxplot
data$treatment <- factor(data$treatment, levels = c("low", "high"))
ggplot(data, aes(x=variety, y=note, fill=treatment)) + 
  geom_boxplot() +
  stat_summary(fun = mean, geom = "point", position = position_dodge(width = 0.75))
```
效果如图：

![效果图](\images\2020-10-11-boxplot_in_R.png)

参考：
1. https://www.r-graph-gallery.com/265-grouped-boxplot-with-ggplot2.html
2. https://stackoverflow.com/questions/43414864/ggplot2-boxplot-stat-summary-text-placement-by-group