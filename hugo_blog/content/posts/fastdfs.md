---
title: "FastDFS客户端与自定义文件存储系统"
date: 2019-02-14T14:26:00+08:00
draft: false
tags: ["fastdfs"]
slug: "Fastdfs"
---

```

FastDFS客户端与自定义文件存储系统
<1>安装

安装提供给大家的fdfs_client-py-master.zip到虚拟环境中
pip install fdfs_client-py-master.zip
pip install mutagen
pip install requests
<2>使用

使用FastDFS客户端，需要有配置文件。

我们在mall/utils目录下新建fastdfs目录，将提供给大家的client.conf配置文件放到这个目录中。

需要修改一下client.conf配置文件

base_path=FastDFS客户端存放日志文件的目录
tracker_server=运行tracker服务的机器ip:22122


上传文件需要先创建fdfs_client.client.Fdfs_client的对象，并指明配置文件，如
from fdfs_client.client import Fdfs_client
client = Fdfs_client('mall/utils/fastdfs/client.conf')#自己的文件路径

通过创建的客户端对象执行上传文件的方法

client.upload_by_filename(文件名)
或
client.upload_by_buffer(文件bytes数据)
```
![](http://localhost:1313/img/f1.png)
```
生成文件：
```
![](http://localhost:1313/img/f2.png)
```
共网+8888+Remote file_id 图片名，即可访问成功

 

```

