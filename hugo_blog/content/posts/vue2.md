---
title: "vue.js的计算属性"
date: 2017-06-05T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "vue.js的计算属性"
---
```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <title>vue 计算属性的学习</title>
 <script type="text/javascript" src="./js/vue.js"></script>
 <script type="text/javascript">
 window.onload = function(){
  var app = new Vue({
   el:"#app",
   data:{
    information:'灰色的世界里，只有你的眼睛是色彩斑斓的'
   },
   computed:{
    reverseInformation:function(){
     return this.information.split('').reverse().join('')
    }
   }
  });
 }
 

 </script>
</head>
<body>
 <div id="app">
  <!-- 颠倒字符串  上面的是原版下面的是颠倒版-->
  {{information}}
  <br/><br/>
  {{reverseInformation}}
  <br/><br/>
  {{information.split('').reverse()}}
  <br/>
  {{information.split('').join('')}}
 </div>
 
</body>
</html>
```