---
title: Jquery 复制粘贴插件clipboard.js
date: 2017-05-01 14:02:28
tags:
---
分享一个良心插件，clipboard.js 不需要加载flash就可以实现,是的,你没有看错,不需要加载flash!不需要加载flash,不需要加载flash!，简直不要太爽，废话少说，直接上码。

## 引入js

``` bash
<script src="dist/clipboard.min.js"></script>
```

## 使用

``` bash
<!-- HTML -->
<input type="text" id="text" value="content">
<button class="copy" data-clipboard-target="#text">copy</button>
```

## 事件,success和error,下面代码使用以上例子
<!-- more -->

``` bash
var clipboard = new Clipboard('.copy');

clipboard.on('success', function(){
  //doing something
})
clipboard.on('error', function(){
  //doing something
})
```

## 更多使用参考[clipboard.js](https://clipboardjs.com/#example-action) 官方网站。下载地址: [clipboard.js](https://github.com/zenorocha/clipboard.js/archive/master.zip)