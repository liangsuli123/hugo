---
title: "jquery 的鼠标事件/淡入淡出/绑定"
date: 2017-03-10T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "jquery 的鼠标事件/淡入淡出/绑定"
---
```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <title>jquery的学习</title>
 <!-- 引入第三方库用单表签 -->
 <script type="text/javascript" src="./js/jquery.min.js"></script>
 <script type="text/javascript">
 /* jquery 代码的入口，用来等待元素的全部加载*/ 
 // $(function() {
 //  /* 用jQuery选择器来选取某一个div 的内容*/ 
 //  /*var声明一个变量*/ 
 //  alert($("#c2").html());
  
 // });
 $(function(){
  var content =jQuery("#c2").html();
  var content1 =$(".c2").val();
  alert(content1);
  // jquery 绑定点击事件
  // $("#b3").click(function(){
  //  // 隐藏div  -----淡出时间
  //  // $("#c2").hide(3000);
  //  $("#c2").fadeOut(3000);
  
  // });
  // $("#b2").click(function(){
   // 淡入
  //  $("#c2").fadeIn(3000); 
  // });  
  $("#b2").click(function(){
   $("#c2").fadeToggle(3000); 
   });  
 
 });
 </script>
</head>
<body>
<div id="c2">
123123123
</div>
<!-- 文本框 -->
<input class=" c2" type=" text" width = "400" value= "中国"/>
 
<!-- <input  id="b3" type="button" value=" 淡出"/>
<input  id="b2" type="button" value=" 淡入"/> -->
<input  id="b2" type="button" value=" 开始"/>
</body>
</html>
```