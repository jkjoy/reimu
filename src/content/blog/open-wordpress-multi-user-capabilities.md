---
pubDate: "2016-12-20T05:48:00Z"
title: "开启wordpress多用户功能"
keywords:
  - 笔记
tags:
  - wordpress
description: "本文介绍了如何开启WordPress的多用户功能。首先需要编辑根目录下的wp-config.php文件，在代码define('WPLANG', 'zh_CN');之后添加代码define('WP_ALLOW_MULTISITE', true);。添加完成后，刷新后台页面，就可以在工具菜单中看到添加网络(Network)选项。"
draft: "false"
---

<p>编辑根目录的 wp-config.php 文件，找到以下代码：</p>
<blockquote>define ('WPLANG', 'zh_CN');</blockquote>
<p>在其之后添加以下代码：</p>
<blockquote>define('WP_ALLOW_MULTISITE', true);</blockquote>
<p>这个时候刷新后台页面，工具菜单中已经有添加网络 (Network) 选项。</p>