---
pubDate: "2022-07-27T10:39:00Z"
title: "Linux下本地安装包命令"
keywords:
  - 分享
tags:
  - linux
description: "在Linux系统中，安装本地安装包有不同的命令。在CentOS系统中，可以使用\"sudo yum localinstall file.rpm\"命令来安装RPM安装包。而在Ubuntu系统中，可以使用\"sudo dpkg -i 安装包名称.deb\"命令来安装deb安装包。"
draft: "false"
---

<h2>centos下安装RPM安装包</h2><pre><code class="lang-bash">sudo yum localinstall file.rpm</code></pre><h2>ubuntu下安装deb安装包</h2><pre><code class="lang-bash"> sudo dpkg -i 安装包名称.deb</code></pre>