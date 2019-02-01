---
layout: post
title:  hibernate
date:   2019-01-30 09:00:00 +0800
categories: engineering
---
parameterized queries
### 参数化查询
参数化查询不能改变 查询路径，否则数据库会报异常。
不能使用类似的方式。
select * from myTable order by ?
select id, f1, ? from myTable
select * from ?

### 
