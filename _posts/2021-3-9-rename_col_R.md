---
title:修改tibble的列名 
tag:
- tidyverse; select; coloum
desc:
layout
---

## 修改tibble列名

Data中三列a, b, c，将列名b修改为bb

```
Data %>%
  select(bb = b)
```
```
Data %>%
   rename(bb = b)
```

## 调整tibble列的顺序

将a, b, c, 列顺序修改为c, b, a

```
Data %>%
   select(c, b, a)
```
参考：
1. https://www.cnblogs.com/Mao1518202/p/12216950.html