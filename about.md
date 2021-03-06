---
layout: page
title: About
math: true
permalink: /about/
---

{% if page.math != false %}
 {% include mathjax.html %}
{% endif %}

### fanto：
![微信](/assets/images/wx_icon.png){:height="100px" width="100px"}

曾从事 测试[^1]，开发[^2]，项目管理[^3]，架构[^4]，技术负责人[^5] 等岗位。


{% highlight swift %}
func saySomethingToWorld(who:String ,num :Int ,say:(_ :String)->Void ) {
    for _ in 0..<num {
        say(who)
    }
}
saySomethingToWorld(who: "fanto", num: 3) { (who) in
    print("Hi," + who + " , focus on building things rather than talking it.")
}
{% endhighlight %}

$$  1.02^{365}=1377.4 \over 0.99^{365}=0.03 $$


***

# 工具箱

- [《RSocket》]({% post_url 2020-01-02-Rsocket %})，[《Http2》]({% post_url 2020-01-02-Http2 %})

- [《项目事例》]({% post_url 2018-02-27-开发流程 %}) , [mind]({% post_url 2019-08-02-xmind %}), [UML]({% post_url 2019-09-09-uml %}) , project , axure , [markdown]({% post_url 2018-03-09-Markdown专题 %}), [jekyll]({% post_url 2018-02-27-Jekyll专题 %})


- [《产品事例-appstore》](https://itunes.apple.com/cn/app/%E5%AE%B6%E7%A7%98%E4%B9%A6/id1352891324?mt=8 ), [swift]({% post_url 2018-03-09-swift专题 %}), [java]({% post_url 2018-06-13-java %}) ,[lombok]({% post_url 2019-12-02-lombok %}), node

- cocoapods, [spring boot]({% post_url 2018-03-09-spring-boot专题 %}) , [spring cloud]({% post_url 2018-03-19-SpringCloud专题 %})

- [coreml]({% post_url 2018-02-07-coreml专题 %})

- mysql , db2, oracle , postgresql

- activiti , drools

- openmq , rabbitmq , mule

- pentaho kettle , jasper , qlik sense

- hyperledger, ethereum

- [docker]({% post_url 2019-07-14-docker %}) , [k8s]({% post_url 2019-08-18-k8s %})

- [git]({% post_url 2018-02-28-git专题 %})

- [devops]({% post_url 2019-12-10-devops %})


### 项目角色
[^1]:测试：Webshpere Portal 自动化测试，silktest、robot自动化测试框架 ，jmeter,lr压力测试，手工测试。
[^2]:开发：自动化开发框架OAF-相当于：activti + hibernate，测试缺陷系统开发，hp打印机字体驱动软件程序，Flex+lifecycle审批业务系统开发。
[^3]:项目管理及开发：费用补偿系统，行政办公审批系统，人力招聘候管理系统 ，工资考勤系统， 等系统。
[^4]:架构及开发：Paas平台，多终端自动化测试平台开发，某互联网O2O业务系统，信息交换平台软件。
[^5]:技术负责人及开发：技术部门管理（30人左右），负责含有多语言技术、多终端技术的研发部门的研发生产和人员管理。
