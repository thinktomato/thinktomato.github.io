---
title: 异方差问题
tag:
- Heteroscedasticity; Cross data; panel data;
desc:
layout
---

异方差问题常出现在横截面数据中，面板数据中如果存在固定效应的影响也可看做异方差的影响。在回归分析中要求误差的方差是恒定的( $Var(\epsilon^2) = \sigma^2$ )，且与自变量独立无关( $Cov(X_i, \epsilon) = 0$ ), 不满足这两个条件，数据就存在异方差的问题，即误差项与自变量相关，自然误差项的方差就不是恒定的了。