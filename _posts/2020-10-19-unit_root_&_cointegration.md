---
title: 面板数据，单位根检验，及协整检验
tags:
- panel data
- unite root
- cointegration
desc: 
layout: post
---

看到有人在用面板数据进行回归分析的时候，先进行了*单位根*检验和*协整检验*，目的是为了防止**伪回归**；自己查了相关资料，记录总结。

### 1. 面板数据进行回归的时候是否都要进行相关检验呢？

答案是否定的，一下情况不需要进行检验：(1)*large N large T*; (2) *large N small T*; 一下情况需要检测：(1) *large T small N*; (2) *T ≈ N*.

### 2. 单位根检验的目的是什么？

单位根用于检测时间序列数据的*平稳性*，平稳序列的好处就是数据方差为常数，可以方便的用于统计。对于时间序列$\sum_{t=1}^{T}Y_t$,

$$Y_t = \beta\Y_{t-1} + \sigma_{t}$$

可以证明当$\beta < 1$时，序列的方差为常数，当$\beta = 1$是序列的方差随时间而改变，为变数。

### 3. 协整检验是什么？

协整(co-integration) 指单个变量虽然是非平稳序列，但是多个变量通过简单的线性关系构成的新变量是平稳序列。如：

$$y_{t} - \betax_{t} = u_{t}$$

对$u_{t}$进行平稳性检验。

### 参考文献
1. https://www.zhihu.com/question/24691738
2. https://www.zhihu.com/question/57586704
3. https://en.wikipedia.org/wiki/Cointegration


