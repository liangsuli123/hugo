---
title: "个人简历"
date: 2019-06-26T20:24:28+08:00
hidden: true
draft: false
---


# 个人基本信息

	姓    名：  梁苏莉            性    别：  女                工作年限：  5年  

	年    龄：  28                学    历：统招本科           联系方式：  18710959378    

	博客地址：https://liangsuli123.github.io/ 

	电子邮箱：carb1429@gmail.com


# 求职意向

	目标职能： python全栈工程师              目标地点：北京                     

# 个人简介

	五年Python开发经验，曾作为主力工程师参与设计与开发过多个项目，负责系统核心模块的开发，测试与自动化
	部署，有高并发web应用架构经验。熟悉Django,Scrapy,vue.js等框架,掌握前后端分离开发模式，熟悉响应式
	开发框架 Bootstrap,熟悉 Http/Https 协议、掌握 Websocket、掌握 MySQL,Redis,MongoDB 数据库与Linx
	系统的常见机制与原理,在以往的学习和工作中，练就了较强的程序调错能力，能够单独处理问题。

 
# 教育经历

	2010.9-2014.7               西安电子科技大学                  统招本科

# 开发技能描述

	1.Web开发：Python
	2.前端开发：javaScript
	3.Web框架:Django/Flask/Tornado
	4.前端框架：Bootstrap/ Vue.js/Node.js/Jquery.js 
	5.数据库相关：MySQL/Redis/Mongodb/SQLite/PostgreSQl
	6.第三方框架 Sklearn/Tensorflow 
	7.爬虫框架：Scrapy/Scrapy-redis
	8.服务器：Nginx/uWsgi
	9.工具：Docker/Git/Svn/FastDFS/Celery/Rabbitmq/Websocket
	10.其他：Tcp/Ip/Http/Https/Numpy/Pandas/Matplotlib//Gevent/Siege

 
# 工作经历
  
	2017年 4月 到  至 今            北京易思互动科技有限公司     python高级全栈工程师

	2014年 7月 到  2017年2月        妈宝无忧有限责任公司         python初级全栈工程师 

# 项目经验 

## 项目一:医美管家APP             北京易思互动科技有限公司

	技术栈：
		Django,Jwt,Mysql,Restframework,Websocket,Celery,RBAC，Echart，Nginx，Uwsgi
	项目描述：
		医美管理APP是一款提供商务服务的手机应用。医美管家app是为入驻医美平台的商家服务，商家可以随时随
		地在手机上进行接单、管理线上门店等操作，以互联网+传统医美行业相结合的运营模式，向广大求美者提供
		医学美容服务。该系统的模块有会员管理模块，产品营销模块，员工管理模块，手机收银模块，库存管理模块
		等相关功能。
	项目职责：
		1.手机收银模块，让员工简单更高效的通过手机进行前台业务收银，不再依赖电脑
		宽带，手机收银，方便高效，解决了断网，断电，电脑故障无法收银的后顾之忧。
		2.员工管理中，员工有独立的账号登录，实时查看销售业绩，业绩服务，提成，工资。使用友盟来实现消息推送，提醒员工顾客服务的周期性，顾客预约的时间，和会员顾客的生日，任务完成进度智能推送到员工APP 上，帮助员工规划好每天的工作内容。
	技术要点：

		1.项目采用的是MVT框架，模块化管理
		2.	接口以Django框架中的Restful风格开发
		3.	使用Jwt来保证接口的安全
		4.	使用支付宝来进行第三发支付
		5.	利用 Websocket实现消息主动推送，改造前端传统轮询技术框架,减少了30%的网络请求数,节约了大约一半的可用带宽
		6.	使用Mysql存储数据，使用Celery实现异步邮箱和短信推送
		7.	集成RBAC权限管理系统，方便管理层权限管理及责任划分
		8.	使用友盟消息推送
		9.	使用Bootstrap作为播放页响应式设计解决方案，一套代码自适应大小屏应用，降低了50%左右的移动端开
			发成本。
		10.	通过Echart实现数据可视化
		11.	利用Nginx反向代理后台Uwsgi+Django的平台接口，并且针对性使用Nginx负载均衡策略
	
## 项目二：医美--CRM管理系统          北京易思互动科技有限公司

	技术栈：
		Django+Vue,Numpy，Pandas，Matplotlib，SuperVisor，uwsgi
	项目描述： 
		CRM客户管理系统 是一套客户销售与服务跟进管理系统，主要侧重于对客户销售与服务过程进行持续，跟踪与管理。
		该系统主要的功能模块有 顾客档案管理，销售管理，售后管理，收银缴费，员工管理，库存管理，市场活动管理，
		数据分析中心等一些实际功能。

	项目责任： 
		顾客档案管理这个模块,详细记录顾客的消费情况，顾客的基本信息，身体信息，照片对比，特殊需求，沟通记录等各种
		特征，随时了解顾客的来龙去脉,为店面的营销政策提供全面详细的数据支持。使用Celery定时任务来实现顾客生日时发
		送邮件祝福，使用机器学习三剑客对顾客的个性特征值进行分析，从而得出表签，并对标签进行管理，使用FastDFS
		图片上传，把顾客护理前后的所有图片进行比对。

	技术要点： 
		
		1.利用 Docker搭建FastDFS对海量数据进行分布式存储，视频指纹避免重复文件问题,	为服务端节约了
		大约30%的硬盘空间。
		2.利用SuperVisor守护服务端进程提高用户体验。
		3.使用 Celery实现异步邮箱和短信推送。
		4.利用Numpy，Pandas，Matplotlib对顾客的信息进行数据分析,调整销售策略
		5.利用协同过滤算法的CF对用户的标签进行智能推荐
		6.使用Supervisor对后台服务和uwsgi操作，降低了日常维护成本
	
	
## 项目三: 分布式护肤品信息采集平台                妈宝无忧有限责任公司

	技术栈： Scrapy_Redis，Re, Xpath
	项目描述：
		该项目是一个护肤品相关热点爬取项目，旨在让公司动态实时的护肤美容行业产品热卖信息，让护肤品展示平台
		及时更新，提升市场销量，增加买点，快速的抢占市场资源
	项目职责：
		研究一些反扒策略
		使用Scrapy_Redis框架对数据进行抓取
		使用Xpath、Requests、正则表达式对数据进行抽取和清洗
		使用Ip池、Cookie池、Useragent池防止反爬虫技术
	技术要点：
		1.	使用 Docker 对项目进行重新拆分和架构，减少项目模块之间的资源耦合度，实现了持续集成  
		2.	使用 MarkDown编写公司技术文档以及维护，定期维护团队的代码，与团队成员共同进步  
		3.	使用 Selenium针对反爬虫进行反复测试和改进抓取方案 
		4.	负责设计和开发基于Scrapy 的分布式信息采集平台，优化爬虫规则和制定防反扒策 略,利用 **Redis **
			维护 Ip 代理池，提升爬去信息抓取的效率和质量。  

			

