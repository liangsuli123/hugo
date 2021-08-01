---
title: "redis安装成功后get: command not found"
date: 2019-05-20T14:26:00+08:00
draft: false
tags: ["error"]
slug: "Redis_error"
---



```


redis安装成功后get: command not found
安装redis后客户端无法使用，即redis-cli执行后报找不到的错误。

这主要是安装redis的时候没有把客户端装上，在StackOverFlow上找到了一种只安装redis cli的方法。

安装过程：

Wget

http://download.redis.io/releases/redis-5.0.4.tar.gz

 

tar xzf redis-5.0.4.tar.gz

mv redis-5.0.4 /usr/local/redis

cd /usr/local/redis

make

make install

安装完成后，我们进入目录/usr/local/bin中查看

cd /usr/local/bin
ls -all

redis-server

 

启动成功后，进入

redis-cli

set name ' data'  存入数据

get  name 获取 值

key:value 键值对的存取方式

```







    


