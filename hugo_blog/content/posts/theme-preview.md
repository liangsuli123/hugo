---
title: "list 的操作"
date: 2016-03-11T17:49:40+08:00
hidden: false
draft: false
tags: ["基础"]
keywords: []
description: ""
slug: "Theme Preview"
---
```
"""
通过自定义的规律命中list元素中的值，若索引没有命中，直接获取该元素，合成一个新的list，
将list元素合成字符串进行反转。
"""
        lista = ["aycc","kh","llc","u","l"]
        # 自定义的规律
        listb = [1, 0, 2, 0, 3, 0, 4, 0, 5]
        c = []
        lengta = len(lista)
        for i in range(lengta):
            length = len(lista[i])
            if length < listb[i]:
                c.append(lista[i])
            else:
                c.append(lista[i][listb[i]:listb[i]+1])
        c.reverse()
        st = ''
        for i in c:
            st +=i
        print(st.upper())


#LUCKY

```