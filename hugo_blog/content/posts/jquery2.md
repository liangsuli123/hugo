---
title: "鼠标事件"
date: 2017-04-20T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "鼠标事件"
---
```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <title>mouse 事件</title>
 <script type="text/javascript" src=" ./js/jquery.min.js"></script>
 <script type="text/javascript" >
  $(function(){
   // 用id 选择器监听鼠标 悬停事件
   $("#b2").mouseover(function(){
    $(".c2").css("background-color","gold");
    $(".c2").css("color","blue");
    $(".c2").css("font-size","36px");

   });
   // 用id选择器来修改元素的样式
   $("#b2").mouseout(function(){
    $(".c2").css("background-color","pink");
    $(".c2").css("color","red");
    $(".c2").css("font-size","18px");
   });
  });
 
 </script>
</head>
<body>
<input type="button" id="b2" value="悬停改变颜色"/>
<div class=" c2"> 123456 </div>
<img id="b2" src ="./images/微信图片_20180903143139.jpg"/>
 
</body>
</html>
```