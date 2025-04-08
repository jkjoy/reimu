---
pubDate: "2019-04-10T17:52:00Z"
title: "Ubuntu如何更改显示器分辨率并永久保存所设置的分辨率"
keywords:
  - 笔记
tags:
  - Ubuntu
description: "本文介绍了在Ubuntu系统中如何更改显示器分辨率并永久保存所设置的分辨率。通过在终端执行一系列命令，包括使用\"cvt\"命令生成新的分辨率模式，使用\"xrandr\"命令添加新的分辨率模式并将其应用到显示器上。然后，通过编辑\".profile\"文件将这些命令添加到系统启动时自动执行的脚本中。最后，重启系统并使用\"xrandr\"命令查看已设置的分辨率。"
draft: "false"
---

<p>终端执行命令行如下</p><pre><code>cvt 1920 1080
xrandr –newmode 1920x1080_60 173.00 1920 2048 2248 2576 1080 1083 1088 1120 -hsync +vsync
xrandr –addmode VGA-0 1920x1080_60
xrandr –output VGA-0 –mode 1920x1080_60
</code></pre><p>然后执行<br /><code>sudo gedit .profile</code><br />把以上的命令行复制粘贴到最后即可<br />保存 重启系统，使用“<code>xrandr</code>”命令查看<br /><img src="https://xy07-1251893119.costj.myqcloud.com/2019/04/10/465359891.png" alt="2019-04-10 18-03-21 的屏幕截图.png" title="2019-04-10 18-03-21 的屏幕截图.png"></p>