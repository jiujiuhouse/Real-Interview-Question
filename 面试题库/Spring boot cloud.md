## 104. 什么是 spring boot？

spring boot 是为 spring 服务的，是用来简化新 spring 应用的初始搭建以及开发过程的。

## 105. 为什么要用 spring boot？

* 配置简单
* 独立运行
* 自动装配
* 无代码生成和 xml 配置
* 提供应用监控
* 易上手
* 提升开发效率
## 106. spring boot 核心配置文件是什么？

spring boot 核心的两个配置文件：

* bootstrap (.yml 或者.properties)：boostrap 由父 ApplicationContext 加载的，比 applicaton 优先加载，且 boostrap 里面的属性不能被覆盖；
* application (.yml 或者.properties)：用于 spring boot 项目的自动化配置。
## 107. spring boot 配置文件有哪几种类型？它们有什么区别？

配置文件有 . properties 格式和 . yml 格式，它们主要的区别是书法风格不同。

. properties 配置如下：
```properties
spring. RabbitMQ. port=5672
```

.yml配置如下：
```yml
spring:
    RabbitMQ:
        port: 5672
```
. yml 格式不支持 @PropertySource 注解导入。

## 108. spring boot 有哪些方式可以实现热部署？

* 使用 devtools 启动热部署，添加 devtools 库，在配置文件中把 spring. devtools. restart. enabled 设置为 true；
* 使用 Intellij Idea 编辑器，勾上自动编译或手动重新编译。
## 109. jpa 和 hibernate 有什么区别？

jpa 全称 Java Persistence API，是 Java 持久化接口规范，hibernate 属于 jpa 的具体实现。

## 110. 什么是 spring cloud？

spring cloud 是一系列框架的有序集合。它利用 spring boot 的开发便利性巧妙地简化了分布式系统基础设施的开发，如服务发现注册、配置中心、消息总线、负载均衡、断路器、数据监控等，都可以用 spring boot 的开发风格做到一键启动和部署。

## 111. spring cloud 断路器的作用是什么？

在分布式架构中，断路器模式的作用也是类似的，当某个服务单元发生故障（类似用电器发生短路）之后，通过断路器的故障监控（类似熔断保险丝），向调用方返回一个错误响应，而不是长时间的等待。这样就不会使得线程因调用故障服务被长时间占用不释放，避免了故障在分布式系统中的蔓延。

## 112. spring cloud 的核心组件有哪些？

* Eureka：服务注册于发现。
* Feign：基于动态代理机制，根据注解和选择的机器，拼接请求 url 地址，发起请求。
* Ribbon：实现负载均衡，从一个服务的多台机器中选择一台。
* Hystrix：提供线程池，不同的服务走不同的线程池，实现了不同服务调用的隔离，避免了服务雪崩的问题。
* Zuul：网关管理，由 Zuul 网关转发请求给对应的服务。

[回到目录](https://github.com/jiujiuhouse/Real-Interview-Question/blob/master/面试题库/interviews.md)