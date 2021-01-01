---
title:一元线性回归与二元线性回归参数估计
tag:
- regression; parameter estimator
desc:
layout
---

在二元线性回归中$y = b_0 + b_1x_1 + b_2x_2$, 若$x_1$与$x_2$相互独立，$b_1$参数的估计是否受到$x_2$的影响呢？可以通过参数的估计公式来判断：

(1) 一元线性回归参数估计
模型为：$y = \beta_0 + \beta_1x$

![](\images\2020-12-27-univarible_regression.png)

(2)二元线性回归参数估计
模型为：$y = \beta_0 + \beta_1x_1 + \beta_2x_2$

![](\images\2020-12-27-binear_regression.png)

可以看到一元线性回归与二元线性回归模型中的$\beta_1$并不相同。