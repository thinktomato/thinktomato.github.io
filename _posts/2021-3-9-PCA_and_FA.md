---
title:主成分分析和因子分析
tag:
- PCA; FA
desc:
layout
---

主成分分析(PCA)和因子分析(FA)都可以对数据进行降维，可能有时候PCA对原始数据的可解释性没有FA好。

先来看一下两者的计算步骤：

```
PCA:
1. 原始数据标注化
2. 建立相关系数矩阵R
3. 求解R的特征根和特征向量
4. 根据特征值累计贡献率确定主成分个数
5. 写出主成分F与原始数据X关系, F = AX 
```
```
FA:
1~4步和PCA完全一样
5. 建立载荷矩阵
6. 因子载荷矩阵方差最大旋转，X = AF
7. 根据高载荷确定因子实际意义
8. 计算因子得分
```
可以看到PCA是FA的一部分，PCA是将原始数据映射到新的低维坐标系中，FA在PCA的基础上根据数据协方差进一步计算的。

具体解释可参考
https://blog.csdn.net/Da___Vinci/article/details/83650705
https://blog.csdn.net/weixin_33949359/article/details/93294562
https://zhuanlan.zhihu.com/p/49481213


