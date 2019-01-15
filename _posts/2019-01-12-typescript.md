---
layout: post
title:  typescript
date:   2019-01-12 09:00:00 +0800
categories: engineering
---
typescript 和 js
### 准备调试环境
ng 产生project后，在main.ts 中进行。
### function declare 和function expression
浏览器支持 function hoisting。 所以declare的可以先被浏览器识别。
### default para , rest para
let myFunc = function (name, weather = "raining")
let myFunc = function (name, weather, ...extraArgs) {
### function 也可以作为参数
### 箭头函数
三个部分，参数， 箭头， 函数主体
### let and var
var scope是定义的函数内。
let 定义的region内  
尽量使用const 和let
### function 内的funciton
inner function 可以访问外部函数的变量和参数。
### spread operator
使用 。。。扩展数组
let myArray = [100, "Adam", true];
let otherArray = [...myArray, 200, "Bob", false];

### properties in typescript
在构造函数里进行属性定义。
