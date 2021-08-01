---
title: "正则2"
date: 2018-04-20T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "Re2"
---



```


正达表达式：匹配    爬取     过滤   合法性的判断---------runoob.com网址
四方法：match   group
             compile  findall


爬取编码：
两个步骤：爬取（ import    urllib.request）
                数据清洗（import   re）
import  urllib.resquest    导入爬取模块
import  re     导入正则表达式
response=urllib.request.urlopen("http://www.baidu.com")
html=response.read()
html=html.decode("utf-8”)把爬取到的数据进行解码 
ret=re.compile("百度一下")  编译   
print(ret.findall(html))     寻找所有

```







    


