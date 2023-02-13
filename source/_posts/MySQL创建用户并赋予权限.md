---
title: MySQL创建用户并赋予权限
date: 2019-10-23 16:15:18
tags: 
---
CREATE USER 'username'@'localhost' IDENTIFIED BY 'password'; 创建用户

grant select,update on * to username identified by 'password'; 赋权

FLUSH PRIVILEGES;（刷新权限）

重启服务生效
