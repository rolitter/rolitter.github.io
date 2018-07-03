---
title: JavaScript随手记
tags: 
  - JavaScript
---
## js 0.1+0.2=!0.3
引入`bignumber.js`
```JavaScript
import {BigNumber} from 'bignumber.js'
    proEquals (value) { //乘100
      let x = new BigNumber(value)
      return Number(x.multipliedBy(100))
    },
    proDivision (value) { //除100
      let x = new BigNumber(value)
      return Number(x.div(100))
    }
```
## 金额 千分符
``` JavaScript
function numverWithCommas(num) {
  // 正则解释: 匹配到 \B(非单词边界)后, 后面要匹配到 (\d{3})+(?!\d)
  // (\d{3})+ 至少匹配到一次或多次三个数字
  // (?!\d) 同时后面不是数字的话, 就匹配.
  // 注意, 后面的(?=)那一段代码只是判断的规则, 匹配到后只替换掉\B
  // 这是一个很巧妙的方法 ..
  return num.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',')
}
```
## 随机数
``` JavaScript
function random (min, max) {
  return Math.round(Math.random() * (max - min) + min)
}
```
## 字符串转数字
```JavaScript
  ['1.1', '4566', '3e300'].map(Number) //[1.1, 4566, 3e+300]
```
## 月份日期转星座
``` JavaScript
/**
 * 根据生日的月份和日期，计算星座。
 * @param {String} m - 月份
 * @param {String} d - 日期
 * �@desc 返回星座名
 */
function getAstro(m,d){
  return "魔羯水瓶双鱼牡羊金牛双子巨蟹狮子处女天秤天蝎射手魔羯".substr(m*2-(d<"102223444433".charAt(m-1)- -19)*2,2);
}
```