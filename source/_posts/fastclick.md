---
title: FastClick
date: 2017-05-15 14:49:20
tags: 
---
## FastClick

FastClick简单来说就是消除移动浏览器上的点击事件的触发之间的300ms的时间延迟.

## 为什么会有延迟?

默认情况下手机浏览器在单击事件上会等待300ms的时间.  原因是浏览器在等待是否有双击事件.


## 支持情况

Safari IOS 3 以上
Chrome IOS 5 以上
Chrome Android(ICS)
Opera 11.5 以上
Android 2.0以上浏览器
PlayBook(黑莓) OS 1 以上

## 引入js
``` bash
<script type='application/javascript' src='fastclick.js'></script>
```
## 使用
<!-- more -->
官方推荐实例化FastClick在其他页面的任何元素之前:
```bash
if ('addEventListener' in document) {
  document.addEventListener('DOMContentLoaded', function() {
    FastClick.attach(document.body);
  }, false);
}
```
jQuery:
```bash
$(function() {
  FastClick.attach(document.body);
});
```
CommonJS:
```bash
var fastClick = require('fastclick');
fastClick(document.body);
```

## 更多使用参考[Fastclick.js](https://github.com/ftlabs/fastclick) 网站。下载地址: [Fastclick.js](https://github.com/ftlabs/fastclick/archive/master.zip)
