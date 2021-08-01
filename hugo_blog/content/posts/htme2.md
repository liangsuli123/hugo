---
title: "html table"
date: 2017-01-06T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "html table"
---

```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8"/>
 <title>表格制作</title>
</head>
<body>
<table border="2" width="500" align="center" height="300" cellspacing="0" cellpadding="20">
 <tr>
  <td align="center">12</td> 
  <td>1234</td> 
  <td>12345</td>
 </tr>
 <tr> 
  <td align="center"><font color="red" face="楷体" size='16'>这个世界好可怕</td></font></td>
  <td align="center">我的世界只有hello world</td>
  <td align="center">谈笑间bug灰飞烟灭</td>
 </tr>
</table>
<!-- colspan 横向合并 rowspan 竖合并 -->
 <table border="1" bgcolor="pink" width="500" align="center" height="300" cellspacing="0">
  <tr>
   <td colspan="3" align='center'> 表格2</td>
  </tr>
    <tr>
     <td rowspan="2">1</td>
     <td>2</td>
     <td>3</td>
  
    </tr>
  <tr>
     
     <td>4</td>
     <td>5</td>
 
    </tr>
 </table>

 
</body>
</html>    
```