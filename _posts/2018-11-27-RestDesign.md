---
layout: post
title:  RESTDesign
date:   2018-11-27 9:00:00 +0800
categories: engineering
---
Mock api的方式。
prism mock  --spec swaggerattribute.json
http://localhost:4010/products/attributes
能否按照需要返回结果，返回的结果之间的联系，比如属性为enum时，结果
为数组

采用restlet，stoplight，swagger进行

---
Rest 资源
https://www.moesif.com/blog/technical/api-design/REST-API-Design-Filtering-Sorting-and-Pagination/

best practice
https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api
---
Rest 的风格特点有：
### 一切都是资源，资源的识别通过URI
资源与展现分开；客户端和交互通过hypermedia  HATEOAS

### client-server结构
客户端负责交互和用户状态的管理。服务端负责存储和扩展。

### stateless
服务端不保存状态，全部在请求中进行处理。

### Cacheable
必须提供cache的能力。

### layered System
无状态就可以在多个服务器上分别处理某个方面。

### Code on demand
服务端可以提供扩展，客户端动态的将处理的方法传递到服务端上去。

### 设计需要考虑的因素
- easy of user
- consistency
- exposing as little as necessary.
- extensibility
- forward compatitibility
