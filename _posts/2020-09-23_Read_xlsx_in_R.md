---
title: Read xlsx in R
tags:
- R
- xlsx
desc: 
layout: post
---

在R中读取xlsx的方法很多，最常用的是`xlsx`包，这个包依赖JAVA的库，因此需要安装JAVA后才可以使用。具体步骤如下

1. 安装JAVA

https://www.java.com/zh_CN/download/

2. 安装`xlsx`包

安装完成后，引用时出现错误

> 错误: package or namespace load failed for ‘xlsx’:    
> loadNamespace()里算'rJava'时.onLoad失败了，详细内容：    
>  调用: inDL(x, as.logical(local), as.logical(now), ...)    
>  错误: 无法载入共享目标对象‘C:/Users/****/Documents/R/win-library/4.0/rJava/libs/x64/rJava.dll’：:    
> LoadLibrary failure:  %1 不是有效的 Win32 应用程序。

错误原因

操作系统的版本是win10, 64bit，我系统安装的jdk1.8,是32bit的，而使用的R版本是64位的；R版本与jre版本不兼容导致；

解决办法之一：     
更改R版本位32位的即可！     
RStudio中，Tools –> Global Options –General –> R version Change一下（如果安装R时没勾选32bit的，就重新安装一下）     

解决办法之二：    
设置*JRE*路径即可解决      
> Sys.setenv(JAVA_HOME='D:/jdk1.6.0_45/jre')

3. 使用

> library(xlsx)    
> dat <- read.xlsx("data.xlsx", sheetName = "Sheet1", encoding = 'UTF-8')

若表格中含有中文，编码一定要设置为`UTF-8`。

参考
https://blog.csdn.net/weixin_41929524/article/details/81911295

https://blog.csdn.net/hongweigg/article/details/49892455

https://blog.csdn.net/huangyouyu523/article/details/77951857