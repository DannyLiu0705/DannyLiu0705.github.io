---
title: Jquery Tab页签
date: 2017-03-31 14:31:13
tags:
---
以前一直用bootstrap里面的标签页,后面觉得bootstrap太臃肿了,使用一个小插件浪费资源,就自己用jq写了个小东西,希望不足之处还请指出.(注:请引入jquery.js)

## js部分

``` bash
$.fn.tab = function(click,tabs){
  return this.each(function(){
    var tabNav = $(this).find(click);
    var tabCon = $(this).find(tabs);
    $(this).find(tabNav).click(function(){
      $(this).addClass("on").siblings().removeClass("on");
      $(tabCon).hide().eq($(this).index()).show();
    })
  })
}
$(".tab").tab(".tabNav a",".tabCon .tabs");
```

## html部分
<!-- more -->

``` bash
<div class="tab">
  <div class="tabNav">
    <a href="javascript:;" class="on">tab1</a>
    <a href="javascript:;">tab2</a>
  </div>
  <div class="tabCon">
    <div class="tabs">
      tab1-content
    </div>
    <div class="tabs hide">
      tab2-content
    </div>
  </div>
</div>
```

以上的class "on" 表示tab选中的样式