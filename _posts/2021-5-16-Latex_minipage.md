---
latex分栏显示
tag:
- Latex; minipage;
desc:
layout
---
1. latex分栏显示-左图右表

在figure环境里嵌套minipage，且两个minipage之间没有空行，若空行则表示回车，两边内容不一样高了。

```
\begin{figure}
    \bigin{minipage}[b]{.5\linewidth}
        \centerting
        \includegraphics[]{}
        \caption
    \end{minipage}%
    \bigin{minipage}[b]{.5\linewidth}
        \centering
        \begin{tabular}[ll]
        
        \end{tabular}
    \end{minipage}
\end{figure}
```

2. 控制表格大小

表格过宽或过窄，会很难看，需要调整表格宽度，使用的命令为`\setlength{\tabcolsep}{7mm}{XXXX}`(按页面调整宽度), 或者`\resizebox{\textwidth}{15mm}{XXX}`(按内容调整)

3. 批量注释

(1) 使用宏包`\usepackage{verbatim}`，使用命令`\begin{comment}`和`\end{comment}`

(2) 或者使用`\iffalse ... \fi`

参考：

https://www.zhihu.com/question/29803796

https://blog.csdn.net/wbl90/article/details/52597429

https://www.jianshu.com/p/f5cee88e3218