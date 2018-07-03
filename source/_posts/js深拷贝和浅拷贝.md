---
title: js深拷贝和浅拷贝
tags: 
  - JavaScript
---

## es6
es6拷贝,不能深拷贝
```javascript
let arr = {t: 1, p: 'gg'}
let brr= Object.assign({}, arr);
console.log(brr) //{t: 1, p: 'gg'}
```
## JSON
简单实现深拷贝的方法，当然，有一定限制，如下：
```javascript
const obj1 = JSON.parse(JSON.stringify(obj));
```
思路就是将一个对象转成json字符串，然后又将字符串转回对象。这个方法当有属性是undefined或null的时候会被移除掉。
而且不能拷贝function.

## Lodash
使用Lodash 的_.defaultsDeep方法可以得到深拷贝的合并。
```javascript
var array = [1];
var other = _.concat(array, 2, [3], [[4]]);
 
console.log(other);
// => [1, 2, 3, [4]]
 
console.log(array);
// => [1]
```
[Lodash中文文档](http://www.css88.com/doc/lodash)