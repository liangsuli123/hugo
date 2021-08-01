---
title: "centos 中 redis 的安装"
date: 2016-05-30T14:26:00+08:00
draft: false
tags: ["配置"]
slug: "Centos"
---



```
centos 中 redis 的安装
安装流程

Wget http://download.redis.io/releases/redis-5.0.4.tar.gz

 tar xzf redis-5.0.4.tar.gz

mv redis-5.0.4 /usr/local/redis

cd /usr/local/redis

make

make install

安装完成后，我们进入目录/usr/local/bin中查看

cd /usr/local/bin
ls -all

redis-server &

 

配置
Redis的配置信息在/usr/local/redis/redis.conf下。
查看   sudo vi    redis.conf
核心配置选项
绑定ip：如果需要远程访问，可将此⾏注释，或绑定⼀个真实ip
    bind 127.0.0.1    如需要远程连接 可以将端口修改为 0.0.0.0

端⼝，默认为6379
     port 6379

是否以守护进程运⾏
如果以守护进程运⾏，则不会在命令⾏阻塞，类似于服务
如果以⾮守护进程运⾏，则当前终端被阻塞
设置为yes表示守护进程，设置为no表示⾮守护进程
推荐设置为yes
      daemonize yes

数据⽂件
       dbfilename dump.rdb

数据⽂件存储路径
      dir /var/lib/redis

⽇志⽂件
     logfile "/var/log/redis/redis-server.log"

数据库，默认有16个
      database 16

主从复制，类似于双机备份。
     slaveof

 

启动：

redis-server &  后台启动使用默认配置

redis-server 直接启动

redis-server  配置路径 如redis-server  /usr/local/redis/redis.conf 不是后台启动 这时候要后台启动的话就需要配置redis.conf中的

daemonize on     改为yes

关闭redis

 ps -ef | grep redis 查看redis服务器进程
sudo kill -9 pid 杀死redis服务器

 

以守护进程的方式进行

修改redis.conf中daemonize为yes

Cd /usr/local/bin

./redis-server /usr/local/redis/redis.conf

 

redis是key-value的数据结构，每条数据都是⼀个键值对
键的类型是字符串
注意：键不能重复
 

设置键值
　　　　set key value

例1：设置键为name值为data的数据
　　　　set name data

 

设置键值及过期时间，以秒为单位
　　　　setex key seconds value

例2：设置键为aa值为aa过期时间为3秒的数据
　　　　setex aa 3 aa

 

设置多个键值
　　　　mset key1 value1 key2 value2 ...

例3：设置键为'a1'值为'python'、键为'a2'值为'java'、键为'a3'值为'c'
　　　　mset a1 python a2 java a3 c

 

追加值
　　　　append key value

例4：向键为a1中追加值' haha'
　　　　append 'a1' 'haha'

 

获取
获取：根据键获取值，如果不存在此键则返回null
　　　　get key

例5：获取键'name'的值
　　　　get 'name'

根据多个键获取多个值
　　　　mget key1 key2 ...

例6：获取键a1、a2、a3'的值
　　　　mget a1 a2 a3

 

查看键对应的value的类型
　　　　type key

例4：查看键a1的值类型，为redis⽀持的五种类型中的⼀种
　　　　type a1

删除键及对应的值
　　　　del key1 key2 ...

例5：删除键a2、a3
　　　　del a2 a3

 　设置过期时间，以秒为单位

如果没有指定过期时间则⼀直存在，直到使⽤DEL移除
　　　　expire key seconds

例6：设置键'a1'的过期时间为3秒
　　　　expire 'a1' 3

　　查看有效时间，以秒为单位

　　　　ttl key

 

hash类型
hash⽤于存储对象，对象的结构为属性、值
值的类型为string
设置单个属性
增加、修改
hset key field value

例1：设置键 user的属性name为itheima
                 hset user name itheima

 获取

获取指定键所有的属性
　　　　hkeys key

例3：获取键u2的所有属性
　　　　hkeys u2

获取⼀个属性的值
　　　　hget key field

例4：获取键u2属性'name'的值
　　　　hget u2 'name'

获取多个属性的值
　　　　hmget key field1 field2 ...

例5：获取键u2属性'name'、'age的值
　　　　hmget u2 name age

获取所有属性的值
　　　　hvals key

例6：获取键'u2'所有属性的值
　　　　hvals u2

 删除

删除整个hash键及值，使⽤del命令
删除属性，属性对应的值会被⼀起删除
　　　　hdel key field1 field2 ...

例7：删除键'u2'的属性'age'
　　　　hdel u2 age

 

centos配制外面可以访问  在阿里云配置6379 端口到权限安全组 

bind 127.0.0.1  改为bind 0.0.0.0

将  redis.conf 文件 中的   protected-mode yes  改为      protected-mode no

重启redis

在服务器里用客户端连接

redis-cli

设置密码 

config set requirepass xxx    xxx 为密码

redis-cli -a xxx   启动时使用密码

 

在views.py 中   


 

在setting中配置：

 

在xshell 中启动redis-cli -a  xxx

set name 'hhh'

get name  获取name 的值

在项目中配置好setting文件,启动项目文件，访问接口查看是否获取到接口中name 的值，获取到值说明 远程连接成功

```







    


