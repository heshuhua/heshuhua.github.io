---
layout: post
title:  SpringCloud专题
date:   2018-03-19 09:09:00 +0800
categories: skill
---
单体应用:虽然按照 模块化的设计，但最终打包到一个war，ear。
, 部署和监控都很方便。但是：

- 代码多，混在一起，越来越大
- 多个team 弄同一个 代码，麻烦多多
- 扩展应用中的某个部分，不太可能。
- 从长期运维的角度， 技术变化，和功能变化需要更新代码，酸爽。

## 微服务

- 开始切分子业务领域困难
- 需要处理分布式应用的复杂
- 没有恰当的devops 管理分布应用是困难的。
- 本地的开发环境的设置，比较困难。

## SpringCloud

[SpringCloud子项目](https://projects.spring.io/spring-cloud/)

springboot：越来越多的企业不会建立数据中心来跑各种应用，而是开发出来部署到云端。

Springcloud是建立 云 服务的一些基本的实现。可以只关注业务逻辑，剩下的内容有springcloud中的modules来实现

## 配置管理 congfigServer

spring cloud config 解决了将配置脱离应用，放到分布式环境中的问题，通过更改配置并不需要重新启动应用，而就将
整个的配置更新到分布式环境中。


## 服务发现

服务需要 scale up/down ， 不能依赖手动的hostname等， 因此需要 服务的发现和注册组件。 Eureka，Consul，Zookeeper

## 熔断机制

服务依赖，如果一个服务的不可用会影响到其他的服务。采用 Hystrix

## 处理大量数据

需要处理大量的数据流的时候，采用 DAtaStreams， 处理kafka，spark的数据

## 安全机制

某些服务的调用需要认证与授权的时候，并希望sso，可以使用Oauth2

## 分布式跟踪

调用不同的组件，需要 Sleuth with Zipkin 进行跨服务的跟踪

## 契约

在多个team进行api开发的时候，形成约束机制。 Spring cloud contract .
