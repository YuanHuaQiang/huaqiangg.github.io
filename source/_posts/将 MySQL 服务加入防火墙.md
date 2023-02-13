---
title: 将 MySQL 服务加入防火墙
date: 2020-07-19 13:11:17
tags:
---
## [root@centos-linux ~]# sudo firewall-cmd --zone=public --permanent --add-service=mysql
## success
## [root@centos-linux ~]# sudo systemctl restart firewalld
