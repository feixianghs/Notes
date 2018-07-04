### 一、数据库简介

#### 1.数据库系统

##### 1.1数据库

> DataBase【DB】，指的是长期保存到计算机上的数据，按照一定顺序组织，可以被各种用户或者应用共享的数据集合
>
> 【用于存储数据的地方，可以视为存储数据的容器】

##### 1.2数据库管理系统

> DataBase Management System【DBMS】,能够管理和操作数据库的大型的软件
>
> 用于建立、使用和维护数据库，对数据库进行统一的管理和控制，为了保证数据库的安全性和完整性，用户可以通过数据库管理系统访问数据库中的数据
>
> 【面试题：数据库和数据库管理系统之间的关系】
>
> 数据库：存储，维护和管理数据的集合
>
> 数据库管理系统其实就是数据库管理软件，通过它可以进行数据库的管理和维护工作
>

##### 1.3数据库的应用

> 涉及到大量的数据需要长期存储，就可以使用数据库
>
> 使用：增删改查的操作

#### 2.常见数据库管理系统

> 1>Oracle（甲骨文）:目前比较成功的关系型数据库管理系统，运行稳定，功能齐全，性能超群，技术领先，主要应用在大型的企业数据库领域
>
> 2>DB2:IBM（国际商业机器公司）的产品，伸缩性比较强
>
> 3>SQL Server:Microsoft的产品，软件界面友好，易学易用，在操作性和交互性方面独树一帜
>
> 4>PostgreSQL:加州大学伯克利分校以教学为目地开发的数据库系统，支持关系和面向对象的数据库，属于数据库管理系统
>
> 5>MySQL:免费的数据库系统，被广泛引用于中小型应用系统，体积小，速度快，总体拥有成本低，开发源代码，2008年被SUN收购，2009年SUN被Oracle收购

### 二.数据库的安装

#### 1.安装

> 1.验证是否安装MySQL
>
> ```python
> 演示命令：
> yangyang@yangyang-virtualmachine:~$ mysql -u root -p		#登录MySQL数据库
> Enter password: 
> ERROR 2002 (HY000): Can't connect to local MySQL server through socket 	'/var/run/mysqld/mysqld.sock' (2)				#报错，说明数据库没有启动
> yangyang@yangyang-virtualmachine:~$ sudo service mysql start		#启动数据库
> yangyang@yangyang-virtualmachine:~$ mysql -u root -p		
> Enter password: 							#输入数据库密码rock1204
> Welcome to the MySQL monitor.  Commands end with ; or \g.		#出现左边的信息说明已经安装
> Your MySQL connection id is 3
> Server version: 5.7.22-0ubuntu0.16.04.1 (Ubuntu)
> 
> Copyright (c) 2000, 2018, Oracle and/or its affiliates. All rights reserved.
> 
> Oracle is a registered trademark of Oracle Corporation and/or its
> affiliates. Other names may be trademarks of their respective
> owners.
> 
> Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
> 
> #退出数据库
> mysql> exit		
> Bye
> ```
>
> 2.如果之前有安装 不能使用的话 可按如下步骤卸载
>
> ```python
> 演示命令：
> #第一步：依次执行下面的语句
> sudo apt-get autoremove --purge mysql-server
> sudo apt-get remove mysql-server
> sudo apt-get autoremove mysql-server
> sudo apt-get remove mysql-common 
> 
> #第二步：清理残留数据
> dpkg -l |grep ^rc|awk '{print $2}' |sudo xargs dpkg -P
> #这个步骤尽量多执行几次，清理干净
> ```
>
> 3.重新安装
>
> 第一步：下载MySQL资源，安装之前请先卸载之前的，一定要卸载干净
> https://dev.mysql.com/downloads/file/?id=477124，进入官网之后直接点击No thanks, just start my download，下载下来的是mysql-apt-config_0.8.10-1_all.deb安装包【注意：如果是其他的则有问题】
> 第二步：在终端里输入下面的命令安装下载的发布包
> sudo dpkg -i 文件路径+文件名　
> 也可以cd到文件目录下，直接执行sudo dekg -i mysql-apt-config_0.8.10-1_all.deb
>
> 第三步：使用以下命令从MySQL APT存储库更新包信息
> sudo apt-get update
>
> 第四步：安装MySQL
> sudo apt-get install mysql-server　
>
> 注意：这里要选择第二个，不然安装之后只有用sudo才能进入MySQL，而且不能使用数据库

#### 2.启动和停止mysql服务

> 查看mysql服务端的状态
>
> 检查MySQL的状态：**sudo service mysql status**
>
> 开启MySQL服务器：**sudo service mysql start**
>
> 关闭MySQL服务器：**sudo service mysql stop**

### 三、SQL概述

#### 1.简介

> Structure Query  Language，结构化查询语言，

#### 2.数据库服务器、数据库和表之间的关系

> 表：为了保存应用实体中的数据，一般会给数据库中创建表，一个数据库可以同时管理多个表
>

#### 3.数据在SQL中的存储形式

> 案例：
>
> User表
>
> id 		name 		age
>
> 1		lisi			10
>
> 2		zhangsan	         18
>
> 说明：
>
> **a.表中的一条数据被称为一条记录【实体】**
>
> **b.表中的一列记录的是不同对象的同一类数据**

#### 4.SQL的分类

> DDL【Data   Definition Language】,数据定义语言，用户创建、修改、删除表结构
>
> DML【Data  Manipulation Language】,数据操作语言，用于对数据表进行增删改的操作
>
> DQL【Data  Query Language】,数据查询语言，用于负责数据表的查询工作
>
> DCL【Data Control Language】：数据控制语言，用来定义访问权限和安全级别

### 四、数据库操作

> 1.概念
>
> ​	数据库管理系统，数据库，表
>
> ​	SQL的分类**：DDL、DML、DQL、DCL**
>
> 2.数据库的使用
>
> ​	DDL:**create**【创建数据库和创建表】    **alter**【操作表】   **drop**【删除表】**表的结构**
>
> ​	DML:**insert into**【给表中插入数据】  **update   set**【需要结合where使用】 **delete、truncate  from**【表中的数据】
>
> ​	DQL：**select  最重要的功能**
>
> ​	where  **相当于if判断**
>
> ​	where like--------->_   %   **模糊查询的时候使用**
>
> ​	as  **给字段起别名，主要用在表中有相同的列**
>
> ​	 ifnull(a,0)   distinct   **当表格中的数据为空时，做一个判断，并重新赋值为**
>
> ​	order     by:asc  **升序排列**     desc **降序排列**    
>
> ​	聚合函数：count **个数**  sum **计算总和** max **计算列中最大值** min **计算列中最小值**  avg **计算列中的平均数**

#### 1.DDL

> 使用关键字：CREATE    ALTER    DROP
>
> 注意：**一般情况下，mysql关键字是大写的，但是为了方便，一般小写**

##### 1.1create创建

> 语法：
>
> ```mysql
> #创建数据库
> CREATE DATABASE database_name;
> 
> #创建表
> CREATE TABLE 表名{
> 		字段1 字段类型[列级别约束条件][默认值]，
> 		字段2 字段类型[列级别约束条件][默认值]，
> 		….
> 		字段n 字段类型[列级别约束条件][默认值]
> 		[表级别约束条件]
> }
> ```
>
> 演示：
>
> ```mysql
> #查询当前数据库服务器中的所有数据库
> mysql> show databases;			    
> +--------------------+	
> | Database           |
> +--------------------+
> | information_schema |
> | mydb1              |
> | mysql              |
> | performance_schema |
> | sys                |
> +--------------------+
> 5 rows in set (0.01 sec)
> 
> #查看当前正在使用的数据库
> mysql> select database();
> +------------+
> | database() |
> +------------+
> | mydb1      |
> +------------+
> 1 row in set (0.00 sec)
> 
> #切换数据库
> mysql> use mydb1;
> Database changed
> 
> #修改数据库的编码
> #第一步：查看切换后该数据库的信息
> mysql> show create database mydb1 \G;
> *************************** 1. row ***************************
>        Database: mydb1
> Create Database: CREATE DATABASE `mydb1` /*!40100 DEFAULT CHARACTER SET latin1 */
> 1 row in set (0.00 sec)
> 
> #第二步：重启一个终端
> #首先进入MySQL存放配置文件的目录
> yangyang@yangyang-virtualmachine:~$ cd /etc/mysql/
> #执行ls，查看下此文件夹下的文件
> yangyang@yangyang-virtualmachine:/etc/mysql$ ls
> conf.d        fabric.cfg       mysql.cnf
> debian.cnf    my.cnf           mysql.conf.d
> debian-start  my.cnf.fallback  mysql-fabric-doctrine-1.4.0.zip
> #会发现有个文件是my.cnf，这个文件是mysql的配置文件
> 
> #第三步：用vim打开my.cnf文件
> yangyang@yangyang-virtualmachine:/etc/mysql$ vim my.cnf
> #打开my.cnf后，会发现在此文件的最后有两行(此配置文件又引用了其他的两个配置文件，我们需要修改的是mysqld.cnf ，这是mysql服务端基础配置文件 )
> !includedir /etc/mysql/conf.d/
> !includedir /etc/mysql/mysql.conf.d/
> 
> #第四步：用vim打开/etc/mysql/mysql.conf.d/mysqld.cnf文件
> #(如果提示不可编辑的话，可以切换账号为root或者用sudo命令)
> yangyang@yangyang-virtualmachine:/etc/mysql$ vim /etc/mysql/mysql.conf.d/mysqld.cnf 
> yangyang@yangyang-virtualmachine:/etc/mysql$ sudo vim /etc/mysql/mysql.conf.d/mysqld.cnf
> [sudo] yangyang 的密码： 
> 
> #第五步
> #打开文件后，在[mysqld]下，添加character-set-server=utf8【注意：是utf8,而不是utf-8】
> [mysqld]
> character-set-server=utf8
> 
> #第六步：重启mysql服务
> yangyang@yangyang-virtualmachine:/etc/mysql$ cd ../..
> yangyang@yangyang-virtualmachine:/$ service mysql restart
>   
> #第七步：回到原来的终端中，退出mysql服务，重新登录
> mysql> exit
> Bye
> yangyang@yangyang-virtualmachine:~$ mysql -u root -p
> Enter password: 
> Welcome to the MySQL monitor.  Commands end with ; or \g.
> Your MySQL connection id is 3
> Server version: 5.7.22-0ubuntu0.16.04.1 (Ubuntu)
> 
> #第八步：用\s查看是否修改成功
> mysql> \s
> --------------
> mysql  Ver 14.14 Distrib 5.7.22, for Linux (x86_64) using  EditLine wrapper
> Server characterset:	utf8
> Db     characterset:	utf8
> Client characterset:	utf8
> Conn.  characterset:	utf8
> 
> #退出数据库
> 演示命令：
> #方式一
> mysql> exit
> Bye
> 
> #方式二
> mysql> quit
> Bye
> 
> #注意：如要再次使用数据库，则需要重新登录
> ```
>
> 总结：
>
> ```mysql
> #1.创建数据库
> create database xxx;
> 
> #2.切换数据库
> use  xxx;
> 
> #3.查看正在使用的数据库的信息
> select database();
> 
> #4.查看当前数据库管理系统中所有的数据库
> show databases;
> 
> #5.退出数据库
> quit / exit
> 
> #6.显示当前数据库中所有的表
> show tables;
> ```

