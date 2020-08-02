---
title: R启动时自动加载包编辑
tags:
- R
- Rprofile
desc: When R start, we edite the auto-loading libraty in Rprofile
layout: post
---

删除了某个R包后，每次启动R都提示某某包加载失败，没有找到某R包。删除R启动时自动加载包就可以了。    
用 `file.edit(".Rprofile")` 打开Rprofile文件，删除加载该R包的语句即可。

