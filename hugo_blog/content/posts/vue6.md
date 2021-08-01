---
title: "vue样式的动态绑定"
date: 2017-07-03T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "vue样式的动态绑定"
---

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>vue的样式绑定</title>
    <style type="text/css">
    .active{
        background-color: gold;
        color:blue;
    }

    </style>
    <script type="text/javascript" src="./js/vue.js"></script>
    <script type="text/javascript">

    window.onload = function(){

        var app = new Vue({
            el:"#a",
            data:{
                //激活 false
                isactive:true
            }

        });
    }

    </script>

</head>
<body>
    
    <div id="a">人生最棒的是不后悔
    <div v-bind:class="{ active:isactive }" style="width: 200px">
    人生最难的是不留遗憾
    </div>
    </div>

</body>
</html>
```