##### 1.2alter操作

> a.语法：
>
> ```mysql
> #1.修改表名
> 语法规则：ALTER TABLE old_table_name RENAME [TO] new_table_name
> 
> #2.修改字段的数据类型
> 语法规则：ALTER TABLE table_name MODIFY 字段名 数据类型
> 修改完成之后可以查看DESC table_name检验结果
> 
> #3.修改字段名
> 语法规则：ALTER TABLE table_name CHANGE 旧字段名 新字段名 数据类型
> 
> #4.添加字段
> 语法规则：ALTER TABLE table_name ADD 新字段名 数据类型 [约束条件] [FIRST|AFTER 已经存在的字段名]
> 
> #5.删除字段
> 语法规则：ALTER TABLE table_name DROP 字段名
> 
> #6.修改字段的排列位置
> 语法规则：ALTER TABLE table_name MODIFY 字段1 数据类型 FIRST|AFTER 字段2
> 	first: 设置成第一个
> 	after 字段2： 在指定字段2的后面
> 	
> #7.删除表的外键约束
> 语法规则：ALTER TABLE table_name DROP FOREIGN KEY 外键约束名
> 
> #8.删除数据表
> #删除没有被关联的表
> 语法规则：DROP TABLE [IF EXISTS] 表1，表2...
> #删除被其他表关联的的表
> 直接删除会出现错误的，操作： 先解除关联 再进行删除
> ```
>
> b.常用数据类型
>
> ```mysql
> 1.数字数据类型
> - INT - 正常大小的整数，可以带符号。如果是有符号的，它允许的范围是从-2147483648到2147483647。如果是无符号，允许的范围是从0到4294967295。 可以指定多达11位的宽度。
> - TINYINT - 一个非常小的整数，可以带符号。如果是有符号，它允许的范围是从-128到127。如果是无符号，允许的范围是从0到255，可以指定多达4位数的宽度。
> - SMALLINT - 一个小的整数，可以带符号。如果有符号，允许范围为-32768至32767。如果无符号，允许的范围是从0到65535，可以指定最多5位的宽度。
> - MEDIUMINT - 一个中等大小的整数，可以带符号。如果有符号，允许范围为-8388608至8388607。 如果无符号，允许的范围是从0到16777215，可以指定最多9位的宽度。
> - BIGINT - 一个大的整数，可以带符号。如果有符号，允许范围为-9223372036854775808到9223372036854775807。如果无符号，允许的范围是从0到18446744073709551615. 可以指定最多20位的宽度。
> - FLOAT(M,D) - 不能使用无符号的浮点数字。可以定义显示长度(M)和小数位数(D)。这不是必需的，并且默认为10,2。其中2是小数的位数，10是数字(包括小数)的总数。小数精度可以到24个浮点。
> - DOUBLE(M,D) - 不能使用无符号的双精度浮点数。可以定义显示长度(M)和小数位数(D)。 这不是必需的，默认为16,4，其中4是小数的位数。小数精度可以达到53位的DOUBLE。 REAL是DOUBLE同义词。
> - DECIMAL(M,D) - 非压缩浮点数不能是无符号的。在解包小数，每个小数对应于一个字节。定义显示长度(M)和小数(D)的数量是必需的。 NUMERIC是DECIMAL的同义词。[decimal]
> 
> 2.日期和时间类型
> - DATE - 以YYYY-MM-DD格式的日期，在1000-01-01和9999-12-31之间。 例如，1973年12月30日将被存储为1973-12-30。
> - DATETIME - 日期和时间组合以YYYY-MM-DD HH:MM:SS格式，在1000-01-01 00:00:00 到9999-12-31 23:59:59之间。例如，1973年12月30日下午3:30，会被存储为1973-12-30 15:30:00。
> - TIMESTAMP - 1970年1月1日午夜之间的时间戳，到2037的某个时候。这看起来像前面的DATETIME格式，无需只是数字之间的连字符; 1973年12月30日下午3点30分将被存储为19731230153000(YYYYMMDDHHMMSS)。
> - TIME - 存储时间在HH:MM:SS格式。
> - YEAR(M) - 以2位或4位数字格式来存储年份。如果长度指定为2(例如YEAR(2))，年份就可以为1970至2069(70〜69)。如果长度指定为4，年份范围是1901-2155，默认长度为4。
> 
> 3.字符串类型
> 虽然数字和日期类型比较有意思，但存储大多数数据都可能是字符串格式。 下面列出了在MySQL中常见的字符串数据类型。
> - CHAR(M) - 固定长度的字符串是以长度为1到255之间个字符长度(例如：CHAR(5))，存储右空格填充到指定的长度。 限定长度不是必需的，它会默认为1。
> - VARCHAR(M) - 可变长度的字符串是以长度为1到255之间字符数(高版本的MySQL超过255); 例如： VARCHAR(25). 创建VARCHAR类型字段时，必须定义长度。 [varchar]
> - BLOB or TEXT - 字段的最大长度是65535个字符。 BLOB是“二进制大对象”，并用来存储大的二进制数据，如图像或其他类型的文件。定义为TEXT文本字段还持有大量的数据; 两者之间的区别是，排序和比较上存储的数据，BLOB大小写敏感，而TEXT字段不区分大小写。不用指定BLOB或TEXT的长度。
> - TINYBLOB 或 TINYTEXT - BLOB或TEXT列用255个字符的最大长度。不指定TINYBLOB或TINYTEXT的长度。
> - MEDIUMBLOB or MEDIUMTEXT - BLOB或TEXT列具有16777215字符的最大长度。不指定MEDIUMBLOB或MEDIUMTEXT的长度。
> - LONGBLOB 或 LONGTEXT -  BLOB或TEXT列具有4294967295字符的最大长度。不指定LONGBLOB或LONGTEXT的长度。
> - ENUM - 枚举，这是一个奇特的术语列表。当定义一个ENUM，要创建它的值的列表，这些是必须用于选择的项(也可以是NULL)。例如，如果想要字段包含“A”或“B”或“C”，那么可以定义为ENUM为 ENUM(“A”，“B”，“C”)也只有这些值(或NULL)才能用来填充这个字段。
> ```

