---
title: "html 表单"
date: 2017-01-08T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "html 表单"
---

```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <title>form 表单的学习</title>
</head>
<body>
<!-- 表单的标签 提交方式两种： get (默认 长度有限制)和 post（安全性高）  -->
<form action="http://192.168.1.238" method="get">
     用户名：<input type="text" placeholder="请输入用户名" /><br/><br/><br/>
     密&nbsp;码：<input type="password"/><br/><br/><br/>
     性&nbsp;别：<input type="radio" name="gender" value='1' />男<input type="radio" name="gender" value='0' checked="checked" />女<br/><br/><br/>
     兴趣： <input type="checkbox" name='like'/>打篮球<input type="checkbox" name='like' checked="checked"/>写代码 <br/><br/><br/>
     头像 ：<input type="file" name="picture"/><br/><br/><br/>
     个人简介：
     <textarea name="about" style="width:100px;height:200px;"></textarea><br/><br/><br/>
     地区：
     <select> 
      <option value="zz"> 郑州</option>
      <option value="ly"> 西安</option>
      <option value=""> 北京</option>
      </select><br/><br/><br/>
      按钮 ：
      <input type="sumit" value='提交表单'/> 
      <input type="reset" value='重置表单'/> 
      <input type="button" value='取消'/> 

</form>
 
</body>
</html>
```