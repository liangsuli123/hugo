---
title: "web三大框架"
date: 2019-04-10T14:26:00+08:00
draft: false
tags: ["后端", "体系"]
slug: "Japanese-Preview"
---

> python web三大框架，flask、django、tornado



 


```
Django（ORM、URL分发系统、MTV）
Django是一个开放源代码的Web应用框架，由Python写成。采用了MVC的框架模式，即模型M，视图V和控制器C。它最初是被开发来用于管理劳伦斯出版集团旗下的一些以新闻内容为主的网站的，即CMS（内容管理系统）软件。并于2005年7月在BSD许可证下发布。这套框架是以比利时的吉普赛爵士吉他手Django Reinhardt来命名的。
Django基于MVC的设计十分优美：

django内部是如何运行的？
	Django会先根据settings中的WSGI_APPLICATION来获取handler；在创建project的时候，Django会默认创建一个wsgi.py文件，而settings中的WSGI_APPLICATION配置也会默认指向这个文件。看一下这个wsgi.py文件，其实它也和上面的逻辑一样，最终调用get_wsgi_application实现。


uWSGI+Nginx的方法是现在最常见的在生产环境中运行Django的方法，
	WSGI，全称Web Server Gateway Interface，或者Python Web Server Gateway Interface，是为Python语言定义的Web服务器和Web应用程序或框架之间的一种简单而通用的接口，基于现存的CGI标准而设计的。WSGI其实就是一个网关(Gateway)，其作用就是在协议之间进行转换。
	uWSGI是一个Web服务器，它实现了WSGI协议、uwsgi、http等协议。
	注意uwsgi是一种通信协议，而uWSGI是实现uwsgi协议和WSGI协议的Web服务器。uWSGI具有超快的性能、低内存占用和多app管理等优点。
	
	
	Uwsgn 网关接口，也是一种服务器，实现了wsgi，uwsgi，http 等协议超块的性能，地内存占用，和多app管理等优点，实现了协议之间的转换
	反向代理  http服务器和反向代理服务器




Flask
Flask是一个使用 Python 编写的轻量级 Web 应用框架。其 WSGI 工具箱采用 Werkzeug ，模板引擎则使用 Jinja2 。Flask使用 BSD 授权。
Flask也被称为 “microframework” ，因为它使用简单的核心，用 extension 增加其他功能。Flask没有默认使用的数据库、窗体验证工具。

Flask确实很“轻”，不愧是Micro Framework，从Django转向Flask的开发者一定会如此感慨，除非二者均为深入使用过
Flask自由、灵活，可扩展性强，第三方库的选择面广，开发时可以结合自己最喜欢用的轮子，也能结合最流行最强大的Python库
入门简单，即便没有多少web开发经验，也能很快做出网站
非常适用于小型网站
非常适用于开发web服务的API
开发大型网站无压力，但代码架构需要自己设计，开发成本取决于开发者的能力
各方面性能均等于或优于Django



Tornado
    Tornado是一种 Web 服务器软件的开源版本。Tornado 和现在的主流 Web 服务器框架（包括大多数 Python 的框架）有着明显的区别：它是非阻塞式服务器，而且速度相当快。
    得利于其非阻塞的方式和对epoll的运用，Tornado 每秒可以处理数以千计的连接，因此 Tornado 是实时 Web 服务的一个 理想框架。
    
	
	Tornado就是我们在 FriendFeed 的 Web 服务器及其常用工具的开源版本  。Tornado 和现在的主流 Web 服务器框架（包括大多数 Python 的框架）有着明显的区别：它是非阻塞式服务器，而且速度相当快。得利于其 非阻塞的方式和对epoll的运用，
	
	Tornado 每秒可以处理数以千计的连接，因此 Tornado 是实时 Web 服务的一个 理想框架。我们开发这个 Web 服务器的主要目的就是为了处理 FriendFeed 的实时功能 ——在 FriendFeed 的应用里每一个活动用户都会保持着一个服务器连接。

```