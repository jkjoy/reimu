---
pubDate: "2024-01-08T11:26:00Z"
title: "使用Vercel做反向代理"
keywords:
  - 分享
tags:
  - vercel
  - 说说
description: "本文介绍了使用Vercel做反向代理的具体步骤。首先需要安装nodejs和vercel-cli，然后登录vercel账号。接着新建一个web.json文件，并编辑其中的路由规则。最后使用vercel命令部署并启动反向代理服务。"
draft: "false"
---

## 准备工作

### 自行安装

- nodejs

## 具体步骤

### 安装vercel-cli

```bash
npm i -g vercel
```

###  登录

```bash
vercel login
```

### 新建

新建一个web.json文件并编辑以下内容

```json
{
    "version": 2,
    "routes": [
      {"src": "/(.*)","dest": "https://class.imsun.org"}
    ]
}
```

###  部署

```bash
vercel -A web.json --prod
```