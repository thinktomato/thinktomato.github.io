---
title: LISA 时间路径
tags:
- Time structure
- LISA
- time-space analysis
desc: Indroduction of the LISA time path
layout: post
---

Lisa时间路径(LISA Time Path)方法是对LISA(Local indicator of spatial autocorrelation)时间维度的扩展，将时间截面上的局部空间自相关性扩展到时间序列上空间结构的变化。各研究个体空间相关性的变化(HH,LH,LL,HL)可以使用**Markov chain matrix**来表示；其变动强度可以用变动长度(Length)来表示;变动曲折性用弯曲度(tortuosity)表示；变动稳定性用稳定性(instability)表示；时空跃迁用空间自相关状态转化的概率来表示。

#### 1.截面坐标

个体在时间截面的坐标$L_{it}$为$(y_{it}, yl_{it})$, $y_{it}$为个体本身的属性值，$yl_{it}$为个体的空间滞后值，一般表示为$yl_{it} = \sum_{i=1}^nWy_{it}$。

#### 2.变动长度

个体变动总长度与总体平均长度比值，若$\Gamma$大于1，则变动强度较大。
$$\Gamma_{it}=\frac{N\sum_{t=1}^{T-1}d_{it}(L_{it},L_{it+1})}{\sum_{n=1}^N\sum_{t=1}^Td_{it}(L_{it},L_{it+1})}$$ 

#### 3.变动弯曲度

个体变动总长度与首末长度的比值，$\Delta_i$越大变化路径越曲折。

$$\Delta_i=\frac{\sum_{t=1}^{T-1}d_{it}(L_{it},L_{it+1})}{d(L_0,L_t)}$$

#### 4. 变动稳定性

个体长度变动方差与总体变动方差比值。

$$\Lambda_i=\frac{N*\sigma_i}{\sum_{i=1}^{N}\sigma_i}$$

#### 5. 状态跃迁

衡量整体结构的稳定性，总体状态变化的概率，及Markov Matrix的对角线因素总和与完全没有变动状态的比值。

$$\tau =1-\frac{\sum_{i=1}^NP_{ii}}{Nclass}$$

具体实例参考*Rey S.J., Ye X. (2010) Comparative Spatial Dynamics of Regional Systems. In: Páez A., Gallo J., Buliung R., Dall'erba S. (eds) Progress in Spatial Analysis. Advances in Spatial Science (The Regional Science Series). Springer, Berlin, Heidelberg. https://doi.org/10.1007/978-3-642-03326-1_20*