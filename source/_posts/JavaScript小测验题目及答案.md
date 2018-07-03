---
title: JavaScript小测验题目及答案
date: 2018-07-03 18:51:16
tags: 
 - JavaScript
---
# 小测验题目及答案

## 1 What is printed in the console?

```JavaScript
  var foo = function foo() {
    console.log(foo === foo);  
  };
  foo();
  // true
```

---

## 2 What does the above

```JavaScript
  function aaa() {
    return
    {
      test: 1
    };
}
 typeof aaa() // underfined
```

---

## 3 What is the result?

```JavaScript
  Number("1") - 1 == 0;
  // true
```

---

## 4 3 What is the result?

```JavaScript
  (true + false) > 2 + true;
  // false
```

---

## 5 What is?

```JavaScript
  function bar() {
    return foo;
    foo = 10;
    function foo() {}
    var foo = '11';
}
typeof bar()
// function
```

---

## 6 What is the result?

```JavaScript
 "1" - - "1";
 // 2
```

---

## 7 What is the order of values?

```JavaScript
var x = 3;

var foo = {
    x: 2,
    baz: {
        x: 1,
        bar: function() {
            return this.x;
        }
    }
}

var go = foo.baz.bar;

alert(go());
alert(foo.baz.bar());
// 3, 1
```

---

## 8 What is the result?

```JavaScript
  new String("This is a string") instanceof String;
  // true
```

---

## 9 What is the result?

```JavaScript
  "This is a string" instanceof String;
  // false
```

---

## 10 What is the result?

```JavaScript
  [] + [] + 'foo'.split('');
  /*
  [] + [] = ""
  'foo'.split('') f,o,f
   "f,o,o"
  */
```

---

## 11 What is the result?

```JavaScript
  new Array(5).toString();
  //new Array(5) [,,,,]
  // toString() ",,,,"
```

---

## 12 What is the result?

```JavaScript
  var myArr = ['foo', 'bar', 'baz'];
  myArr.length = 0; // 清空myArr
  myArr.push('bin'); 
  console.log(myArr); // bin
```

---

## 13 What is the result?

```JavaScript
  String('Hello') === 'Hello'; // true
  
  //String('Hello') 输出 Hello
```

---

## 14 What is printed on the console?

```JavaScript
  var x = 0;
function foo() {
    x++;
    this.x = x;
    return foo;
}
var bar = new new foo;
console.log(bar.x);
// underfined
```

---

## 15 What is the result?

```JavaScript
  var bar = 1,
    foo = {};

foo: {
    bar: 2;
    baz: ++bar;
};
foo.baz + foo.bar + bar;
// NAN
```

---

## 16 What is the result of console.log?

```JavaScript
  var myArr = ['foo', 'bar', 'baz'];
  myArr[2];
  console.log('2' in myArr);
  '2' in 隐式转换 变成 number的 2
// true
```

---

## 17 What value is alerted?

```JavaScript
  var arr = [];
  arr[0]  = 'a';
  arr[1]  = 'b';
  arr.foo = 'c';
  alert(arr.length);
  // arr = ['a', 'b', foo:'c']
  // lngth = 2
```

---

## 18 What is the result?

```JavaScript
  10 > 9 > 8 === true;

  // 10 > 9 = true
  // true = 1 > 8 = false
  //false === true
  // false
```

---

## 19 What value is alerted?

```JavaScript
  function foo(a, b) {
    arguments[1] = 2;
    alert(b);
  }
  foo(1);
  // underfined
```

---

## 20 What is the result?

```JavaScript
  NaN === NaN;
  // NaN not a number
  // false
```

---
