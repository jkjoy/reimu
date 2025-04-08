---
pubDate: "2018-10-19T04:47:00Z"
title: "一键部署X-UI面板"
keywords:
  - 分享
tags:
  - 部署
description: "X-UI面板是一个功能强大的系统状态监控工具，支持多用户多协议，网页可视化操作。它支持多种协议，包括vmess、vless、trojan、shadowsocks等，并且可以配置更多传输配置。此外，它还提供流量统计、限制流量和到期时间的功能，可以自定义xray配置模板。面板支持https访问，并且可以一键申请和自动续签SSL证书。更多高级配置项可以在面板中找到。安装和升级非常简单，只需执行一行命令即可。项目地址为https://github.com/vaxilu/x-ui。对于国内环境，可以通过下载install.zip文件或执行另一条命令进行安装。"
draft: "false"
---

### 功能介绍
- 系统状态监控
- 支持多用户多协议，网页可视化操作
- 支持的协议：vmess、vless、trojan、shadowsocks、dokodemo-door、socks、http
- 支持配置更多传输配置
- 流量统计，限制流量，限制到期时间
- 可自定义 xray 配置模板
- 支持 https 访问面板（自备域名 + ssl 证书）
- 支持一键SSL证书申请且自动续签
- 更多高级配置项，详见面板

### 安装&升级

```BASH
bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh)
```

### 项目地址
https://github.com/vaxilu/x-ui

### 适合国内环境
 [install.zip][1]
或执行
```sh
bash <(curl -Ls https://down.asbid.cn/x-ui/install.sh)
```


  [1]: https://blogcdn.asbid.cn/2023/07/27/1690426036.zip