---
title: 通过for循环来取出两个数组不同的值
author: 闫先森
avatar: /images/favicon.png
authorDesc: 充满正能量的骚年
date: 2018-09-14 10:31:31
categories: 前端
tags: 
  - javascript
---

**摘要:**本文记录于很久以前的学习笔记,仅限个人学习与记录

```
var arr1 = [ {"id": 1  },{"id": 2}];
var arr2 = [ {"id": 1,"Name": "t1 " }, {"id": 2,"Name": "t2"}, {"id": 3 ,"Name": "t3 "}];
var result = [];
for(var i = 0; i < arr2.length; i++){
    var obj = arr2[i];
    var num = obj.id;
    var isExist = false;
    for(var j = 0; j < arr1.length; j++){
        var n = arr1[j].id;
        if(n == num){
            isExist = true;
            break;
        }
    }
    if(!isExist){
        result.push(obj);
    }
}
console.log(result); //result:{id: 3, Name: "t3 "}
```