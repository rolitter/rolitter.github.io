---
title: JavaScript简写
tags: 
  - JavaScript
---

## 定义初始值
```
const variable2 = variable1  || 'abc';
```
---
## 箭头函数

普通写法
```
  function sayHello(name) {
    console.log('Hello', name);
  }
```
简写
```
  const sayHello = name => console.log('Hello', name)
```
---
## 隐式返回简写

普通写法
```javascript
  function calcCircumference(diameter) {
    return Math.PI * diameter
  }
```
简写
```javascript
  calcCircumference = diameter => (Math.PI * diameter)
  //函数名=接受值=> 返回值
```
---
## 展开运算符简写
普通写法
```javascript
// 拼接数组
const odd = [1, 3, 5];
const nums = [2 ,4 , 6].concat(odd);
 
// 克隆数组
const arr = [1, 2, 3, 4];
const arr2 = arr.slice()
```
简写
```javascript
// 拼接数组
const odd = [1, 3, 5 ];
const nums = [2 ,4 , 6, ...odd];
console.log(nums); // [ 2, 4, 6, 1, 3, 5 ]
 
// 克隆数组
const arr = [1, 2, 3, 4];
const arr2 = [...arr];
```
---