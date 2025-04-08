---
pubDate: "2022-08-12T16:52:00Z"
title: "centos7 ssh连接慢的解决方法"
keywords:
  - 笔记
tags:
  - SSH
description: "本文介绍了解决CentOS 7 SSH连接慢的方法。首先，通过编辑sshd_config文件，将UseDNS的注释符号#去掉，并将其值改为no。然后，将GSSAPIAuthentication的值改为no。最后，保存退出并重启sshd服务。这些操作可以提高SSH连接的速度。"
draft: "false"
---

<pre><code class="lang-bash">vim /etc/ssh/sshd_config</code></pre><p>按i编辑插入<br />找到<br /><code>UseDNS</code>去掉前面的#号 改为 no</p><p><code>GSSAPIAuthentication</code> 改为 no</p><p>然后<code>：wq </code>保存退出</p><pre><code class="lang-bash">systemctl restart sshd</code></pre><p>重启</p>