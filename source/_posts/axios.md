---
title: axios使用总结
tags: 
  - axios
  - JavaScript
  - vue
# 文章摘要渲染方式: 为 true 时将渲染为 html，否则为文本
excerpt_render: false
# 截断长度
excerpt_length: 50
# 文字正文页链接文字
excerpt_link: 阅读全文...
---

## axios挂在vue上

```javascript
import axios from 'axios'
Vue.prototype.$http = axios
```
在vue文件中使用
```javascript
this.$http.get('http://www.baidu.com')
  .then((res) => {
  })
```

## axios 请求携带头部
```javascript
import axios from 'axios';
import { getToken } from '@/utils/auth'

const service = axios.create();

service.defaults.timeout = 5000;
service.defaults.baseURL = 'http://127.0.0.1:8080'


service.interceptors.request.use(
  config => {
    let token = getToken()
     if (token) {
       config.headers.Authorization = token
     }
    return config
  },
  error => {
    return Promise.reject(error)
  }
);

service.interceptors.response.use(
  response => {
    return response
  },
  error => {
    return Promise.resolve(error.response)
  }
)
export default service
```