> 注意：主要了解 char 和 varchar 的区别
>
> **char(M)是固定长度的字符串， 在定义时指定字符串列长。当保存数据时如果长度不够在右侧填充空格以达到指定的长度。M 表示列的长度，M 的取值范围是0-255个字符**
>
> **varchar(M)是长度可变的字符串，M 表示最大的列长度。M 的取值范围是0-65535。varchar的最大实际长度是由最长的行的大小和使用的字符集确定的，而实际占用的空间为字符串的实际长度+1**
>
> **主要使用的数据类型：**
>
> **​	数字型数据类型：int float  double  decimal**
>
> **​	日期类：date**
>
> **	字符串：varchar(num)   blob【二进制】**
>
> c.需求：创建一个员工表【图3】
>
> 演示：
>
> ```mysql
> #切换数据库
> mysql> use mydb1			
> Database changed
> #查看当前正在使用的数据库
> mysql> select database();	
> +------------+
> | database() |
> +------------+
> | mydb1      |
> +------------+
> 1 row in set (0.00 sec)
> 
> #在当前数据库下创建新的表
> mysql> create table worker(			
>     -> id int(11),
>     -> name varchar(20),
>     -> gender varchar(10),
>     -> brithday date,
>     -> entry_date date,
>     -> job varchar(20),
>     -> salary double,
>     -> resume blob
>     -> );
> Query OK, 0 rows affected (0.02 sec)
> 
> #显示当前数据库中的所有表
> mysql> show tables;			
> +-----------------+
> | Tables_in_mydb1 |
> +-----------------+
> | worker          |
> +-----------------+
> 1 row in set (0.00 sec)
> 
> #显示指定表中的所有字段
> mysql> desc worker;			
> +------------+-------------+------+-----+---------+-------+
> | Field      | Type        | Null | Key | Default | Extra |
> +------------+-------------+------+-----+---------+-------+
> | id         | int(11)     | YES  |     | NULL    |       |
> | name       | varchar(20) | YES  |     | NULL    |       |
> | gender     | varchar(10) | YES  |     | NULL    |       |
> | brithday   | date        | YES  |     | NULL    |       |
> | entry_date | date        | YES  |     | NULL    |       |
> | job        | varchar(20) | YES  |     | NULL    |       |
> | salary     | double      | YES  |     | NULL    |       |
> | resume     | blob        | YES  |     | NULL    |       |
> +------------+-------------+------+-----+---------+-------+
> 8 rows in set (0.01 sec)
> 
> #增加字段image
> mysql> alter table worker add image blob;
> Query OK, 0 rows affected (0.04 sec)
> Records: 0  Duplicates: 0  Warnings: 0
> 
> mysql> desc worker;
> +------------+-------------+------+-----+---------+-------+
> | Field      | Type        | Null | Key | Default | Extra |
> +------------+-------------+------+-----+---------+-------+
> | id         | int(11)     | YES  |     | NULL    |       |
> | name       | varchar(20) | YES  |     | NULL    |       |
> | gender     | varchar(10) | YES  |     | NULL    |       |
> | brithday   | date        | YES  |     | NULL    |       |
> | entry_date | date        | YES  |     | NULL    |       |
> | job        | varchar(20) | YES  |     | NULL    |       |
> | salary     | double      | YES  |     | NULL    |       |
> | resume     | blob        | YES  |     | NULL    |       |
> | image      | blob        | YES  |     | NULL    |       |
> +------------+-------------+------+-----+---------+-------+
> 9 rows in set (0.00 sec)
> 
> #修改job的长度为60
> mysql> alter table worker modify job varchar(60);
> Query OK, 0 rows affected (0.00 sec)
> Records: 0  Duplicates: 0  Warnings: 0
> 
> mysql> desc worker;
> +------------+-------------+------+-----+---------+-------+
> | Field      | Type        | Null | Key | Default | Extra |
> +------------+-------------+------+-----+---------+-------+
> | id         | int(11)     | YES  |     | NULL    |       |
> | name       | varchar(20) | YES  |     | NULL    |       |
> | gender     | varchar(10) | YES  |     | NULL    |       |
> | brithday   | date        | YES  |     | NULL    |       |
> | entry_date | date        | YES  |     | NULL    |       |
> | job        | varchar(60) | YES  |     | NULL    |       |
> | salary     | double      | YES  |     | NULL    |       |
> | resume     | blob        | YES  |     | NULL    |       |
> | image      | blob        | YES  |     | NULL    |       |
> +------------+-------------+------+-----+---------+-------+
> 9 rows in set (0.00 sec)
> 
> #删除image字段
> mysql> alter table worker drop image;
> Query OK, 0 rows affected (0.01 sec)
> Records: 0  Duplicates: 0  Warnings: 0
> 
> mysql> desc worker;
> +------------+-------------+------+-----+---------+-------+
> | Field      | Type        | Null | Key | Default | Extra |
> +------------+-------------+------+-----+---------+-------+
> | id         | int(11)     | YES  |     | NULL    |       |
> | name       | varchar(20) | YES  |     | NULL    |       |
> | gender     | varchar(10) | YES  |     | NULL    |       |
> | brithday   | date        | YES  |     | NULL    |       |
> | entry_date | date        | YES  |     | NULL    |       |
> | job        | varchar(60) | YES  |     | NULL    |       |
> | salary     | double      | YES  |     | NULL    |       |
> | resume     | blob        | YES  |     | NULL    |       |
> +------------+-------------+------+-----+---------+-------+
> 8 rows in set (0.00 sec)
> 
> #对表名重新命名
> #方式一
> mysql> rename table worker to user;
> Query OK, 0 rows affected (0.00 sec)
> #方式二
> mysql> alter table  worker rename to user;
> Query OK, 0 rows affected (0.00 sec)
> 
> #查看表格的创建细节
> mysql> desc worker;
> ERROR 1146 (42S02): Table 'mydb1.worker' doesn't exist     #报错：worker表不存在，说明重命名成功
> 
> #查看表的信息
> mysql> desc user;
> +------------+-------------+------+-----+---------+-------+
> | Field      | Type        | Null | Key | Default | Extra |
> +------------+-------------+------+-----+---------+-------+
> | id         | int(11)     | YES  |     | NULL    |       |
> | name       | varchar(20) | YES  |     | NULL    |       |
> | gender     | varchar(10) | YES  |     | NULL    |       |
> | brithday   | date        | YES  |     | NULL    |       |
> | entry_date | date        | YES  |     | NULL    |       |
> | job        | varchar(60) | YES  |     | NULL    |       |
> | salary     | double      | YES  |     | NULL    |       |
> | resume     | blob        | YES  |     | NULL    |       |
> +------------+-------------+------+-----+---------+-------+
> 8 rows in set (0.00 sec)
> 
> 
> #查看创建表的详细信息
> mysql> show create table user;
> | Table | Create Table                                                                                                   
> | user  | CREATE TABLE `user` (
>   `id` int(11) DEFAULT NULL,
>   `name` varchar(20) DEFAULT NULL,
>   `gender` varchar(10) DEFAULT NULL,
>   `brithday` date DEFAULT NULL,
>   `entry_date` date DEFAULT NULL,
>   `job` varchar(60) DEFAULT NULL,
>   `salary` double DEFAULT NULL,
>   `resume` blob
> ) ENGINE=InnoDB DEFAULT CHARSET=latin1 |
> 
> 1 row in set (0.00 sec)
> 
> 
> #修改表的字符集为gbk
> mysql> alter table user character set gbk;	
> Query OK, 0 rows affected (0.00 sec)
> Records: 0  Duplicates: 0  Warnings: 0
> 
> mysql> show create table user;			#查看信息，已经改为gbk
> 
> | Table | Create Table                                       
> | user  | CREATE TABLE `user` (
>   `id` int(11) DEFAULT NULL,
>   `name` varchar(20) CHARACTER SET latin1 DEFAULT NULL,
>   `gender` varchar(10) CHARACTER SET latin1 DEFAULT NULL,
>   `brithday` date DEFAULT NULL,
>   `entry_date` date DEFAULT NULL,
>   `job` varchar(60) CHARACTER SET latin1 DEFAULT NULL,
>   `salary` double DEFAULT NULL,
>   `resume` blob
> ) ENGINE=InnoDB DEFAULT CHARSET=gbk |
> 
> 1 row in set (0.00 sec)
> 
> 将列名name修改为username
> mysql> alter table user change name username varchar(100);
> Query OK, 0 rows affected (0.02 sec)
> Records: 0  Duplicates: 0  Warnings: 0
> 
> mysql> desc user;
> +------------+--------------+------+-----+---------+-------+
> | Field      | Type         | Null | Key | Default | Extra |
> +------------+--------------+------+-----+---------+-------+
> | id         | int(11)      | YES  |     | NULL    |       |
> | username   | varchar(100) | YES  |     | NULL    |       |
> | gender     | varchar(10)  | YES  |     | NULL    |       |
> | brithday   | date         | YES  |     | NULL    |       |
> | entry_date | date         | YES  |     | NULL    |       |
> | job        | varchar(60)  | YES  |     | NULL    |       |
> | salary     | double       | YES  |     | NULL    |       |
> | resume     | blob         | YES  |     | NULL    |       |
> +------------+--------------+------+-----+---------+-------+
> 8 rows in set (0.00 sec)
> 
> ```

##### 1.3drop删除

> 语法：
>
> ```mysql
> DROP DATABASE database_name
> ```
>
> 演示：
>
> ```mysql
> mysql> drop table user;
> Query OK, 0 rows affected (0.00 sec)
> 
> mysql> show tables;
> Empty set (0.00 sec)
> ```

#### 2.DML

##### 2.1insert插入

> 语法：
>
> ```mysql
> #单行插入
> INSERT INTO table_name (field1, field2,...fieldN) VALUES(value1, value2,...valueN);
>                        
> #多行插入[批量插入]
> INSERT INTO table_name (field1, field2,...fieldN)
>                        VALUES
>                        (value1, value2,...valueN),
>                        (value12, value22,...valueNN)...;
> ```
>
> 注意：
> **a.列名和列值的类型、个数以及顺序一一对应**
> **b.可以把列名当做Python中的形参，把列值当做实参**
> **c.值不能超出列定义的长度**
> **d.如果插入的是空值，写null** 
>
> **e.插入的是日期，和字符串一样，使用引号括起来**

> 演示：
>
> ```mysql
> mysql> use mydb1;
> Database changed
> mysql> show tables;
> Empty set (0.00 sec)
> 
> mysql> create table worker(
>     -> id int(11),
>     -> name varchar(20),
>     -> gender varchar(10),
>     -> salary double
>     -> );
> Query OK, 0 rows affected (0.01 sec)
> 
> mysql> show tables;                                                             +-----------------+
> | Tables_in_mydb1 |
> +-----------------+
> | worker          |
> +-----------------+
> 1 row in set (0.00 sec)
> 
> mysql> desc worker;
> +--------+-------------+------+-----+---------+-------+
> | Field  | Type        | Null | Key | Default | Extra |
> +--------+-------------+------+-----+---------+-------+
> | id     | int(11)     | YES  |     | NULL    |       |
> | name   | varchar(20) | YES  |     | NULL    |       |
> | gender | varchar(10) | YES  |     | NULL    |       |
> | salary | double      | YES  |     | NULL    |       |
> +--------+-------------+------+-----+---------+-------+
> 4 rows in set (0.00 sec)
> 
> #插入单条数据
> mysql> insert into worker(id,name,gender,salary) values(1,'tom','b',4000);
> Query OK, 1 row affected (0.02 sec)
> 
> mysql> insert into worker(id,name,gender,salary) values(2,'jack','b',6000);
> Query OK, 1 row affected (0.01 sec)
> 
> #如果给每个字段都赋值，就可以省略掉字段的书写
> mysql> insert into worker values(3,'rose','g',6000);
> Query OK, 1 row affected (0.01 sec)
> 
> mysql> desc worker;
> +--------+-------------+------+-----+---------+-------+
> | Field  | Type        | Null | Key | Default | Extra |
> +--------+-------------+------+-----+---------+-------+
> | id     | int(11)     | YES  |     | NULL    |       |
> | name   | varchar(20) | YES  |     | NULL    |       |
> | gender | varchar(10) | YES  |     | NULL    |       |
> | salary | double      | YES  |     | NULL    |       |
> +--------+-------------+------+-----+---------+-------+
> 4 rows in set (0.00 sec)
> 
> mysql> select * from worker;
> +------+------+--------+--------+
> | id   | name | gender | salary |
> +------+------+--------+--------+
> |    1 | tom  | b      |   4000 |
> |    2 | jack | b      |   6000 |
> |    3 | rose | g      |   6000 |
> +------+------+--------+--------+
> 3 rows in set (0.00 sec)
> 
> #一次性插入多条数据【批量插入】
> mysql> insert into worker(id,name,gender,salary) values(4,'bob','b',1500),(5,'hello','g',5500),(6,'abc','b',6600);
> Query OK, 3 rows affected (0.01 sec)
> Records: 3  Duplicates: 0  Warnings: 0
> 
> mysql> select * from worker;                                                    +------+-------+--------+--------+
> | id   | name  | gender | salary |
> +------+-------+--------+--------+
> |    1 | tom   | b      |   4000 |
> |    2 | jack  | b      |   6000 |
> |    3 | rose  | g      |   6000 |
> |    4 | bob   | b      |   1500 |
> |    5 | hello | g      |   5500 |
> |    6 | abc   | b      |   6600 |
> +------+-------+--------+--------+
> 6 rows in set (0.00 sec)
> ```

##### 2.2update更新

