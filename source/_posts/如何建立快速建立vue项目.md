---
title: 如何快速创建vue项目
author: 闫先森
avatar: /images/favicon.png
authorDesc: 充满正能量的骚年
date: 2018-09-14 09:40:03
categories: 前端
tags: 
  - Vue
---

**摘要:**本篇文章主要用于记录如何快速的生成vue项目

## 前提是先安装好node
  在[node官网](https://nodejs.org/en/download/)选择相对应的版本进行下载,按照提示进行每一步的操作即可.

  **如果网速过慢,可以考虑安装国内的淘宝镜像cnpm(可忽略)**
### 安装cnpm
  `npm install -g cnpm --registry=https://registry.npm.taobao.org`

## 安装webpack
  `npm install webpack -g`

## 全局安装Vue脚手架
  `npm install -g vue-cli`
 **使用脚手架创建新项目;要先使用cd 命令打开将要放置项目的目录**

## 初始化项目,也就是创建项目
  `vue init webpack my-project`
  **my-project为项目的名称,可根据自己用不同的名字,接下来会有项目的配置,可根据自己的需求自行配置**

## 安装项目依赖
  在项目根目录下执行以下代码
  `npm install`

## 启动项目
  `npm run dev`


这时你就能看到一个vue的演示例子了,剩下的就剩下写代码了