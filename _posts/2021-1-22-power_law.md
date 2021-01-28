---
title:回归过程中的数据标准化
tag:
- pareto distribution; zipf's law; power law
desc:
layout
---

## 1. 幂定律(Power Law)

指满足如下多项式关系，且表现出**标度不变性**：

$$f(x) = ax^k + o(x^k)$$

其中$o(x^k)$ 为*渐进微小函数*。

## 2. 帕累托分布(Patero Distribution)

是一种*幂定律*分布，其概率密度函数为：

$$
p(x) =
\begin{array}
   0, & if x < x_{min}\\
   \frac{kx^k_{min}}{x^{k+1}}, & if x > x_{min} 
\end{array}
$$

## 3. 齐夫定律(Zipf's Law)

齐夫定律可看作帕累托分布的离散概率分布，其最初用来描述自然语言语料库中单词出现频率与单词频率排名之间的关系“*在自然语言的语料库里，一个单词出现的频率与它在频率表里的排名成反比。所以，频率最高的单词出现的频率大约是出现频率第二位的单词的2倍，而出现频率第二位的单词则是出现频率第四位的单词的2倍。*”

这个定律被作为任何与**幂定律**概率分布有关的事物的参考。

齐夫定律很容易用点阵图观察，坐标分别为排名和频率的自然对数（log），如果所有的点接近一条直线，那么它就遵循齐夫定律。

以上内容皆参考维基百科：
1. https://zh.wikipedia.org/wiki/%E5%86%AA%E5%AE%9A%E5%BE%8B
2. https://zh.wikipedia.org/wiki/%E5%B8%95%E7%B4%AF%E6%89%98%E5%88%86%E5%B8%83
3. https://zh.wikipedia.org/wiki/%E5%B8%95%E7%B4%AF%E6%89%98%E6%B3%95%E5%88%99
4. https://zh.wikipedia.org/wiki/%E9%BD%8A%E5%A4%AB%E5%AE%9A%E5%BE%8B

