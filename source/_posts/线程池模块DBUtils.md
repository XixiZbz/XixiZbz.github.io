title: 线程池模块DBUtils
author: XixiZbz
date: 2017-10-25 19:02:06
tags:
---
#### 问题出现：

- 亚马逊评论爬虫并行插入mysql数据库时，出现(0,("",""))的报错，跟我很早以前遇到的一样，之前因为项目急，用列表代替队列的形式把插入数据单独一个模块。

#### 分析：

- 基本上可以确定是插入中，多个进程抢夺一个游标所致。

#### 解决：

- 使用python 的DBUtils模块，在线程池下进行插入，就完美解决这个问题，当然，后续应该是要把数据缓存到redis之类的数据库内，再处理，公司还没有这个准备，就先用数据库连接池解决。
<!--more-->

```
from DBUtils.PooledDB import PooledDB
import pymysql

db_pool = PooledDB(pymysql,mincached =100,blocking=True,maxconnections=102,maxshared=100,**mysql_config)
conn = db_pool.connection()
cursor = conn.cursor()
# PooledDB的参数：
#1. mincached，最少的空闲连接数，如果空闲连接数小于这个数，pool会创建一个新的连接
#2. maxcached，最大的空闲连接数，如果空闲连接数大于这个数，pool会关闭空闲连接
#3. maxconnections，最大的连接数，
#4. blocking，当连接数达到最大的连接数时，在请求连接的时候，如果这个值是True，请求连接的程序会一直等待，直到当前连接数小于最大连接数，如果这个值是False，会报错，
#5. maxshared 当连接数达到这个数，新请求的连接会分享已经分配出去的连接
```