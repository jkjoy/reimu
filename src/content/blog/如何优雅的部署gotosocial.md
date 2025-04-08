---
pubDate: "2023-09-11T01:25:00Z"
title: "如何优雅的部署Gotosocial"
keywords:
  - 分享
tags:
  - Gotosocial
description: "GoToSocial是一个使用Golang编写的ActivityPub社交网络服务器，它提供了一个轻量级、安全的联邦社交网络入口，用户可以保持联系、发布和分享内容。GoToSocial强调用户的隐私和自由，不会跟踪用户的行为或收集数据用于广告展示。部署GoToSocial可以通过使用docker-compose进行，配置文件中需要设置一些环境变量和存储方式。运行后可以创建用户并赋予管理员权限。最后，可以通过反向代理将GoToSocial部署到指定的域名上。客户端可以通过https://login.ima.cm访问，演示可以通过https://ima.cm访问。"
draft: "false"
---

## Gotosocial是什么

GoToSocial 是一个使用 Golang 编写的 ActivityPub 社交网络服务器，它是一个轻量级、安全的联邦社交网络入口，可让用户保持联系、发布和分享图片、文章等内容。GoToSocial 强调用户的隐私和自由，不会跟踪用户的行为，也不会为了向用户展示广告而收集他们的数据。 使用 GoToSocial 可以让用户进入联邦社交网络的世界，联邦网络是一种基于协议的社交网络结构，它允许用户从一个社交网络实例互相跟随、交流和分享内容。这种结构可以让用户自由选择社交网络平台，同时避免某个平台垄断市场。用户可以在不同的实例之间进行跟随和互动，这样就可以更好地保护用户的隐私和自由。

## 部署方式

### 使用docker-compose部署

创建安装目录并更改权限

```bash
mkdir -p /var/www/gotosocial/data && cd /var/www/gotosocial && chown 1000:1000 ./data
```

### 配置 `docker-compose.yaml` 文件

```yaml
version: "3.3"

services:
  gotosocial:
    image: superseriousbusiness/gotosocial:latest
    container_name: gotosocial
    networks:
      - gotosocial
    environment:
      GTS_HOST: social.example.com
      GTS_DB_TYPE: sqlite
      GTS_DB_ADDRESS: /gotosocial/storage/sqlite.db
      GTS_LETSENCRYPT_ENABLED: "false"
      GTS_STORAGE_BACKEND: "s3"
      GTS_STORAGE_S3_BUCKET: "BUCKET名称"
      GTS_STORAGE_S3_ENDPOINT: "#S3 API"
      GTS_STORAGE_S3_ACCESS_KEY: "#api-tokens"
      GTS_STORAGE_S3_SECRET_KEY: "#api-tokens"
      GTS_STORAGE_S3_PROXY: "true"
    ports:
      - "127.0.0.1:8080:8080"
    volumes:
      - ./data:/gotosocial/storage
    restart: "always"

networks:
  gotosocial:
    ipam:
      driver: default
```

支持S3存储

### 运行

```bash
docker compose up -d
```

### 创建用户

```bash
docker exec -it gotosocial ./gotosocial admin account create --username admin --email YOUR@EMAIL.COM --password  SOME_VERY_GOOD_PASSWD ;
```

自行更改`用户名``密码``邮箱地址`

把`admin`改成自己需要的用户名

### 增加管理员权限

```bash
docker exec -it gotosocial ./gotosocial admin account promote --username admin
```

## 反向代理

反代`127.0.0.1:8080`即可 此处就不赘述了.

## 客户端

[https://login.ima.cm](https://login.ima.cm)

* 大家都可以使用

## 演示

[https://ima.cm](https://ima.cm)