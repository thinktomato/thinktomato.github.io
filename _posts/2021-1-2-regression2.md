---
title:若两个变量(X1, X2)相互独立，为什么在二元线性回归中X1的系数受到X2的影响呢(2)？
tag:
- regression; parameter estimator
desc:
layout
---

以下各式中$x_{1i} = X_{1i} - \bar{X_1}; x_{2i} = X_{2i} - \bar{X_2}; y_i = Y_i - \bar{Y_i}$

(1) **一元线性回归的参数估算**

在一元线性回归分析$Y_i = b_0 + b_1X_{1i}$中, $b_1$的参数估计公式为：

$$
\hat{b}_1 = \frac{\sum x_{1i}y_i}{\sum x_{1i}^2} 
$$

(2)**二元线性回归的参数估算**

在二元线性回归分析$Y_i = b_0 + b_1X_{1i} + b_2X_{2i}$中，$b_1$的参数估计公式为：

$$
\hat{b}_{1}=\frac{\left(\sum y_{i} x_{1 i}\right)\left(\sum x_{2 i}^{2}\right)-\left(\sum y_{i} x_{2 i}\right)\left(\sum x_{1 i} x_{2 i}\right)}{\left(\sum x_{1 i}^{2}\right)\left(\sum x_{2 i}^{2}\right)-\left(\sum x_{1 i} x_{2 i}\right)^{2}}
$$

若变量$X_1$与$X_2$相互独立则

$$
Cov(X_1, X_2) = \frac{\sum (X_{1i} - \bar{X_1})(X_{2i} - \bar{X_2})}{n-1} = \frac{\sum x_{1i}x_{2i}}{n-1} = 0
$$

由上式可知$\sum x_{1i}x_{2i} = 0$，$b_1$的估计参数化简为

$$
\hat{b}_1=\frac{\sum y_ix_{1i}}{\sum x_{1i}^2}
$$

上式与一元线性回归中$b_1$的参数估算一致，**可知若$X_1$与$X_2$相互独立，$X_2$不影响$X_1$的参数$b_1$的估算**。

参考文献:
https://wenku.baidu.com/view/434aa032a9956bec0975f46527d3240c8547a175.html

https://wenku.baidu.com/view/6c5c66eab8f67c1cfad6b8bf.html

https://www.zhihu.com/question/437479654

https://zhuanlan.zhihu.com/p/56620950