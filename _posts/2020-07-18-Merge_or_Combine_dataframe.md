---
title: 横行合并数据框或添加列数
tags:
- R
- merge
- cbind
desc: use merge and cbind in R
layout: post
---

在R中想要合并两个数据框，依据为行名称，可以使用merge和cbind函数。    

(1) merge(x, y, by = "row.names", all=TRUE), 该函数需要注意的是参数*by = "row.names"*；    
(2) cbind函数需行数相等且以同顺序排序，**无法使用公共索引**。

参考：https://stackoverflow.com/questions/6029743/merge-or-combine-by-rownames