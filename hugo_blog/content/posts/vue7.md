---
title: "vue累加计数器"
date: 2017-07-08T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "vue累加计数器"
---

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>vue的单击事件</title>
    <script type="text/javascript" src="./js/vue.js"></script>
    <script type="text/javascript">

    window.onload = function(){

        var app = new Vue({
            el:".c",
            data:{

                //定义计数器
                counter:0,
                
            }
        });
    }

    </script>

</head>
<body>
    <div class="c">
        <!-- 定义一个按钮，使用counter做累加-->
        <button v-on:click="counter += 1"><font size="2" color="blue">+</font></button>
        <input type="text" v-model="counter" style="width: 40px;background-color: pink;text-align:center" />
        <button v-on:click="counter -= 1"><font size="2" color="blue">-</font></button>
    </div>
</body>
</html>
```