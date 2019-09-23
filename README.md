#1. MySQL 教程

##1.1. MySQL 简介

##1.2. MySQL 安装
由于服务器上自带了MariaDB，故选择直接使用。 MariaDB 数据库管理系统是 MySQL 的一个分支，主要由开源社区在维护，采用 GPL 授权许可。开发这个分支的原因之一是：甲骨文公司收购了 MySQL 后，有将 MySQL 闭源的潜在风险，因此社区采用分支的方式来避开这个风险。

MariaDB的目的是完全兼容MySQL，包括API和命令行，使之能轻松成为MySQL的代替品。

以为安装好了可以直接用，但是启动MariaDB时`systemctl start mariadb`报错：Failed to start mariadb.service: Unit not found.

应该是 uninstall the mariadb-server package. So use `rpm -q mariadb-server` to see if we have it installed. If you don't then `yum install mariadb-server`

mariadb数据库的相关命令是：
 
	systemctl start mariadb	#启动MariaDB
	systemctl stop mariadb	#停止MariaDB
	systemctl restart mariadb	#重启MariaDB
	systemctl enable mariadb	#设置开机启动

##1.3. 连接
`mysql`或`mysql -u root -p`即可直接连接，若要输入password，可直接回车即可。

**修改MariaDB的root密码:**   

	mysql	#连接
	USE mysql;	#进入mysql
	UPDATE user SET password=PASSWORD('TypeNewPasswordHere') WHERE User='root' AND Host = 'localhost';	#设置新密码
	FLUSH PRIVILEGES;
	exit;  #退出

现在就可以使用新密码连接到服务器了。


##1.4. 数据库

	创建数据库： CREATE DATABASE DatabaseName;
	删除数据库： drop database DatabaseName;
	选择数据库： use DatabaseName;

##1.5. 数据类型
MySQL中定义数据字段的类型对你数据库的优化是非常重要的。

MySQL支持多种类型，大致可以分为三类：数值、日期/时间和字符串(字符)类型。

##1.6. 数据表

	创建数据表： CREATE TABLE table_name (column_name column_type);
	删除数据表： DROP TABLE table_name;

MySQL 数据库使用SQL SELECT语句来查询数据。

以下为在MySQL数据库中查询数据通用的 SELECT 语法：

	SELECT column_name,column_name
	FROM table_name
	[WHERE Clause]
	[LIMIT N][ OFFSET M]

select * from runoob_tbl;	#读取数据表


#2. Python MySQL - mysql-connector 驱动
