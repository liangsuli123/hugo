---
title: "数据库分表分库"
date: 2019-04-03T14:26:00+08:00
draft: false
tags: ["sql"]
slug: "Sql_1"
---

```

分表分库
	1、分库
    当数据库中的表太多，将某些表分到不同数据库，例如：1W张表时
    代价：连表查询跨数据库，代码变多
	2、分表
		水平分表：将某些列拆分到另一张表，例如：博客+博客详情
		垂直分表：将某些历史信息，分到另外一张表中，例如：支付宝账单  order 表

	当一张表的数据达到几千万时，查询一次所花的时间会变长。这时候，如果有联合查询的话，可能会卡死在那儿，甚至把系统给拖垮。
	
	而分库分表的目的就在于此：减小数据库的负担，提高数据库的效率，缩短查询时间。
	如果有2个sql都要同时修改同一张表的同一条数据，mysql对这种情况的处理是：一种是表锁定（MyISAM存储引擎），一个是行锁定（InnoDB存储引擎）。
	
	分库分表术语：
	读写分离: 不同的数据库，同步相同的数据，分别只负责数据的读和写；
	
	分区:指定分区列表达式，把记录拆分到不同的区域中(必须是同一服务器，可以是不同硬盘)，应用看来还是同一张表，没有变化；
	
	分库：一个系统的多张数据表，存储到多个数据库实例中；
	分表: 对于一张多行(记录)多列(字段)的二维数据表，又分两种情形：
	
	垂直分表: 竖向切分，不同分表存储不同的字段，可以把不常用或者大容量、或者不同业务的字段拆分出去；
	水平分表(最复杂): 横向切分，按照特定分片算法，不同分表存储不同的记录。
	在实际生产中，通常的进化过程是：单库单表->单库多表->多库多表；；分区->分表->分库（垂直分库 - 水平分库 - 读写分离）



```






    


