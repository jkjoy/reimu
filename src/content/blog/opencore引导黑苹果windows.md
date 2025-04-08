---
pubDate: "2021-10-07T03:27:00Z"
title: "解决opencore引导黑苹果&amp;Windows双系统蓝屏的问题"
keywords:
  - 笔记
description: "解决opencore引导黑苹果和Windows双系统蓝屏的问题的方法是打开config.plist文件，找到booter---Quirks---SyncRuntimePermissions的值，将其改为true即可。"
draft: "false"
---

<p><del>最好的办法就是使用mod版本的opencore</del>
开机蓝屏报错的解决办法</p>
<p>打开config.plist查找<span style="color:red;"></span></p>
<p><code>booter</code>---<code>Quirks</code>---<code>SyncRuntimePermissions</code>的值改成<span style="color:red;">true</span>即可。</p>