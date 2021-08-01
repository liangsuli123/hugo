---
title: "编码"
date: 2018-04-03T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "Bianma"
---



```
import base64

s = '无可挑剔'
q=base64.b64encode(bytes(s, 'gbk'))
print(q)
w=base64.b64decode(base64.b64encode(bytes(s, 'gbk')))

print(w)


编码过程
s = "无可挑剔"

encoder = base64.b64encode(s.encode("utf-8"))
print(encoder)

str_encoder = encoder.decode('utf-8')
print(str_encoder)

# 解码过程
decoder = base64.b64decode(str_encoder)
print(decoder.decode('utf-8'))



src = "功成名就"
tgt = base64.b64encode(src.encode('UTF-8'))
print (tgt)
src = base64.b64decode(tgt).decode('utf-8')
print (src)

"""
b'zt6/ycz0zN4='
b'\xce\xde\xbf\xc9\xcc\xf4\xcc\xde'
b'5peg5Y+v5oyR5YmU'
5peg5Y+v5oyR5YmU
无可挑剔
b'5Yqf5oiQ5ZCN5bCx'
功成名就

"""

```







    


