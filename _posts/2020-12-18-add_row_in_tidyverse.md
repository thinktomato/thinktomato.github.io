---
title: add_row 函数使用
tag:
- add_row; tidyverse
desc:
layout
---

假设有`tiblle`类型的变量*A*，使用`add_row`函数添加行数据。若该操作在`for`循环中，使用方式为`add_row(A, newrow)`,*A*数据不显示更新，原因是没有将添加完行后的数据重新赋值给*A*。

愚蠢的自己呀。