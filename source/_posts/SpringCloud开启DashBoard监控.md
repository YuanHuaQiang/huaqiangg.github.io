---
title: SpringCloud开启DashBoard监控
date: 2021-04-11 15:49:02
tags:
---
1. 导入DashBoard依赖
2. 在需要监控的服务中导入actuator依赖，注入一个Bean将 `registrationBean.addUrlMappings("/actuator/hystrix.stream");`
3. 在需要监控的接口加上@HystrixCommand注解
4. 启动类添加@EnableCircuitBreaker注解
5. 监控服务参数修改 hystrix.dashboard.proxy-stream-allow-list: "*"
