---
layout: post
title:  dockermicroservices
date:   2019-03-18 09:00:00 +0800
categories: engineering
---
使用 基本框架完成事务与saga
### 在mac下使用 消息事务化。
http://eventuate.io/docs/usingdocker.html

sudo ifconfig lo0 alias 10.200.10.1/24  # (where 10.200.10.1 is some unused IP address)
export DOCKER_HOST_IP=10.200.10.1

### 配置docker KAFKA_ADVERTISED_HOST_NAME

https://stackoverflow.com/questions/35861501/kafka-in-docker-not-working
配置
environment:
    KAFKA_ADVERTISED_HOST_NAME: "kafka"

more /etc/hosts
127.0.0.1       localhost kafka

### 配置 eclipse 远程debug
新建立远程调试的配置，验证选择的是调试的应用。端口设定为 tomcat 指定的jpda接口。

### 配置 docker-composse
service

service restart 指的service restart

build

volumes：将local机器路径映射到 容器。
volumes:
     - ./app/target/UserSignup:/usr/local/tomcat/webapps/UserSignup



https://docs.docker.com/compose/compose-file/compose-file-v2/

### 制作docker image
expose 指定docker 监听的端口
ENV 设定 环境变量， 比如 在启动tomcat的 远程debug，ENV JPDA_TRANSPORT="dt_socket"
ADD 就是copy
RUN

https://docs.docker.com/engine/reference/builder/

### cdc
指 change data capture
