---
title: base64中文不兼容解决方案
tags: 
  - JavaScript
  - base64
---

# base64中文不兼容解决方案

## 编码
``` JavaScript
window.btoa(encodeURIComponent(str))
// or
window.btoa(unescape(encodeURIComponent( str )))
```
# 解码
```JavaScript
decodeURIComponent(window.atob(str))
// or
decodeURIComponent(escape(window.atob( str )))
```

