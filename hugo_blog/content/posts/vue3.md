---
title: "vue.js 监听属性的学习/ 千米、米的转换 /时、分、秒 的转换"
date: 2017-06-10T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "vue.js 监听属性的学习/ 千米、米的转换 /时、分、秒 的转换"
---
```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <title>vue_的监听属性</title>
 <script type="text/javascript" src="./js/vue.js"></script>
 <script type="text/javascript">
 window.onload = function(){
  var app= new Vue({
   el:"#app",
   data:{
    kilometers:0,
    meters:0
   },
   //监听属性
   watch:{
    kilometers:function(val){
     this.kilometers = val;
     this.meters = val * 1000;
    },
    meters:function(val){
     this.kilometers = val / 1000;
     this.meters.val;
    }
   }

  });
       
        var app1 = new Vue({
         el:"#app1",
   data:{
    seconds:0,
    minutes:0,
    hours:0
   },
   //监听属性
   watch:{
    seconds:function(val){
     this.seconds = val;
     this.minutes = val/60;
     this.hours=val/3600;
    },
    minutes:function(val){
     this.seconds = val*60;
     this.minutes =val;
     this.hours = val/60;
    },
    hours: function(val){
     this.seconds = val*3600;
     this.minutes = val *60;
     this.hours= val;
    }
   }
  });  
 }
 
 </script> 
</head>
<body>
 <div id='app'>
  千米：<input  type="text" v-model = "kilometers"/>
  米： <input type="text" v-model = "meters"/>
 </div>
 <br/> <br/> 
 <div id='app1'>
 时：<input type="text" v-model = "hours">
 分：<input type="text" v-model ="minutes">
 秒：<input type="text" v-model ="seconds">
 </div>
 
</body>
</html>
```