> 语法：
>
> ```mysql
> UPDATE table_name SET field1=new-value1, field2=new-value2  [WHERE Clause]
> 
> 注意：
> 	a.完全可以更新一个字段或者多个字段
> 	b.where相当于Python中的if语句
> 	c.可以指定任何条件到where子句中
> 	d.如果没有where子句，则默认所有的行都被同时更新为指定的操作
> ```
>
> 演示：
>
> ```mysql
> #1.将所有员工的薪水修改为5000
> mysql> update worker set salary=5000;
> Query OK, 6 rows affected (0.01 sec)
> Rows matched: 6  Changed: 6  Warnings: 0
> 
> mysql> select * from worker;
> +------+-------+--------+--------+
> | id   | name  | gender | salary |
> +------+-------+--------+--------+
> |    1 | tom   | b      |   5000 |
> |    2 | jack  | b      |   5000 |
> |    3 | rose  | g      |   5000 |
> |    4 | bob   | b      |   5000 |
> |    5 | hello | g      |   5000 |
> |    6 | abc   | b      |   5000 |
> +------+-------+--------+--------+
> 6 rows in set (0.00 sec)
> 
> #2.将tom的薪水改为3000元
> mysql> update worker set salary=3000 where name='tom';
> Query OK, 1 row affected (0.01 sec)
> Rows matched: 1  Changed: 1  Warnings: 0
> 
> mysql> select * from worker;
> +------+-------+--------+--------+
> | id   | name  | gender | salary |
> +------+-------+--------+--------+
> |    1 | tom   | b      |   3000 |
> |    2 | jack  | b      |   5000 |
> |    3 | rose  | g      |   5000 |
> |    4 | bob   | b      |   5000 |
> |    5 | hello | g      |   5000 |
> |    6 | abc   | b      |   5000 |
> +------+-------+--------+--------+
> 6 rows in set (0.00 sec)
> 
> #3.将jack的薪水改为10000，并将性别改为g
> mysql> update worker set salary=10000,gender='g' where name='jack';
> Query OK, 1 row affected (0.01 sec)
> Rows matched: 1  Changed: 1  Warnings: 0
> 
> mysql> select * from worker;
> +------+-------+--------+--------+
> | id   | name  | gender | salary |
> +------+-------+--------+--------+
> |    1 | tom   | b      |   3000 |
> |    2 | jack  | g      |  10000 |
> |    3 | rose  | g      |   5000 |
> |    4 | bob   | b      |   5000 |
> |    5 | hello | g      |   5000 |
> |    6 | abc   | b      |   5000 |
> +------+-------+--------+--------+
> 6 rows in set (0.00 sec)
> 
> #4.将rose的薪水在原来的基础上增加1000
> mysql> update worker set salary=salary+1000 where name='rose';
> Query OK, 1 row affected (0.01 sec)
> Rows matched: 1  Changed: 1  Warnings: 0
> 
> mysql> select * from worker;
> +------+-------+--------+--------+
> | id   | name  | gender | salary |
> +------+-------+--------+--------+
> |    1 | tom   | b      |   3000 |
> |    2 | jack  | g      |  10000 |
> |    3 | rose  | g      |   6000 |
> |    4 | bob   | b      |   5000 |
> |    5 | hello | g      |   5000 |
> |    6 | abc   | b      |   5000 |
> +------+-------+--------+--------+
> 6 rows in set (0.01 sec)
> 
> #5.将abc的薪水改为6000
> update worker set salary=6000 where name='abc';
> #6.将bob的性别改为b
> update worker set gender='b' where name='bob';
> ```

##### 1>where子句

> 语法：
>
> 注意：where子句其实就是一个操作符，类似于Python中的if语句，可以做数据的筛选
>
> | 操作符      | 说明                      |
> | ----------- | ------------------------- |
> | =           | 相等                      |
> | <> / !=     | 不相等                    |
> | <           | 小于                      |
> | <=          | 小于等于                  |
> | >           | 大于                      |
> | >=          | 大于等于                  |
> | IN(A，B)    | A 和 B 之间               |
> | between and | 位于两值之间              |
> | AND         | 连接多个表达式 并且的关系 |

##### 2.3delete删除

> 语法：
>
> ```mysql
> DELETE FROM table_name [WHERE Clause]
> 
> 注意：
> 	a.如果where子句没有指定，则默认将表中的数据全部删除
> 	b.可以指定任何条件在where子句中
> ```

> 演示：
>
> ```mysql
> #1.删除表中tom的全部数据
> mysql> delete from worker where name='tom';
> Query OK, 1 row affected (0.01 sec)
> 
> mysql> select * from worker;
> +------+-------+--------+--------+
> | id   | name  | gender | salary |
> +------+-------+--------+--------+
> |    2 | jack  | g      |  10000 |
> |    3 | rose  | g      |   6000 |
> |    4 | bob   | b      |   5000 |
> |    5 | hello | g      |   5000 |
> |    6 | abc   | b      |   5000 |
> +------+-------+--------+--------+
> 5 rows in set (0.00 sec)
> 
> #2.删除表中的所有数据
> mysql> delete from worker;
> Query OK, 5 rows affected (0.01 sec)
> 
> mysql> select * from worker;
> Empty set (0.00 sec)
> 
> mysql> truncate table worker;
> Query OK, 0 rows affected (0.02 sec)
> 
> #3.删除表
> mysql> drop table worker;
> Query OK, 0 rows affected (0.01 sec)
> 
> mysql> show tables;
> Empty set (0.00 sec)
> 
> 注意：
> delete:删除表中的数据，表结构还在，删除之后的数据可以找回
> truncate:不但删除表中的数据，还drop掉了表结构，删除的数据是不能找回的，执行速度比delete快
> ```

#### 3.DQL

> 数据库执行DQL语言不会对数据库中的数据发生任何改变，而是让数据库发送查询结果到客户端
>
> 查询返回的结果其实是一张虚拟表
>
> 语法：
>
> ```mysql
> SELECT 列名 FROM 表名【WHERE --> GROUP BY -->HAVING--> ORDER BY --->limit】
> ```

##### 3.1基础查询

> 演示：
>
> ```mysql
> #1.查询所有列
> mysql> select * from student;
> +------+----------+------+--------+
> | id   | name     | age  | gender |
> +------+----------+------+--------+
> | 1    | aaaa     |   19 | female |
> | 2    | bbbbbbbb |   20 | male   |
> | 3    | cc       |   15 | male   |
> | 4    | ddd      |   16 | female |
> | 5    | eee      |   20 | female |
> +------+----------+------+--------+
> 5 rows in set (0.00 sec)
> 
> 
> #2.查询指定列
> mysql> select id,name,gender from student;
> +------+----------+--------+
> | id   | name     | gender |
> +------+----------+--------+
> | 1    | aaaa     | female |
> | 2    | bbbbbbbb | male   |
> | 3    | cc       | male   |
> | 4    | ddd      | female |
> | 5    | eee      | female |
> +------+----------+--------+
> 5 rows in set (0.00 sec)
> ```

##### 3.2条件查询

> 主要结合where的使用
>
> between...and:介于。。和。。。之间
>
> and：逻辑与
>
> or：逻辑或
>
> in：类似于Python中的成员运算符
>
> not in:
>
> is:类似于Python中的身份运算符
>
> is not:
>
> 演示：
>
> ```mysql
> #1.查询性别为女，并且年龄为20的记录
> mysql> select * from student where gender='female' and age=20;
> +------+------+------+--------+
> | id   | name | age  | gender |
> +------+------+------+--------+
> | 5    | eee  |   20 | female |
> +------+------+------+--------+
> 1 row in set (0.00 sec)
> 
> #2.查询编号为1或者姓名为ddd的记录
> mysql> select * from student where id='1' or name='ddd';
> +------+------+------+--------+
> | id   | name | age  | gender |
> +------+------+------+--------+
> | 1    | aaaa |   19 | female |
> | 4    | ddd  |   16 | female |
> +------+------+------+--------+
> 2 rows in set (0.00 sec)
> 
> #3.查询编号分别为1,2,3的记录
> mysql> select * from student where id='1' or id='2' or id='3';
> +------+----------+------+--------+
> | id   | name     | age  | gender |
> +------+----------+------+--------+
> | 1    | aaaa     |   19 | female |
> | 2    | bbbbbbbb |   20 | male   |
> | 3    | cc       |   15 | male   |
> +------+----------+------+--------+
> 3 rows in set (0.00 sec)
> #简写形式
> mysql> select * from student where id in('1','2','3');
> +------+----------+------+--------+
> | id   | name     | age  | gender |
> +------+----------+------+--------+
> | 1    | aaaa     |   19 | female |
> | 2    | bbbbbbbb |   20 | male   |
> | 3    | cc       |   15 | male   |
> +------+----------+------+--------+
> 3 rows in set (0.00 sec)
> 
> #4.查询编号不为1,2,3的记录
> mysql> select * from student where id not in('1','2','3');
> +------+------+------+--------+
> | id   | name | age  | gender |
> +------+------+------+--------+
> | 4    | ddd  |   16 | female |
> | 5    | eee  |   20 | female |
> +------+------+------+--------+
> 2 rows in set (0.00 sec)
> 
> 
> #5.查询年龄为null的记录
> mysql> select * from student where age is null;
> Empty set (0.00 sec)
> 
> #6.查询年龄在15~20之间的记录
> mysql> select * from student where age>=15 and age<=20;
> +------+----------+------+--------+
> | id   | name     | age  | gender |
> +------+----------+------+--------+
> | 1    | aaaa     |   19 | female |
> | 2    | bbbbbbbb |   20 | male   |
> | 3    | cc       |   15 | male   |
> | 4    | ddd      |   16 | female |
> | 5    | eee      |   20 | female |
> +------+----------+------+--------+
> 5 rows in set (0.00 sec)
> #简写形式
> mysql> select * from student where age between 15 and 20;
> +------+----------+------+--------+
> | id   | name     | age  | gender |
> +------+----------+------+--------+
> | 1    | aaaa     |   19 | female |
> | 2    | bbbbbbbb |   20 | male   |
> | 3    | cc       |   15 | male   |
> | 4    | ddd      |   16 | female |
> | 5    | eee      |   20 | female |
> +------+----------+------+--------+
> 5 rows in set (0.00 sec)
> 
> #7.查询性别非男的记录
> #方式一
> mysql> select * from student where gender='female';
> +------+------+------+--------+
> | id   | name | age  | gender |
> +------+------+------+--------+
> | 1    | aaaa |   19 | female |
> | 4    | ddd  |   16 | female |
> | 5    | eee  |   20 | female |
> +------+------+------+--------+
> 3 rows in set (0.00 sec)
> #方式二
> mysql> select * from student where gender!='male';
> +------+------+------+--------+
> | id   | name | age  | gender |
> +------+------+------+--------+
> | 1    | aaaa |   19 | female |
> | 4    | ddd  |   16 | female |
> | 5    | eee  |   20 | female |
> +------+------+------+--------+
> 3 rows in set (0.00 sec)
> #方式三
> mysql> select * from student where gender<>'male';
> +------+------+------+--------+
> | id   | name | age  | gender |
> +------+------+------+--------+
> | 1    | aaaa |   19 | female |
> | 4    | ddd  |   16 | female |
> | 5    | eee  |   20 | female |
> +------+------+------+--------+
> 3 rows in set (0.00 sec)
> ```

