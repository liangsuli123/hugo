---
title: "vue的选项卡功能"
date: 2017-06-20T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "vue的选项卡功能"
---
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>vue选项卡学习</title>
    <style>
    .box{
        border:1px solid blueviolet;
        height: 228px;
        width: 323px;
         background-color: bisque;
    }
    
    </style>
    <script type="text/javascript" src="./js/vue.js"></script>
    <script type="text/javascript">
        window.onload= function(){
            var app = new Vue({
                el:"#app",
                data:{
                    tabId:0
                }
            });
        }       
    </script>
</head>
<body>
    
    <div id="app">
        <!-- tab 选项 -->
        <div class="tab"> 
            <!-- 制作选项卡头部的网页 click单击-->
            <a href="#" @click="tabId=0" class="{tabId=0}">
                <!-- button 按钮 -->
               <button style="background-color:blueviolet"> mysql</button>
            </a>
            <a href="#" @click="tabId=1" class="{tabId=1}">
                <button style="background-color:palevioletred">jquery</button>
            </a>
            <a href="#" @click="tabId=2" class="{tabId=2}">
                <button style="background-color:aqua">vue.js</button>
            </a>
        </div>
        <br/>
        <!-- box 内容 -->
        <div class="box" >
            <!-- 制作选项卡内容 === 是判断 -->
            <div v-show="tabId===0" style="background-color:brown">mysql的内容
            <img src="./微信图片_20181121185958.jpg"/>
            </div>
            <div v-show="tabId===1">
            <img src="./微信图片_20181121185952.jpg" width="300" height="200"/>    
                jquery的内容
            </div>
            <div v-show="tabId===2">
            <img src="./微信图片_20181121185947.jpg" width="320" height="200"/>      
                vue.js的内容
            </div>

        </div>
    </div>
</body>
</html>
```