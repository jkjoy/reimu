---
pubDate: "2022-07-29T15:33:00Z"
title: "macOS一键安装homebrew国内镜像"
keywords:
  - 分享
tags:
  - 分享
  - 说说
description: "本文介绍了如何在macOS上一键安装homebrew国内镜像。由于墙的原因，官方提供的一键安装可能无法成功，因此作者找到了一个国内镜像的一键安装脚本，并提供了具体的安装命令。"
draft: "false"
---

<p>官方给出的一键安装由于墙的原因可能无法安装成功。<br />所以找到了一个国内镜像的一键安装脚本</p><pre><code class="lang-bash">/bin/zsh -c &quot;$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)&quot;</code></pre>