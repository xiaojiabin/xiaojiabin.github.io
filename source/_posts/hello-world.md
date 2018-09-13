---
title: vue项目如何引入ElementUI(全局引入和按需引入)
author: 闫先森 
avatar: /images/favicon.png 
authorDesc: 充满正能量的骚年 
categories: 前端
tags: 
  - javascript 
---

**摘要:**本篇文章主要是在官网上通过学习,参照官网写的一点小心得,仅供参考!

## 通过npm安装element-ui模块

`npm i element-ui -S`

## 在代码中引入
 #### 完整引入
在main.js中写入以下内容
  ```
import Vue from 'vue';
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';//样式文件一定要引入
import App from './App.vue';

Vue.use(ElementUI);

new Vue({
  el: '#app',
  render: h => h(App)
});
```
#### 按需引入
首先，安装 babel-plugin-component:

`npm install babel-plugin-component -D`

然后，将 .babelrc 修改为：
```
{
  "presets": [
    ["env", {
      "modules": false,
      "targets": {
        "browsers": ["> 1%", "last 2 versions", "not ie <= 8"]
      }
    }],
    "stage-2"
  ],
  "plugins": [
    [
      "component",
      {
        "libraryName": "element-ui",
        "styleLibraryName": "theme-chalk"
      }
    ]
  ]
}
```
**注意:**这里我没有完全按照官网里面的改,区别可以看[Element官网](http://element-cn.eleme.io/#/zh-CN/component/quickstart).

接下来，如果你只希望引入部分组件，比如 Select，那么需要在 main.js 中写入以下内容：
```
import Vue from 'vue';
import { Select,Option } from 'element-ui';
import App from './App.vue';

Vue.use(Select)
Vue.use(Option)
  
new Vue({
  el: '#app',
  render: h => h(App)
});
```
**注意:**当你引入Select组件的时候,一定要引入Option组件,否则Select的下拉框是不会显示的.

到这里,你就可以在你的项目中使用Element组件了.如果有什么问题,可以一块交流下哦!

