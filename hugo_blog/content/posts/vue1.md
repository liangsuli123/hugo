---
title: "vue入门"
date: 2017-05-10T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "vue入门"
---
```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <title>Vue.js 的入门</title>
 <!-- 导入 -->
 <script type="text/javascript" src="./js/vue.js"></script>
 <script type="text/javascript">
 //单一入口
 window.onload = function(){
  var app = new Vue({
   //el 属性用来绑定元素节点
   el:"#app",
   //data属性用来绑定数据
   data:{
    message:'Hello World'
   }
  });
  //建立vue对象
  var app2 = new Vue({
   // 绑定元素节点
   el:"#app2",
   data:{
    message:'页面加载于'+new Date().toLocaleString+ '你是不是傻'
   }
  });

 }
 

 </script>
</head>
<body>
<div id="app">
<!-- vue 的模板语法，两个大括号用来输出变量 -->
 {{message}}
</div>
<div id="app2">
 <!-- 把title属性和message变量联系起来 -->
 <span v-bind:title="message">
  请让鼠标悬停几秒钟，来观看这个页面刷新的时间
 </span>
 <br/> <br/>
 <a href="#" title=" 这是一个空链接"> 请鼠标悬停几秒</a>
</div>
 
</body>
</html>
```