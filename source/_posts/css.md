---
title: css常用知识点
tags: 
  - css
---

## div设置display:inline
```
block元素设置为inline,不能再设置该元素的height和width,margin-top,margin-bottom,float
```
## vw
```scss

//iPhone 6尺寸作为设计稿基准
$vw_base: 375; 
@function vw($px) {
    @return ($px / 375) * 100vw;
}
```

## scss px转rem

```scss
// rem 单位换算：定为 75px 只是方便运算，750px-75px、640-64px、1080px-108px，如此类推
$vw_fontsize: 75; // iPhone 6尺寸的根元素大小基准值
@function rem($px) {
     @return ($px / $vw_fontsize ) * 1rem;
}
// 根元素大小使用 vw 单位
$vw_design: 750;

html {
    font-size: ($vw_fontsize / ($vw_design / 2)) * 100vw; 
    // 同时，通过Media Queries 限制根元素最大最小值
    @media screen and (max-width: 320px) {
        font-size: 64px;
    }
    @media screen and (min-width: 540px) {
        font-size: 108px;
    }
}
// body 也增加最大最小宽度限制，避免默认100%宽度的 block 元素跟随 body 而过大过小
body {
    max-width: 540px;
    min-width: 320px;
}
```
## table
table表格跟随浏览器宽度适应.
```
{
  able-layout:fixed
}

```

## 文字超出省略号
### 单行文本
```
{
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
  
```
### 多行文本
```
{
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
  overflow: hidden;
}
```

## 清除浮动
### 简洁版
```css
.clearfix:before, .clearfix:after {
	content:"";
	display:table;
}
.clearfix:after{
	clear:both;
	overflow:hidden;
}
.clearfix{
    zoom:1;
}
```
### 经典版
```css
.clearfix:after {
    visibility: hidden;
    display: block;
    font-size: 0;
    content: " ";
    clear: both;
    height: 0;
}
```

### bootstrap版本
```css
.clearfix::after {
  display: block;
  clear: both;
  content: "";
}
```