##### 3.3模糊查询

> **where子句中=表示精准查询**
>
> **like：一般情况下结合where子句使用**
>
> **通配符：**
>
> **	_:匹配任意一个字符   几个下划线就代表有几个确定的数**
>
> **	%：匹配0~n个字符【n大于等于1】**
>
> 演示：
>
> ```mysql
> #1.查询姓名由4个字符组成的记录
> mysql> select * from student where name like '____';
> +------+------+------+--------+
> | id   | name | age  | gender |
> +------+------+------+--------+
> | 1    | aaaa |   19 | female |
> +------+------+------+--------+
> 1 row in set (0.00 sec)
> 
> #2.查询姓名由3个字符组成的记录，并且最后一个字母为c的记录
> mysql> select * from student where name like '__c';
> Empty set (0.00 sec)
> 
> #3.查询以a开头的记录
> mysql> select * from student where name like 'a%';
> +------+------+------+--------+
> | id   | name | age  | gender |
> +------+------+------+--------+
> | 1    | aaaa |   19 | female |
> +------+------+------+--------+
> 1 row in set (0.01 sec)
> 
> #4.查询姓名中包含b的记录
> mysql> select * from student where name like '%b%';
> +------+----------+------+--------+
> | id   | name     | age  | gender |
> +------+----------+------+--------+
> | 2    | bbbbbbbb |   20 | male   |
> +------+----------+------+--------+
> 1 row in set (0.00 sec)
> 
> #5.查询姓名中第2个字母为c的记录
> mysql> select * from student where name like '_c%';
> +------+------+------+--------+
> | id   | name | age  | gender |
> +------+------+------+--------+
> | 3    | cc   |   15 | male   |
> +------+------+------+--------+
> 1 row in set (0.00 sec)
> ```

##### 3.4字段控制查询

> **as:起别名，用法 ：select 字段 as 别名**
>
> **ifnull:将null转换为其他数据，用法，ifnull(字段名，其他数据)**
>
> **distinct:去除重复记录**      **select distinct 字段名 from 表名;**
>
> 演示；
>
> ```mysql
> #1.去除重复记录
> mysql> select id from student;
> +------+
> | id   |
> +------+
> | 1    |
> | 2    |
> | 3    |
> | 4    |
> | 5    |
> | 1    |
> +------+
> 6 rows in set (0.00 sec)
> 
> mysql> select distinct id from student;
> +------+
> | id   |
> +------+
> | 1    |
> | 2    |
> | 3    |
> | 4    |
> | 5    |
> +------+
> 5 rows in set (0.01 sec)
> 
> #2.给列名起别名
> mysql> select name,gender  from student;
> +----------+--------+
> | name     | gender |
> +----------+--------+
> | aaaa     | female |
> | bbbbbbbb | male   |
> | cc       | male   |
> | ddd      | female |
> | eee      | female |
> | ffff     | male   |
> +----------+--------+
> 6 rows in set (0.00 sec)
> 
> 
> mysql> select name as 姓名,gender as 性别  from student;
> +----------+--------+
> | 姓名     | 性别   |
> +----------+--------+
> | aaaa     | female |
> | bbbbbbbb | male   |
> | cc       | male   |
> | ddd      | female |
> | eee      | female |
> | ffff     | male   |
> +----------+--------+
> 6 rows in set (0.00 sec)
> 
> mysql> select name  姓名1,gender  性别1  from student;
> +----------+---------+
> | 姓名1    | 性别1   |
> +----------+---------+
> | aaaa     | female  |
> | bbbbbbbb | male    |
> | cc       | male    |
> | ddd      | female  |
> | eee      | female  |
> | ffff     | male    |
> +----------+---------+
> 6 rows in set (0.00 sec)
> 
> 
> #3.将null转化
> #查看学生的年龄和学号之和
> mysql> select id+age  from student;
> +--------+
> | id+age |
> +--------+
> |     20 |
> |     22 |
> |     18 |
> |     20 |
> |     25 |
> |     31 |
> +--------+
> 6 rows in set (0.01 sec)
> 
> mysql> select age+ifnull(id,0)  from student;
> +------------------+
> | age+ifnull(id,0) |
> +------------------+
> |               20 |
> |               22 |
> |               18 |
> |               20 |
> |               25 |
> |               31 |
> +------------------+
> 6 rows in set (0.00 sec)
> ```

##### 3.5排序

> **order by:指定数据返回的顺序**
>
> **​	asc：ascending,升序**
>
> **​	desc:descending，降序**
>
> **用法：select from  表 order by  xxx**
>
> 演示：
>
> ```mysql
> #1.查询所有的记录，按照年龄升序排序
> mysql> select * from student order by age asc;
> +------+----------+------+--------+
> | id   | name     | age  | gender |
> +------+----------+------+--------+
> | 3    | cc       |   15 | male   |
> | 4    | ddd      |   16 | female |
> | 1    | aaaa     |   19 | female |
> | 2    | bbbbbbbb |   20 | male   |
> | 5    | eee      |   20 | female |
> | 1    | ffff     |   30 | male   |
> +------+----------+------+--------+
> 6 rows in set (0.00 sec)
> 
> #2.查询所有学生记录，按照年龄降序排序，如果年龄相等，则按照编号进行升序排序
> mysql> select * from student order by age desc,id asc;
> +------+----------+------+--------+
> | id   | name     | age  | gender |
> +------+----------+------+--------+
> | 1    | ffff     |   30 | male   |
> | 2    | bbbbbbbb |   20 | male   |
> | 5    | eee      |   20 | female |
> | 1    | aaaa     |   19 | female |
> | 4    | ddd      |   16 | female |
> | 3    | cc       |   15 | male   |
> +------+----------+------+--------+
> 6 rows in set (0.00 sec)
> ```

##### 3.6聚合函数

> 聚合函数主要用来做纵向运算
>
> ###### 1》count():统计指定列不为null的记录行数
>
> ```mysql
> #1.查询年龄大于20的人数
> mysql> select count(*)  from student where age>20;
> +----------+
> | count(*) |
> +----------+
> |        1 |
> +----------+
> 1 row in set (0.00 sec)
> 
> 
> #2.查询年龄和编号之和大于20的条数
> mysql> select count(*) from student where age+ifnull(id,0)>20;
> +----------+
> | count(*) |
> +----------+
> |        3 |
> +----------+
> 1 row in set (0.00 sec)
> ```
>
> ###### 2>sum():计算指定列的数值和
>
> ```mysql
> #1.查询所有学生的年龄和
> mysql> select sum(age) from student;
> +----------+
> | sum(age) |
> +----------+
> |      120 |
> +----------+
> 1 row in set (0.01 sec)
> 
> #2.查询所有学生的年龄和，以及所有学生的编号和
> mysql> select sum(age),sum(id) from student;
> +----------+---------+
> | sum(age) | sum(id) |
> +----------+---------+
> |      120 |      16 |
> +----------+---------+
> 1 row in set (0.00 sec)
> ```
>
> ###### 3>求指定列中的最大值和最小值
>
> max():
>
> min():
>
> ```mysql
> #求最大年龄和最小年龄
> mysql> select max(age),min(age) from student;
> +----------+----------+
> | max(age) | min(age) |
> +----------+----------+
> |       30 |       15 |
> +----------+----------+
> 1 row in set (0.00 sec)
> ```
>
> ###### 4>avg()
>
> average:平均数，
>
> ```mysql
> #查询所有学生的平均年龄
> mysql> select avg(age) from student;
> +----------+
> | avg(age) |
> +----------+
> |  20.0000 |
> +----------+
> 1 row in set (0.00 sec)
> ```
>
> 总结：
>
> 查询关键字的书写顺序：select 聚合函数  from where order by

#### 综合练习：创建表，按照要求操作

> ```mysql
> #建学生信息表student
> create table student(
> sno varchar(20),
> sname varchar(20),
> ssex varchar(20),
> sbirthday datetime,
> class varchar(20)
> );
> #建立成绩表
> create table score
> (
> sno varchar(20),
> cno varchar(20),
> degree decimal
> );
> #添加学生信息
> insert into student values('108','曾华','男','1977-09-01','95033');
> insert into student values('105','匡明','男','1975-10-02','95031');
> insert into student values('107','王丽','女','1976-01-23','95033');
> insert into student values('101','李军','男','1976-02-20','95033');
> insert into student values('109','王芳','女','1975-02-10','95031');
> insert into student values('103','陆君','男','1974-06-03','95031');
> #添加成绩表
> insert into score values('103','3-245','86');
> insert into score values('105','3-245','75');
> insert into score values('109','3-245','68');
> insert into score values('103','3-105','92');
> insert into score values('105','3-105','88');
> insert into score values('109','3-105','76');
> insert into score values('103','3-105','64');
> insert into score values('105','3-105','91');
> insert into score values('109','3-105','78');
> insert into score values('103','6-166','85');
> insert into score values('105','6-166','79');
> insert into score values('109','6-166','81');
> 
> #1、 查询Student表中的所有记录的Sname、Ssex和Class列
> #2、 查询教师所有的单位即不重复的Depart列
> #3、 查询Student表的所有记录
> #4、查询Score表中成绩在60到80之间的所有记录
> #5、 查询Score表中成绩为85，86或88的记录
> #6、 查询Student表中“95031”班或性别为“女”的同学记录
> #7、 以Class降序查询Student表的所有记录
> #8、 以Cno升序、Degree降序查询Score表的所有记录
> #9、 查询“95031”班的学生人数
> #10、查询Score表中的最高分的学生学号和课程号
> #11、查询每门课的平均成绩
> #12、查询Score表中至少有5名学生选修的并以3开头的课程的平均分数
> #13、查询分数大于70，小于90的Sno列
> ```

