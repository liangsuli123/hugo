---
title: "jquery_ajax 跨域"
date: 2017-04-10T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "jquery_ajax 跨域"
---

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jquery_ajax</title>
    <script type="text/javascript" src="./js/jquery.min.js"></script>
    <script type="text/javascript">
        //写jquery的单一入口
        $(function(){
            //绑定按钮事件
            $("#b2").click(function(){
            //用异步的形式来提交数据给服务器
            $.ajax({
                //提交方式使用get
                type:'GET',
                //提交网址
                url:'http://192.168.1.238/ajax.php',
                //数据格式
                dataType:'jsonp',
                //具体数据
                data:{'phone':$("#phone").val()},
                //回调函数
                jsonp:'callback',
                //通信成功，打印服务器返回的数据
                success:function(msg){
                    console.log(msg);
                }            
            });        
            });
        });

    </script>
</head>

<body>
    手机号：<input id='phone' type="text" style="width:200px;padding: 5px" placeholder="请输入你的手机号"/>
    <br/><br/>
    <input id="b2" type="button" value="提交手机号"/>



</body>
</html>
```