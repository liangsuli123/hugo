---
title: "迭代器和生成器和装饰器"
date: 2016-04-15T14:26:00+08:00
draft: false
tags: ["基础"]
slug: "Die"
---



```
迭代器

含有__iter__和__next__方法 (包含__next__方法的可迭代对象就是迭代器)
生成器
包括含有yield这个关键字，生成器也是迭代器，调动next把函数变成迭代器。
应用场景：
range/xrange
    - py2： range(1000000)  ,会立即创建，xrange(1000000)生成器
    - py3：range（10000000）生成器 
    - 列表、字典、元组

装饰器：

能够在不修改原函数代码的基础上，在执行前后进行定制操作，闭包函数的一种应用
场景：
   - flask路由系统
   - flask before_request
   - csrf
   - django内置认证
   - django缓存


#手写装饰器；
import functools
def wrapper(func):
   @functools.wraps(func)  #不改变原函数属性
   def inner(*args, **kwargs):
      执行函数前
      return func(*args, **kwargs)
      执行函数后
   return inner
    1. 执行wapper函数，并将被装饰的函数当做参数。 wapper(index)
    2. 将第一步的返回值，重新赋值给  新index =  wapper(老index)
    @wrapper    #index=wrapper(index)
    def index(x):
    return x+100


调用装饰器其实是一个闭包函数，为其他函数添加附加功能，不修改被修改的源代码和不修改被修饰的方式，装饰器的返回值也是一个函数对象。
比如：插入日志、性能测试、事物处理、缓存、权限验证等，有了装饰器，就可以抽离出大量与函数功能本身无关的雷同代码并继续重用。



```







    


