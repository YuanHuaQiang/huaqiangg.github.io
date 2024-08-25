---
title: Vue懒加载
date: 2024-08-25 16:40:48
tags: vue
---
问题：nginx代理vue项目时除了首页外其他页面无法打开。

原因：vue懒加载没有正确执行。

解决办法：使用‘@babel/plugin-syntax-dynamic-import’插件代替‘dynamic-import-node’

总结：
当使用 @babel/plugin-syntax-dynamic-import 插件时，它仅仅为 Babel 提供了解析动态导入语法的能力，而不会实际改变动态导入的行为。这意味着你的代码仍然可以按预期方式进行懒加载。

与此相反，dynamic-import-node 插件会将所有的 import() 语句转换为 require()，从而在构建阶段实现同步导入。这可能会影响懒加载的实现，尤其是在某些复杂的配置中或与其他插件、工具产生冲突时。

因此，使用 @babel/plugin-syntax-dynamic-import 可以避免因为强制同步化导入而引起的配置冲突或行为变化，从而让懒加载功能在开发和生产环境下都正常工作。这解释了为什么更换插件后，懒加载功能可以正确运行。