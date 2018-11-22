---
layout: post
title:  heroku cmd
date:   2018-10-23 09:00:00 +0800
categories: engineering
---
记录远程登录常用的工具
### heroku
$ heroku login

由于heroku上的目录结构是编译后的目录结构，与本地git的不太一样。

复制后，先删除 git，然后加入远端 heroku git。

保存。

heroku git:remote -a      oepfrontend

cd my-project/
$ git init
$ heroku git:remote -a oepfrontend
Deploy your application
Commit your code to the repository and deploy it to Heroku using Git.

$ git add .
$ git commit -am "make it better"
$ git push heroku master
Existing Git repository
For existing repositories, simply add the heroku remote

$ heroku git:remote -a oepfrontend

### 命令行运维模式
heroku maintenance:on

heroku maintenance 查询状态
