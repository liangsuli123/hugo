---
title: "jwt原理"
date: 2018-05-08T14:26:00+08:00
draft: false
tags: ["jwt"]
slug: "Jwt"
---




```
JWT的实现原理
前言
最近在做一个python项目的改造，将python项目重构为java项目，过程中遇到了这个知识点，觉得这个蛮实用的，所以下班后回来趁热打铁写下这篇总结，希望后面的人能够有所借鉴，少走弯路。

一、优势简介
JSON Web Tokens简称jwt，是rest接口的一种安全策略。本身有很多的优势：

解决跨域问题：这种基于Token的访问策略可以克服cookies的跨域问题。
服务端无状态可以横向扩展，Token可完成认证，无需存储Session。
系统解耦，Token携带所有的用户信息，无需绑定一个特定的认证方案，只需要知道加密的方法和密钥就可以进行加密解密，有利于解耦。
防止跨站点脚本攻击，没有cookie技术，无需考虑跨站请求的安全问题。
二、原理简介
JSON Web Tokens的格式组成，jwt是一段被base64编码过的字符序列，用点号分隔，一共由三部分组成，头部header，消息体playload和签名sign。

1.jwt的头部Header是json格式：
{
"typ":"JWT",
"alg":"HS256",
"exp":1491066992916
}

其中typ是type的简写，代表该类型是JWT类型，加密方式声明是HS256，exp代表当前时间.

2.jwt的消息体Playload
{
"userid":"123456",
"iss":"companyName"
}

消息体的具体字段可根据业务需要自行定义和添加，只需在解密的时候注意拿字段的key值获取value。

3.签名sign的生成
最后是签名，签名的生成是把header和playload分别使用base64url编码,接着用’.‘把两个编码后的字符串连接起来，再把这拼接起来的字符串配合密钥进行HMAC SHA-256算法加密，最后再次base64编码下，这就拿到了签名sign. 最后把header和playload和sign用’.‘ 连接起来就生成了整个JWT。

三、校验简介
整个jwt的结构是由header.playload.sign连接组成，只有sign是用密钥加密的，而所有的信息都在header和playload中可以直接获取，sign的作用只是校验header和playload的信息是否被篡改过，所以jwt不能保护数据，但以上的特性可以很好的应用在权限认证上。

1.加密
比如要加密验证的是userid字段，首先按前面的格式组装json消息头header和消息体playload，按header.playload组成字符串，再根据密钥和HS256加密header.playload得到sign签名，最后得到jwtToken为header.playload.sign，在http请求中的url带上参数想后端服务请求认证。

2. 解密
后端服务校验jwtToken是否有权访问接口服务，进行解密认证，如校验访问者的userid，首先 
用将字符串按.号切分三段字符串，分别得到header和playload和sign。然后将header.playload拼装用密钥和HAMC SHA-256算法进行加密然后得到新的字符串和sign进行比对，如果一样就代表数据没有被篡改，然后从头部取出exp对存活期进行判断，如果超过了存活期就返回空字符串，如果在存活期内返回userid的值。

四、代码示例
1.python代码的加密解密


复制代码
#!/usr/bin/env python
# coding: utf-8

from itsdangerous import BadTimeSignature, SignatureExpired
from itsdangerous import TimedJSONWebSignatureSerializer as Serializer

APP_SECRET_KEY="secret"
MAX_TOKEN_AGE=1800
token_generator = Serializer(APP_SECRET_KEY, expires_in=MAX_TOKEN_AGE)

def generate_auth_token(userid):
access_token = token_generator.dumps({"userid":userid})
return access_token

def verify_token(token):
try:
user_auth = token_generator.loads(token)
print type(token_generator)
except SignatureExpired as e:
raise e
except BadTimeSignature as e:
raise e
return user_auth
复制代码





```






    


