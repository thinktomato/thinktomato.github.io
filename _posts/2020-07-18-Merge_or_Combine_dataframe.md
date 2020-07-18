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

(1) merge(x, y, by = "row.names", all=TRUE), 该函数需要注意的是参数*by = "row.names"*，x,y 需是*data.frame* 格式；   
(2) cbind函数需行数相等且以同顺序排序，**无法使用公共索引**。   
***Note：*** 若取数据框A第3列"*area*"数据，两种获取方式获得数据类型不同：(1) A[,3]格式是numeric, (2) A["area"]格式是data.frame, 所以在merge中合并数据框某几列数据，应用第二种选取方式，否则出错。
```
id  length pop area
1   10     10  10
2   11     11  11
3   12     12  12
``` 

参考：https://stackoverflow.com/questions/6029743/merge-or-combine-by-rownames