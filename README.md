#MySQL 教程

##1.MySQL 简介

##2.MySQL 安装
由于服务器上自带了MariaDB，故选择直接使用。 MariaDB 数据库管理系统是 MySQL 的一个分支，主要由开源社区在维护，采用 GPL 授权许可。开发这个分支的原因之一是：甲骨文公司收购了 MySQL 后，有将 MySQL 闭源的潜在风险，因此社区采用分支的方式来避开这个风险。

MariaDB的目的是完全兼容MySQL，包括API和命令行，使之能轻松成为MySQL的代替品。

以为安装好了可以直接用，但是启动MariaDB时```systemctl start mariadb```报错：Failed to start mariadb.service: Unit not found.

应该是 uninstall the mariadb-server package. So use ```rpm -q mariadb-server``` to see if we have it installed. If you don't then ```yum install mariadb-server```

mariadb数据库的相关命令是：   
```systemctl start mariadb```  #启动MariaDB  
```systemctl stop mariadb```  #停止MariaDB  
```systemctl restart mariadb```  #重启MariaDB  
```systemctl enable mariadb``` #设置开机启动  
##3.My project

###3.1. 0.1 version(2h)

###3.2. 0.2 version

###3.3. 0.3 version

###3.4. 0.4 version

###3.5. 1.0 version
