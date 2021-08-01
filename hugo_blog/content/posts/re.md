---
title: "正则表达式"
date: 2017-01-10T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "正则"
---

```
正达表达式：匹配    过滤

爬取编码：
两个步骤：爬取（ import    urllib.request）
                数据清洗（import   re）

import  urllib.resquest    导入爬取模块
import  re     导入正则表达式

response=urllib.request.urlopen("http://t.cn/RttEZZa")
html=response.read()
html=html.decode("utf-8”)把爬取到的数据进行解码 
ret=re.compile("百度一下")  编译   
print(ret.findall(html))     寻找所有
```