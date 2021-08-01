---
title: "OSError: mysql_config not found"
date: 2019-04-02T14:26:00+08:00
draft: false
tags: ["error"]
slug: "Error"
---



```

上次在部署阿里云安装Centos7里 pip3 install mysqlclient 是 一直报

OSError: mysql_config not found
这个错，上网百度了半天终于找到了解决的办法，需要安装依赖包：

yum install mysql-devel gcc gcc-devel python-devel

安装这个在pip3 install mysqlclient 就可以了



```







    


