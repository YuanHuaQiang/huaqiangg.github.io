---
title: Spring代理那些事
date: 2021-04-13 23:25:56
tags:
---
### JDK动态代理

SpringBoot2.0之前对接口默认试用JDK动态代理
JDK动态代理会生成一个继承自Proxy类的子类并实现原有接口

### CGLIB代理
CGLIB代理通过生成一个代理对象的子类来实现代理
