---
title: "前端正则匹配手机号"
date: 2017-01-15T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "re"
---
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jquery验证表单</title>
    <script type="text/javascript" src="./js/jquery.min.js"></script>
    <!-- 写入jquery的单一入口 -->
    <script type="text/javascript">
        $(function(){
            //验证手机号方法
            function isPhoneNo(phone){
                //写匹配规则 pattern匹配
                var pattern = /^1[3-9]\d{9}$/;
                //返回匹配结果
                return pattern.test(phone);

            }
            // alert(isPhoneNo(15235926326));
            //绑定提交按钮的单击事件
            $("#b2").click(function(){
                //声明变量存储动态手机号
                var _value = $(".pv").val();
                // alert(_value);
                if(isPhoneNo(_value) == false){
                    alert("您的手机号不合理，请重新输入");
                    $(".pv").val("");
                    return false;
                }   
            });
            //绑定键盘回车时间
            $(document).keyup(function(event){
                //判断回车键
                if(event.keyCode == 13){
                    //帮助点击提交按钮
                    $("#b2").click();
                }
            });
        });

    </script>
</head>

<body>
<!-- 表单提交给后端，method方式，get和post submit 提交 -->
<form action="http://192.168.1.238" method="post">

手机号：<input class="pv" name='phone' style="width: 400px;padding: 5px;" type="text" placeholder="请输入11位的手机号"/><br/><br/>
<input id='b2' type="submit" value="提交数据"/>

</form>

</body>
</html>

 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jquery验证表单</title>
    <script type="text/javascript" src="./js/jquery.min.js"></script>
    <!-- 写入jquery的单一入口 -->
    <script type="text/javascript">
        $(function(){
            //验证手机号方法
            function isPhoneNo(phone){
                //写匹配规则 pattern匹配
                var pattern = /^1[3-9]\d{9}$/;
                //返回匹配结果
                return pattern.test(phone);

            }
            // alert(isPhoneNo(15235926326));
            //绑定提交按钮的单击事件
            $("#b2").click(function(){
                //声明变量存储动态手机号
                var _value = $(".pv").val();
                // alert(_value);
                if(isPhoneNo(_value) == true){
                    alert("您的手机号没问题");
                }   else{
                    alert("你输入的手机号不合理");
                }
            });
            //绑定键盘回车时间
            $(document).keyup(function(event){
                //判断回车键
                if(event.keyCode == 13){
                    //帮助点击提交按钮
                    $("#b2").click();
                }
            });
        });

    </script>
</head>
<body>
    
手机号：<input class="pv" style="width: 400px;padding: 5px;" type="text" placeholder="请输入11位的手机号"/><br/><br/>
<input id='b2' type="button" value="提交数据"/>


</body>
</html>
```