##### 3.7分组查询

> group by：分组查询
>
> having：有...,表示条件，类似于where的用法
>
> 演示：
>
> ```mysql
> #1.查询各个部门的人数
> mysql> select count(*) from emp group by deptno;
> +----------+
> | count(*) |
> +----------+
> |        2 |
> |        2 |
> |        4 |
> +----------+
> 3 rows in set (0.00 sec)
> 
> #2.查询每个部门的部门编号和每个部门的工资和
> mysql> select deptno,sum(sal) from emp group by deptno;
> +--------+----------+
> | deptno | sum(sal) |
> +--------+----------+
> |     10 |  7450.00 |
> |     20 |  3800.00 |
> |     30 |  8675.00 |
> +--------+----------+
> 3 rows in set (0.00 sec)
> 
> 
> #3.查询每个部门的部门编号和每个部门的人数
> mysql> select deptno,count(*) from emp group by deptno;
> +--------+----------+
> | deptno | count(*) |
> +--------+----------+
> |     10 |        2 |
> |     20 |        2 |
> |     30 |        4 |
> +--------+----------+
> 3 rows in set (0.00 sec)
> 
> 
> #4.查询每个部门的部门编号和每个部门工资大于1500的人数
> mysql> select deptno,count(*) from emp where sal>1500 group by deptno;
> +--------+----------+
> | deptno | count(*) |
> +--------+----------+
> |     10 |        2 |
> |     20 |        1 |
> |     30 |        3 |
> +--------+----------+
> 3 rows in set (0.01 sec)
> 
> 
> #5.查询工资总和大于7000的部门编号以及工资和
> mysql> select deptno,sum(sal) from emp group by deptno having sum(sal)>9000;
> Empty set (0.00 sec)
> 
> mysql> select deptno,sum(sal) from emp group by deptno having sum(sal)>7000;
> +--------+----------+
> | deptno | sum(sal) |
> +--------+----------+
> |     10 |  7450.00 |
> |     30 |  8675.00 |
> +--------+----------+
> 2 rows in set (0.00 sec)
> ```
>
> 总结：
>
> ​	having和where的区别
>
> ​	a.二者都表示对数据执行条件
>
> ​	b.having是在分组之后对数据进行过滤
>
> ​	  where是在分组之前对数据进行过滤
>
> ​	c.having后面可以使用聚合函数
>
> ​          where后面不可以使用聚合函数
>
> 演示：
>
> ```mysql
> #查询工资大于1500，工资总和大于6000的部门编号和工资和
> mysql> select deptno,sum(sal) from emp where sal>1500 group by deptno having sum(sal)>6000;
> +--------+----------+
> | deptno | sum(sal) |
> +--------+----------+
> |     10 |  7450.00 |
> |     30 |  7425.00 |
> +--------+----------+
> 2 rows in set (0.00 sec)
> ```

##### 3.8分页查询

> limit：用来限定查询的起始行，以及总行数
>
> 演示：
>
> ```mysql
> #1.查询4行记录，起始行从0开始
> mysql> select * from emp limit 0,4;
> +-------+--------+----------+------+------------+---------+---------+--------+
> | empno | enname | job      | mgr  | hiredate   | sal     | comm    | deptno |
> +-------+--------+----------+------+------------+---------+---------+--------+
> |  7369 | smith  | clark    | 7902 | 1980-12-17 |  800.00 |    NULL |     20 |
> |  7499 | allen  | salesman | 7698 | 1981-02-20 | 1600.00 |  300.00 |     30 |
> |  7566 | jones  | managen  | 7839 | 1981-04-02 | 2975.00 |    NULL |     30 |
> |  7654 | martin | salesman | 7698 | 1981-09-28 | 1250.00 | 1400.00 |     30 |
> +-------+--------+----------+------+------------+---------+---------+--------+
> 4 rows in set (0.00 sec)
> 
> mysql> select * from emp limit 2,3;
> +-------+--------+----------+------+------------+---------+---------+--------+
> | empno | enname | job      | mgr  | hiredate   | sal     | comm    | deptno |
> +-------+--------+----------+------+------------+---------+---------+--------+
> |  7566 | jones  | managen  | 7839 | 1981-04-02 | 2975.00 |    NULL |     30 |
> |  7654 | martin | salesman | 7698 | 1981-09-28 | 1250.00 | 1400.00 |     30 |
> |  7698 | blake  | manager  | 7839 | 1981-05-01 | 2850.00 |    NULL |     30 |
> +-------+--------+----------+------+------------+---------+---------+--------+
> 3 rows in set (0.01 sec)
> ```
>
> 总结：
>
> ​	查询语句书写顺序：select----》from---》where---》group by-----》having-----》order by----->limit
>
> ​	查询语句的执行顺序：from----》where-----》group by----》having----》select-----》order by----》limit

### 五、数据的完整性

> 作用：保证用户输入的数据保存到数据库中是正确的
>
> 实质：创建表的时候给表中的字段添加约束

#### 1.实体完整性

> 实体：表中的一行或者一条记录代表一个实体
>
> 实体完整性的作用：标识每一行数据不重复
>
> 约束类型：
>
> ​	主键约束【primary key】
>
> ​	唯一约束【unique】
>
> ​	自动增长列【auto_increment】

##### 1.1主键约束【primary key】

> 特点：数据唯一，且不能为null
>
> 主关键字可以是表中的一个字段或者多个字段，它的值用来唯一标识表中的某一条记录
>
> 场景：在多个表的关联关系中
>
> 演示：
>
> ```mysql
> mysql> create table stu1(
>     -> id int primary key,
>     -> name varchar(50)
>     -> );
> Query OK, 0 rows affected (0.06 sec)
> 
> mysql> create table stu2(
>     -> id int,
>     -> name varchar(50),
>     -> primary key(id)
>     -> );
> Query OK, 0 rows affected (0.03 sec)
> 
> mysql> create table stu3(
>     -> id int,
>     -> name varchar(50)
>     -> );
> Query OK, 0 rows affected (0.03 sec)
> 
> mysql> alter table stu3 add constraint stu3_id primary key(id);
> Query OK, 0 rows affected (0.08 sec)
> Records: 0  Duplicates: 0  Warnings: 0
> ```

##### 1.2唯一约束

> 作用：在非主键列中不能输入重复的值
>
> 演示：
>
> ```mysql
> mysql> create table stu4(
>     -> id int primary key,
>     -> name varchar(50) unique
>     -> );
> Query OK, 0 rows affected (0.04 sec)
> 
> 
> #primary key和unique之间的区别
> a.二者都强调的是唯一性
> b.在同一个表中，只能出现一个primary key，可以出现多个unique
> c.primary key不允许为null，但是unique是允许的
> ```

##### 1.3自动增长列

> 给主键添加添加自动增长性，列只能是整数类型
>
> 场景：一般添加给主键
>
> 演示：
>
> ```mysql
> mysql> create table stu5(
>     -> id int primary key auto_increment,
>     -> name varchar(50) unique
>     -> );
> Query OK, 0 rows affected (0.04 sec)
> ```

#### 2.域完整性

> 作用：限制单元格数据的正确性，
>
> ​	    域代表当前单元格
>
> 约束类型：
>
> ​	数据类型
>
> ​	非空约束【not null】
>
> ​	默认值约束【default】	

##### 2.1数据类型

> 数字类型：int  float  doule decimal
>
> 日期类型：date
>
> 字符串类型：char   varchar

##### 2.2非空约束【not null】

> 演示：
>
> ```mysql
> mysql> create table stu6( id int primary key auto_increment, name varchar(50) unique not null);
> Query OK, 0 rows affected (0.03 sec)
> 
> #注意：name被约束为not null，插入数据的时候，name坚决不能为null，如果未null，数据库立马报错
> ```

##### 2.3默认值约束

> 演示：
>
> ```mysql
> mysql> create table stu7(
>     -> id int primary key auto_increment,
>     -> name varchar(50) unique not null,
>     -> address varchar(50) default "beijing"
>     -> );
> Query OK, 0 rows affected (0.06 sec)
> 
> mysql> insert into stu7 (id,name,address) values(1,'aaa','fff');
> Query OK, 1 row affected (0.02 sec)
> 
> mysql> insert into stu7 (id,name,address) values(2,'bbb',default);
> Query OK, 1 row affected (0.01 sec)
> 
> mysql> select * from stu7;
> +----+------+---------+
> | id | name | address |
> +----+------+---------+
> |  1 | aaa  | fff     |
> |  2 | bbb  | beijing |
> +----+------+---------+
> 2 rows in set (0.00 sec)
> ```

#### 3.引用完整性

> 添加外键约束：foreign key
>
> 注意：添加外键必须先有主键，主键和外键的类型必须保持一致
>
> 举例：学生表，成绩表
>
> 作用：将两个甚至多个毫无关联的表产生联系
>
> 演示：
>
> ```mysql
> #创建表
> #学生表
> mysql> create table student(
>     -> stuid varchar(10) primary key,
>     -> stuname varchar(50)
>     -> );
> Query OK, 0 rows affected (0.01 sec)
> 
> #成绩表
> mysql> create table score(
>     -> stuid varchar(10),
>     -> score int,
>     -> courseid int
>     -> );
> Query OK, 0 rows affected (0.00 sec)
> 
> #插入数据
> mysql> insert into student values('1001','zhangsan');
> mysql> insert into student values('1002','xiaoming');
> mysql> insert into student values('1003','jack');
> mysql> insert into student values('1004','tom');
> 
> mysql> insert into score values('1001',98,1);
> mysql> insert into score values('1002',95,1)；
> mysql> insert into score values('1003',67,2);
> mysql> insert into score values('1004',83,2);
> mysql> insert into score values('1004',70,1);
> 
> #查询
> mysql> select * from student;
> +-------+----------+
> | stuid | stuname  |
> +-------+----------+
> | 1001  | zhangsan |
> | 1002  | lisi     |
> | 1003  | jack     |
> | 1004  | tom      |
> +-------+----------+
> 4 rows in set (0.00 sec)
> 
> mysql> select * from score;
> +-------+-------+----------+
> | stuid | score | courseid |
> +-------+-------+----------+
> | 1001  |    98 |        1 |
> | 1002  |    80 |        2 |
> | 1003  |    70 |        1 |
> | 1004  |    60 |        2 |
> | 1002  |    75 |        3 |
> +-------+-------+----------+
> 5 rows in set (0.00 sec)
> 
> 
> #方式一
> mysql> create table score1( score int, courseid int,stuid varchar(10), constraint stu_sco_id foreign key(stuid) references student(stuid) );
> Query OK, 0 rows affected (0.05 sec)
> #注意：stu_sco_id是给约束起的名字，可以自定义
> 
> #方式二
> mysql> create table score2(
>     -> score int,
>     -> courseid int,
>     -> stuid varchar(10)
>     -> );
> Query OK, 0 rows affected (0.04 sec)
> 
> mysql> alter table score2 add constraint stu_sco_id foreign key(stuid) references student(stuid);
> 
> #注意：主键和外键的类型必须保持一致
> ```

