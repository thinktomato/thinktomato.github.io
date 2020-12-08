---
title:在latex中插入参考文献
tag:
- latex
- biblatex
desc:
layout
---

latex中使用内置的宏插入参考文献时格式很难看，因此使用[caspervector](https://gitea.com/CasperVector/biblatex-caspervector/src/branch/master).

外部宏的引用我现在还不知道怎么办呢，笨的方法是把里边的文件放到工作目录中。

遇到的问题是*插入参考文献序号都是[0]*，实验了很多种方法，原来是`\nocite{*}` 语句的问题，把它放在`\printbibgraphy` 前面，文献前面的序号是正常的。

补：
参考文献外部宏的方法如下：
To use the styles place:
1) the .bbx files in: <HOME>/texmf/tex/latex/biblatex/bbx/
2) the .cbx files in: <HOME>/texmf/tex/latex/biblatex/cbx/
3) the .lbx files in: <HOME>/texmf/tex/latex/biblatex/lbx/
Alternatively, place the .bbx, .cbx and .lbx files in your working directory
or in:
<TEXMFLOCAL>/tex/latex/biblatex-contrib/biblatex-philosophy.
In this case remember to refresh the file name database.
参考：https://www.ctan.org/tex-archive/macros/latex/contrib/biblatex-contrib/biblatex-philosophy