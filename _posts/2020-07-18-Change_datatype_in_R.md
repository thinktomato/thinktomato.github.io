---
title: R语言将数据框中字符类型转换成数字类型
tags:
- R
- as.numerric
- lapply
desc: Change charactors in data.frame into numeric in R
layout: post
---

1. 在R中，导入CSV文件时，列的数据类型要求一致。由于列中含有非数字导致读入R时，数字类型自动转换成了字符类型。这时需要将data.frame中字符类型转换成数字类型进行运算。利用lapply函数将每一列进行转换，再将最后结果重新转换成data.frame.

```
data <- as.data.frame(lapply(data, as.numeric))
```

2. *stringAsFator = FALSE* 参数的应用    
   (1)这一参数挺有用的，读入CSV时，添加该参数可以防止，读入的数据自动转换成factor类型。
   (2)data.frame转置时自动转换为matrix格式，在重新转换成data.frame格式时，添加该参数可以防止将数据转换成factor。

   ```
   #初始data为data.frame
   data <- t(data) #data转换为matrix
   data <- as.data.frame(data, strignAsFactor = FALSE) #防止dataframe中数据转换成factor。
   ```