### 六、多表查询

#### 1.表与表之间的关系

> 一对一
>
> ​	通过嵌套的方式
>
> 一对多【多对一】
>
> ​	添加外键
>
> 多对多
>
> ​	单独创建一张新的表

#### 2.合并结果集

> 作用：将两个select语句的查询结果合并到一起
>
> 两种方式：
>
> ​	union：去除重复记录【并集】
>
> ​	union all；获取所有的结果
>
> 演示：
>
> ```mysql
> #创建表
> mysql> create table A(
>     -> name varchar(10),
>     -> score int
>     -> );
> Query OK, 0 rows affected (0.02 sec)
> mysql> create table B( name varchar(10), score int );
> Query OK, 0 rows affected (0.02 sec)
> 
> #批量插入数据
> mysql> insert into A values('a',10),('b',20),('c',30);
> Query OK, 3 rows affected (0.02 sec)
> Records: 3  Duplicates: 0  Warnings: 0
> mysql> insert into B values('a',10),('d',40),('c',30);
> Query OK, 3 rows affected (0.00 sec)
> Records: 3  Duplicates: 0  Warnings: 0
> 
> #查询结果
> mysql> select * from A;
> +------+-------+
> | name | score |
> +------+-------+
> | a    |    10 |
> | b    |    20 |
> | c    |    30 |
> +------+-------+
> 3 rows in set (0.00 sec)
> mysql> select * from B;
> +------+-------+
> | name | score |
> +------+-------+
> | a    |    10 |
> | d    |    40 |
> | c    |    30 |
> +------+-------+
> 3 rows in set (0.00 sec)
> 
> #合并结果集
> mysql> select * from A
>     -> union
>     -> select * from B;
> +------+-------+
> | name | score |
> +------+-------+
> | a    |    10 |
> | b    |    20 |
> | c    |    30 |
> | d    |    40 |
> +------+-------+
> 4 rows in set (0.00 sec)
> 
> mysql> select * from A
>     -> union all
>     -> select * from B;
> +------+-------+
> | name | score |
> +------+-------+
> | a    |    10 |
> | b    |    20 |
> | c    |    30 |
> | a    |    10 |
> | d    |    40 |
> | c    |    30 |
> +------+-------+
> 6 rows in set (0.00 sec)
> ```
>
> 注意：被合并的两个结果，列数、列类型必须相同
>
> 如果遇到列数不相同的情况，如下的解决办法：
>
> ```mysql
> mysql> insert into C values('a',10,29),('e',20,45),('c',30,10);
> Query OK, 3 rows affected (0.02 sec)
> Records: 3  Duplicates: 0  Warnings: 0
> 
> mysql> select * from A
>     -> union 
>     -> select name,score from C;
> +------+-------+
> | name | score |
> +------+-------+
> | a    |    10 |
> | b    |    20 |
> | c    |    30 |
> | e    |    20 |
> +------+-------+
> 4 rows in set (0.00 sec)
> ```

#### 3.连接查询

> 作用：求出多个表的乘积，例如t1和t2，如果采用了连接查询，得到的结果是t1*t2
>
> 演示：
>
> ```mysql
> mysql> select * from student,score;
> +-------+----------+-------+-------+----------+
> | stuid | stuname  | stuid | score | courseid |
> +-------+----------+-------+-------+----------+
> | 1001  | zhangsan | 1001  |    98 |        1 |
> | 1002  | lisi     | 1001  |    98 |        1 |
> | 1003  | jack     | 1001  |    98 |        1 |
> | 1004  | tom      | 1001  |    98 |        1 |
> | 1001  | zhangsan | 1002  |    80 |        2 |
> | 1002  | lisi     | 1002  |    80 |        2 |
> | 1003  | jack     | 1002  |    80 |        2 |
> | 1004  | tom      | 1002  |    80 |        2 |
> | 1001  | zhangsan | 1003  |    70 |        1 |
> | 1002  | lisi     | 1003  |    70 |        1 |
> | 1003  | jack     | 1003  |    70 |        1 |
> | 1004  | tom      | 1003  |    70 |        1 |
> | 1001  | zhangsan | 1004  |    60 |        2 |
> | 1002  | lisi     | 1004  |    60 |        2 |
> | 1003  | jack     | 1004  |    60 |        2 |
> | 1004  | tom      | 1004  |    60 |        2 |
> | 1001  | zhangsan | 1002  |    75 |        3 |
> | 1002  | lisi     | 1002  |    75 |        3 |
> | 1003  | jack     | 1002  |    75 |        3 |
> | 1004  | tom      | 1002  |    75 |        3 |
> +-------+----------+-------+-------+----------+
> 20 rows in set (0.01 sec)
> 
> #问题：进行连接查询，会产生笛卡尔积
> #笛卡尔积：两个集合相乘的结果
> #解释：假设集合A={a,b},集合B={0,1,2},则笛卡尔积的结果{(a,0),(a,1),(a,2),(b,0),(b,1),(b,2)}
> 
> #解决办法：在实际应用中，需要去除重复记录，则需要通过条件进行过滤
> mysql> select  s.stuid,s.stuname,c.score,c.courseid from student s,score c where s.stuid=c.stuid;
> +-------+----------+-------+----------+
> | stuid | stuname  | score | courseid |
> +-------+----------+-------+----------+
> | 1001  | zhangsan |    98 |        1 |
> | 1002  | lisi     |    80 |        2 |
> | 1003  | jack     |    70 |        1 |
> | 1004  | tom      |    60 |        2 |
> | 1002  | lisi     |    75 |        3 |
> +-------+----------+-------+----------+
> 5 rows in set (0.00 sec)
> ```

##### 3.1内连接-inner join on

> 内连接的特点：查询结果必须满足条件
>
> 演示：
>
> ```mysql
> #内连接
> mysql> select s.stuid,s.stuname,c.score,c.courseid  from student s join score c on s.stuid=c.stuid;
> +-------+----------+-------+----------+
> | stuid | stuname  | score | courseid |
> +-------+----------+-------+----------+
> | 1001  | zhangsan |    98 |        1 |
> | 1002  | lisi     |    80 |        2 |
> | 1003  | jack     |    70 |        1 |
> | 1004  | tom      |    60 |        2 |
> | 1002  | lisi     |    75 |        3 |
> +-------+----------+-------+----------+
> 5 rows in set (0.00 sec)
> 
> #等价写法
> mysql> select  s.stuid,s.stuname,c.score,c.courseid from student s,score c where s.stuid=c.stuid;
> +-------+----------+-------+----------+
> | stuid | stuname  | score | courseid |
> +-------+----------+-------+----------+
> | 1001  | zhangsan |    98 |        1 |
> | 1002  | lisi     |    80 |        2 |
> | 1003  | jack     |    70 |        1 |
> | 1004  | tom      |    60 |        2 |
> | 1002  | lisi     |    75 |        3 |
> +-------+----------+-------+----------+
> 5 rows in set (0.00 sec)
> 
> #练习：查询成绩大于70的学生记录
> #方式一
> mysql> select  s.stuid,s.stuname,c.score,c.courseid from student s,score c where s.stuid=c.stuid and c.score>70;
> +-------+----------+-------+----------+
> | stuid | stuname  | score | courseid |
> +-------+----------+-------+----------+
> | 1001  | zhangsan |    98 |        1 |
> | 1002  | lisi     |    80 |        2 |
> | 1002  | lisi     |    75 |        3 |
> +-------+----------+-------+----------+
> 3 rows in set (0.00 sec)
> 
> #方式二
> #也是内连接，只不过相当于是方言，join on相当于是普通话
> mysql> select  s.stuid,s.stuname,c.score,c.courseid from student s,score c where s.stuid=c.stuid and score>70;
> +-------+----------+-------+----------+
> | stuid | stuname  | score | courseid |
> +-------+----------+-------+----------+
> | 1001  | zhangsan |    98 |        1 |
> | 1002  | lisi     |    80 |        2 |
> | 1002  | lisi     |    75 |        3 |
> +-------+----------+-------+----------+
> 3 rows in set (0.00 sec)
> 
> #方式三
> mysql> select s.stuid,s.stuname,c.score,c.courseid  from student s join score c on s.stuid=c.stuid where score>70;
> +-------+----------+-------+----------+
> | stuid | stuname  | score | courseid |
> +-------+----------+-------+----------+
> | 1001  | zhangsan |    98 |        1 |
> | 1002  | lisi     |    80 |        2 |
> | 1002  | lisi     |    75 |        3 |
> +-------+----------+-------+----------+
> 3 rows in set (0.00 sec)
> ```

##### 3.2外连接-outer join on

