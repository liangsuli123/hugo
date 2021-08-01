---
title: "vue表单选项框"
date: 2017-06-25T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "vue表单选项框"
---
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>vue表单的学习</title>
    <script src="./js/vue.js"></script>
    <script>
        //单一入口
    window.onload = function(){
        var app = new Vue({

            el:"#a",
            data:{
                message:'你好'
            }
        });
        // 多选框的增删改查
        var app = new Vue({
            el:"#b",
            data:{
                checknames:[]
            }
        });
        // 单选框
        var app = new Vue({
            el:"#c",
            data:{
                picked:"",gender:"男"
            }
        });
    }
    
    </script>
    
</head>
<body>
    <div id = "a">
        <!-- 双向绑定用 v-model绑定 -->
    <input type='text' v-model='message'/>

    设置的变量内容是: {{message}}
    <!-- 多行文本域 textarea -->
    <textarea v-model="message" style="height:300px"></textarea><br/>

    <!-- 多选框的绑定 checkbox label是标签属性，来注明多选框的内容 -->
    <input type='checkbox' name="crouse" value='mysql'/>
    <label>mysql</label>

    <input type="checkbox" name="crouse" value="jquery"/>
    <label>jquery</label>

    <input type="checkbox" name="crouse" value="vue"/>
    <label>vue</label>
    <br/><br/>
</div>
<!-- 多选框的绑定并显示出来 -->
<div id="b">
     
     <!-- 多选框的绑定 checkbox label是标签属性，来注明多选框的内容 -->
     <input type='checkbox' name="crouse" value='mysql' v-model="checknames" />
     <label>mysql</label>
 
     <input type="checkbox" name="crouse" value="jquery" v-model="checknames"/>
     <label>jquery</label>
 
     <input type="checkbox" name="crouse" value="vue" v-model="checknames"/>
     <label>vue</label>
     <!-- 用vue的模板语法来打印勾选的课程列表 -->
     {{ checknames }} <label>这是你所选的课程</label>
</div>
<br/><br/>
<!-- vue的单选标签 -->
    <div id="c">
        <!-- name 分组 -->
        <input type="radio" name="yesorno" value="是" v-model="picked" />
        <label>是</label>
        <input type="radio" name="yesorno" value="否" v-model="picked" />
        <label>否</label>
        <input type="radio" name="nanornv" value="男" v-model="gender" />
        <label>男</label>
        <input type="radio" name="nanornv" value="女" v-model="gender" />
        <label>女</label>
        <br/>
        <span>你选中的是：{{ picked }}  ，&nbsp;选择性别：{{ gender }}</span>
    </div>


</body>
</html>
```