---
title: "css动画"
date: 2017-01-10T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "css动画"
---

```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <title>animate 学习</title>
 <script type="text/javascript"  src="./js/jquery.min.js"></script>
 <script type="text/javascript">
 //jquery单一入口
 $ (function(){
  //
  $("#b2").click(function(){
  // 通过标签选择器来进行动画动作
  $("div").animate({
   left: '400px',
   width: '400px',
   height:'400px'
  
  });
  $("div").animate({
   right: '400px',
   width: '400px',
   height:'400px'
  
  });

  });
 });

 </script>
</head>
<body>
 <div style=" width : 200px; height : 200px; font-size: 30px; text-align: center;line-height ;position:absolute;"> 我是你爸爸</div>
 </br></br>
 <input  style="margin-top:400px;" type="button" id="b2" value=" 开始动画"/>
 
</body>
</html>
```