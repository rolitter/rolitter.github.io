---
title: hexo命令
date: 2017-07-07 11:51:16
tags: 
  - hexo
---

<i class="icon icon-book icon-lg"></i>
hexo命令
## 简写

### 新建文章

``` bash
$ hexo n "My New Post"==hexo new "My New Post"
```

详细信息: [Writing](https://hexo.io/docs/writing.html)

### 启动服务预览

``` bash
$ hexo s == hexo server
```

详细信息: [Server](https://hexo.io/docs/server.html)

### 生成

``` bash
$ hexo g == hexo generate
```

详细信息: [Generating](https://hexo.io/docs/generating.html)

### 部署

``` bash
$ hexo d == hexo deploy
```

详细信息: [Deployment](https://hexo.io/docs/deployment.html)

## 服务器

```
$ hexo server #Hexo 会监视文件变动并自动更新，您无须重启服务器。
$ hexo server -s #静态模式
$ hexo server -p 5000 #更改端口
$ hexo server -i 192.168.1.1 #自定义 IP
$ hexo clean #清除缓存 网页正常情况下可以忽略此条命令
$ hexo g #生成静态网页
$ hexo d #开始部署
```
## 监视文件变动

```
$ hexo generate #使用 Hexo 生成静态文件快速而且简单
$ hexo generate --watch #监视文件变动
```

## 完成后部署
```
两个命令的作用是相同的
$ hexo generate --deploy
$ hexo deploy --generate

```
### 简写
```
$ hexo deploy -g
$ hexo server -g
```

## 草稿
```
$ hexo publish [layout] <title>
```

## 模版
```
$ hexo new "postName" #新建文章
$ hexo new page "pageName" #新建页面
$ hexo generate #生成静态页面至public目录
$ hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）
$ hexo deploy #将.deploy目录部署到GitHub

$ hexo new [layout] <title>
$ hexo new photo "My Gallery"
$ hexo new "Hello World" --lang tw
```

## 设置文章摘要

```
$ 以上是文章摘要 <!--more--> 以下是余下全文
```

