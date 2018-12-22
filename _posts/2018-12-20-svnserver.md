---
layout: post
title:  svnserver
date:   2018-12-20 09:00:00 +0800
categories: engineering
---
搭建svnserver
###  安装
下载 apache 的svn的 server

### dump and load
svnadmin load repository/repos < a.svn

### 创建repos
svnadmin create /svnrepos

创建用户
vi /svnrepos/conf/svnserve.conf

anon-access = none
auth-access = write
password-db = passwd

更改密码
vi /svnrepos/conf/passwd
add users in the format : user = password
tony = mypassword

导入项目
svn import /projects/myrailsproject file:///svnrepos/myrailsproject

checkout
svn co svn://192.168.0.2/svnrepos/myyrailsproject