> 特点：以其中一个表作为参照连接另外一个表
>
> 分类：
>
> ​	左外连接：left join on
>
> ​	右外连接：right join on
>
> ​	全外连接：full join【MySQL不支持】
>
> 演示：
>
> ```mysql
> #左外连接
> mysql> select s.stuid,s.stuname,c.score,c.courseid  from student s left join score c on s.stuid=c.stuid;
> +-------+----------+-------+----------+
> | stuid | stuname  | score | courseid |
> +-------+----------+-------+----------+
> | 1001  | zhangsan |    98 |        1 |
> | 1002  | lisi     |    80 |        2 |
> | 1003  | jack     |    70 |        1 |
> | 1004  | tom      |    60 |        2 |
> | 1002  | lisi     |    75 |        3 |
> +-------+----------+-------+----------+
> 5 rows in set (0.01 sec)
> 
> #内连接
> mysql> select s.stuid,s.stuname,c.score,c.courseid  from student s join score c on s.stuid=c.stuid;
> +-------+----------+-------+----------+
> | stuid | stuname  | score | courseid |
> +-------+----------+-------+----------+
> | 1001  | zhangsan |    98 |        1 |
> | 1002  | lisi     |    80 |        2 |
> | 1003  | jack     |    70 |        1 |
> | 1004  | tom      |    60 |        2 |
> | 1002  | lisi     |    75 |        3 |
> +-------+----------+-------+----------+
> 5 rows in set (0.00 sec)
> 
> #右外连接
> #参照为c
> mysql> select s.stuid,s.stuname,c.score,c.courseid  from student s right join score c on s.stuid=c.stuid;
> +-------+----------+-------+----------+
> | stuid | stuname  | score | courseid |
> +-------+----------+-------+----------+
> | 1001  | zhangsan |    98 |        1 |
> | 1002  | lisi     |    80 |        2 |
> | 1002  | lisi     |    75 |        3 |
> | 1003  | jack     |    70 |        1 |
> | 1004  | tom      |    60 |        2 |
> +-------+----------+-------+----------+
> 5 rows in set (0.01 sec)
> ```

##### 3.3自然连接-natural join

> 演示：
>
> ```mysql
> mysql> select * from student natural join score;
> +-------+----------+-------+----------+
> | stuid | stuname  | score | courseid |
> +-------+----------+-------+----------+
> | 1001  | zhangsan |    98 |        1 |
> | 1002  | lisi     |    80 |        2 |
> | 1003  | jack     |    70 |        1 |
> | 1004  | tom      |    60 |        2 |
> | 1002  | lisi     |    75 |        3 |
> +-------+----------+-------+----------+
> 5 rows in set (0.00 sec)
> 
> mysql> select student.stuid,student.stuname,score.score from student natural join score;
> +-------+----------+-------+
> | stuid | stuname  | score |
> +-------+----------+-------+
> | 1001  | zhangsan |    98 |
> | 1002  | lisi     |    80 |
> | 1003  | jack     |    70 |
> | 1004  | tom      |    60 |
> | 1002  | lisi     |    75 |
> +-------+----------+-------+
> 5 rows in set (0.00 sec)
> ```
>
> 总结：
>
> ​	连接查询会产生一些无用笛卡尔积，通常需要使用朱外键之间的关系去除重复记录，而自然连接无需给给出主外键之间的关系，会自动找到这个等式

#### 4.子查询

> 在一个select语句中包含另外一个完整的select语句【select语句的嵌套】
>
> 注意：
>
> ​	a.子查询出现的位置：
>
> ​		from后
>
> ​		where子句的后面，作为条件的一部分被查询
>
> ​	b。当子查询出现在where后面作为条件时，可以使用关键字：any、all
>
> ​	c.子查询结果集的形式
>
> ​		单行单列
>
> ​		单行多列
>
> ​		多行多列
>
> ​		多行单列
>
> 演示：
>
> ```mysql
> #1.查询和scott在同一个部门的员工
> #思路：先查询scott所在的部门，然后根据部门查找所有的信息
> mysql> select deptno from emp where enname='scott';
> +--------+
> | deptno |
> +--------+
> |     20 |
> +--------+
> 1 row in set (0.00 sec)
> 
> mysql> select * from emp where deptno=(select deptno from emp where enname='scott');
> +-------+--------+---------+------+------------+---------+------+--------+
> | empno | enname | job     | mgr  | hiredate   | sal     | comm | deptno |
> +-------+--------+---------+------+------------+---------+------+--------+
> |  7369 | smith  | clark   | 7902 | 1980-12-17 |  800.00 | NULL |     20 |
> |  7788 | scott  | analyst | 7566 | 1987-02-20 | 3000.00 | NULL |     20 |
> +-------+--------+---------+------+------------+---------+------+--------+
> 2 rows in set (0.00 sec)
> 
> 
> #2.查询工资高于joens的员工信息
> #思路：先查询jones的工资，然后根据jones查询其他的员工信息
> mysql> select * from emp where sal>(select sal from emp where enname='jones');
> +-------+--------+-----------+------+------------+---------+------+--------+
> | empno | enname | job       | mgr  | hiredate   | sal     | comm | deptno |
> +-------+--------+-----------+------+------------+---------+------+--------+
> |  7788 | scott  | analyst   | 7566 | 1987-02-20 | 3000.00 | NULL |     20 |
> |  7839 | king   | president | NULL | 1987-02-20 | 5000.00 | NULL |     10 |
> +-------+--------+-----------+------+------------+---------+------+--------+
> 2 rows in set (0.00 sec)
> 
> 
> #3.查询工资高于30号部门所有人的员工信息
> #思路：先查询30号部门中的最高工资，根据最高工资查询其他的员工信息
> mysql> select * from emp where deptno=30;
> +-------+--------+----------+------+------------+---------+---------+--------+
> | empno | enname | job      | mgr  | hiredate   | sal     | comm    | deptno |
> +-------+--------+----------+------+------------+---------+---------+--------+
> |  7499 | allen  | salesman | 7698 | 1981-02-20 | 1600.00 |  300.00 |     30 |
> |  7566 | jones  | managen  | 7839 | 1981-04-02 | 2975.00 |    NULL |     30 |
> |  7654 | martin | salesman | 7698 | 1981-09-28 | 1250.00 | 1400.00 |     30 |
> |  7698 | blake  | manager  | 7839 | 1981-05-01 | 2850.00 |    NULL |     30 |
> +-------+--------+----------+------+------------+---------+---------+--------+
> 4 rows in set (0.00 sec)
> 
> mysql> select max(sal) from emp where deptno=30;
> +----------+
> | max(sal) |
> +----------+
> |  2975.00 |
> +----------+
> 1 row in set (0.01 sec)
> 
> mysql> select * from emp where sal>(select max(sal) from emp where deptno=30);
> +-------+--------+-----------+------+------------+---------+------+--------+
> | empno | enname | job       | mgr  | hiredate   | sal     | comm | deptno |
> +-------+--------+-----------+------+------------+---------+------+--------+
> |  7788 | scott  | analyst   | 7566 | 1987-02-20 | 3000.00 | NULL |     20 |
> |  7839 | king   | president | NULL | 1987-02-20 | 5000.00 | NULL |     10 |
> +-------+--------+-----------+------+------------+---------+------+--------+
> 2 rows in set (0.00 sec)
> 
> #4.查询工作类型和工资与martin完全相同的员工信息
> #思路：先查询martin的工作类型和工资，然后再查询其他的员工信息
> mysql> select * from emp where (job,sal) in(select job,sal from emp where enname='martin');
> +-------+--------+----------+------+------------+---------+---------+--------+
> | empno | enname | job      | mgr  | hiredate   | sal     | comm    | deptno |
> +-------+--------+----------+------+------------+---------+---------+--------+
> |  7654 | martin | salesman | 7698 | 1981-09-28 | 1250.00 | 1400.00 |     30 |
> +-------+--------+----------+------+------------+---------+---------+--------+
> 1 row in set (0.00 sec)
> 
> #5.查询有2个以上下属的员工信息
> ysql> select mgr,count(mgr) from emp group by mgr having count(mgr)>2;
> +------+------------+
> | mgr  | count(mgr) |
> +------+------------+
> | 7839 |          3 |
> +------+------------+
> 1 row in set (0.00 sec)
> ```

#### 5.自连接

> 自己连接自己
>
> 演示：
>
> ```mysql
> #1.查询7654的员工姓名，经理编号和经理姓名
> mysql> select * from emp where  empno=(select mgr from emp where empno=7654);
> +-------+--------+---------+------+------------+---------+------+--------+
> | empno | enname | job     | mgr  | hiredate   | sal     | comm | deptno |
> +-------+--------+---------+------+------------+---------+------+--------+
> |  7698 | blake  | manager | 7839 | 1981-05-01 | 2850.00 | NULL |     30 |
> +-------+--------+---------+------+------------+---------+------+--------+
> 1 row in set (0.00 sec)
> 
> #2.求各个部门中薪水最高的员工信息
> mysql> select * from emp where sal in(select max(sal) from emp group by deptno);
> +-------+--------+-----------+------+------------+---------+------+--------+
> | empno | enname | job       | mgr  | hiredate   | sal     | comm | deptno |
> +-------+--------+-----------+------+------------+---------+------+--------+
> |  7566 | jones  | managen   | 7839 | 1981-04-02 | 2975.00 | NULL |     30 |
> |  7788 | scott  | analyst   | 7566 | 1987-02-20 | 3000.00 | NULL |     20 |
> |  7839 | king   | president | NULL | 1987-02-20 | 5000.00 | NULL |     10 |
> +-------+--------+-----------+------+------------+---------+------+--------+
> 3 rows in set (0.00 sec)
> ```

### 七、数据库的备份和恢复

#### 1.备份

> 生成SQL脚本，导出数据
>
> 命令：mysqldump -u root -p  数据库名>生成sql脚本的路径
>
> 注意：可以不需要登录数据库
>
> 演示：
>
> ```mysql
> rock@rockrong:~$ mysqldump -u root -p mydb1>/home/rock/Desktop/mydb1.sql
> Enter password: 
> ```

#### 2.恢复

> 执行sql脚本，恢复数据
>
> 前提：必须先创建数据库【空的】
>
> 注意：需要先登录数据库，然后进入指定的数据库，执行sql脚本
>
> 演示：
>
> ```mysql
> rock@rockrong:~$ mysql -u root -p
> Enter password: 
> Welcome to the MySQL monitor.  Commands end with ; or \g.
> Your MySQL connection id is 7
> Server version: 5.7.21-0ubuntu0.16.04.1 (Ubuntu)
> 
> Copyright (c) 2000, 2018, Oracle and/or its affiliates. All rights reserved.
> 
> Oracle is a registered trademark of Oracle Corporation and/or its
> affiliates. Other names may be trademarks of their respective
> owners.
> 
> Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
> 
> mysql> create database test;
> Query OK, 1 row affected (0.00 sec)
> 
> mysql> show tables;
> ERROR 1046 (3D000): No database selected
> mysql> use test;
> Database changed
> mysql> show tables;
> Empty set (0.00 sec)
> 
> mysql> source /home/rock/Desktop/mydb1.sql;
> Query OK, 0 rows affected (0.00 sec)
> ```

