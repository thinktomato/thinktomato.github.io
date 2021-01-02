---
title:若两个变量(X1, X2)相互独立，为什么在二元线性回归中X1的系数受到X2的影响呢？
tag:
- regression; parameter estimator
desc:
layout
---

这个[回答](https://www.zhihu.com/question/437479654)特别好。问题中混淆了**独立**与**条件独立**，由于两个自变量(X1, X2)都与因变量Y相关，所以在Y已知的情况下，即以Y为条件，X1和X2并不一定条件独立。大致是这个意思，其实理解并不深刻。

原回答解释X1与X2相关性时用到了条件协方差，其计算公式如下：

![](\images\2021-1-2-条件分布.png)

参考文献：
https://www.zhihu.com/question/42080633/answer/121233345

https://math.cnu.edu.cn/docs/20170327183616843684.pdf
