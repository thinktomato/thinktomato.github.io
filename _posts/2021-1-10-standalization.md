---
title:回归过程中的数据标准化
tag:
- regression; standarlization
desc:
layout
---
## 数据标准化
*z-score*数据标准化所有数据都影响了数据的转换规则；而*max-min*只是最大最小值影响转换后的数据。(参考文献找不到了，抱歉)

## 什么时候进行数据标准化
数据标准化可以(1)消除量纲的影响，(2)各变量的变化范围一致。因此在涉及**欧式距离**或**变量之间比较**的算法。如，*k-means*聚类算法，*PCA*降维，*SVM*，*Lasso/岭*回归。

(1)数据标准化不影响线性回归的预测
(2)线性回归的系数大小并不说明该系数的**重要性**

参考文献:
https://blog.csdn.net/shwan_ma/article/details/80154888