---
title: "迁移报错"
date: 2019-04-10T14:26:00+08:00
draft: false
tags: ["error"]
slug: "Migrations"

---

```
You have 1 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): shopadmin. Run 'python manage.py migrate' to apply them.
数据库迁移时报错，

You have 1 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): shopadmin.
Run 'python manage.py migrate' to apply them.

 

 

 

可以执行 python manage.py migrate

它可以让我们在修改Model后可以在不影响现有数据的前提下重建表结构。
```