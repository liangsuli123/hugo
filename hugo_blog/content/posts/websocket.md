---
title: "websocket"
date: 2019-04-10T14:26:00+08:00
draft: false
tags: ["error"]
slug: "Websocket"

---

```
websocket协议解决消息发送问题 Could not decode a text frame as UTF-8.
在使用websocket 时出现了Could not decode a text frame as UTF-8

首次连接成功当发送消息时，出现了编码作错误

第一请求页面时，连接成功
```
![](http://localhost:1313/img/2.png)
 


```
当发送消息时，不加encode('utf-8') 不加ensure_ascii=False，可以连续的发送消息，但发送的内容不识别中文
```
![](http://localhost:1313/img/3.png)
 ```
 解决问题的方法如下：
```
![](http://localhost:1313/img/1.png)
