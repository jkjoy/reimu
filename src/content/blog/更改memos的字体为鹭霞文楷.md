---
pubDate: "2023-12-14T06:58:00Z"
title: "更改memos的字体为霞鹜文楷"
keywords:
  - 分享
tags:
  - memos
  - 说说
description: "文章介绍了如何通过更改memos的自定义样式来将字体改为霞鹜文楷。由于跨域问题导致一些图标和字体无法正常显示，作者决定自建一个霞鹜文楷的CDN，并提供了相应的代码供读者复制粘贴使用。"
draft: "false"
---

<p>通过memos的自定义样式更改字体为霞鹜文楷</p>
<p>由于cdn.staticfile.org出现了跨域的问题导致很多图标和字体无法正常显示.</p>
<p>加上ucloud买了一年100G的CDN流量.</p>
<p>自己反正也很少用,就自建一个霞鹜文楷的CDN</p>
<p>把以下代码复制粘贴进memos的自定义样式中保存即可.</p>
<pre><code class="language-css">@import &#039;//cdn.09j.cn/lxgw-wenkai-webfont/style.css&#039;;
body {
font-family: &quot;LXGW WenKai&quot;, sans-serif;
}</code></pre>
<p>&nbsp;</p>