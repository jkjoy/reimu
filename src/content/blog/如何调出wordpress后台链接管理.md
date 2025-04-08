---
pubDate: "2018-07-04T13:00:00Z"
title: "如何调出wordpress后台链接管理"
keywords:
  - 笔记
description: "本文介绍了如何调出WordPress后台的链接管理功能。通过在当前主题的functions.php文件中添加一段代码，即可启用链接管理功能。保存并刷新后，链接管理功能就会出现在后台中。"
draft: "false"
---

<p>很多朋友新安装了wordpress之后发现后台没有链接表管理
解决方法很简单，在当前的主题下修改模板函数 (functions.php)</p>
<pre><code class="language-php  line-numbers">//链接管理
add_filter( 'pre_option_link_manager_enabled', '__return_true' );
</code></pre>
<p>添加此段代码在&lt;?php后
保存刷新即可</p>
<img src="https://i.loli.net/2018/07/04/5b3cc70bb080b.jpg" alt="blob.jpg" />
<p>是不是出现了呢</p>