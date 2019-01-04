---
layout: post
title:  Linux Basic
date:   2018-05-09 9:00:00 +0800
categories: engineering
---
问题列表：
###

### 问题kernel
uname -a
uname -srm --- 查看运行的版本。
cat /proc/version --- 查看 哪个发行商的内容。

### 传递文件
scp oepfrontend.tar root@192.168.44.5:~/oepfrontend

http://www.cnblogs.com/peida/archive/2013/03/15/2960802.html

### 打包
解包：tar xvf FileName.tar
打包：tar cvf FileName.tar DirName
解压：tar zxvf FileName.tar.gz
压缩：tar zcvf FileName.tar.gz DirName

### 安装组件方式
各个系统不同

### 运行
nohup command &

退出ssh时，使用exit；直接关掉，导致打开的进程也被关掉了。

ip addr show
ipconfig

### 磁盘空间
df -ah

du -sh code/
nohup npm start &
nohup node app.js &

service *** status
systemctl status service

netstat -tulnp

ps aux|grep nginx
