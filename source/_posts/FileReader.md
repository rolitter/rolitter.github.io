---
title: 使用FileReader实现图片上传预览
tags: 
  - JavaScript
  - FileReader
---

# 使用FileReader实现图片上传预览

## html
```html
<label for="upload" class="label">选择图片
  <input type="file" id="upload" @change='selectImage' hidden="" accept="image/*">
</label>
```
## JavaScript
```javascript
selectImage(event) {
  let reader = new FileReader();
  let file = event.target.files[0];
  reader.readAsDataURL(file);
  reader.onloadend = function() {
   // 把reader.result赋img便签即可进行预览
    let imgBase64 = reader.result.replace(/^.*?,/, '')// 清除base64 前缀
  }
}
```
