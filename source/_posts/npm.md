---
title: npm设置
tags: 
  - npm
# 文章摘要渲染方式: 为 true 时将渲染为 html，否则为文本
excerpt_render: false
# 截断长度
excerpt_length: 50
# 文字正文页链接文字
excerpt_link: 阅读全文...
---


## npm 更换源地址
### 查看当前源地址
```
npm config get registry
```
### 更换源地址
```
npm config set registry https://registry.npm.taobao.org/
```
## 关于chromedriver下载失败的方法
```
npm install chromedriver --chromedriver_cdnurl=http://cdn.npm.taobao.org/dist/chromedriver
```
## 升级nodejs和npm到最新版本
### 第一步,先查看本机node.js版本
```
node -v
```
### 第二步,清除node的cache
```
sudo npm cache clean -f
```
####第三步,安装n工具,用来管理node.js版本
```
sudo npm install -g n
```
### 第四步,安装最新版本的node.js
```
sudo n stable
```
### 第五步,查看本机的node.js版本
```
node -v
```
#### 第六步，更新npm到最新版：
```
sudo npm install npm@latest -g
```
### 第七步,验证
```
node -v
npm -v
```

