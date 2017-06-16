
# 更新源

用vim打开源列表文件。

    sudo vim /etc/apt/sources.list

# 将下面的源粘贴到源列表里。

```sql
deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
##测试版源
deb http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
# 源码
deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
##测试版源
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
# Canonical 合作伙伴和附加
deb http://archive.canonical.com/ubuntu/ xenial partner
deb http://extras.ubuntu.com/ubuntu/ xenial main
```

# Apache安装

    sudo apt-get update
    sudo apt-get install tasksel
sudo tasksel

# 连接到本机上的MYSQL

        键入命令mysql -u root -p，回车后提示你输密码.
    
# 创建数据库

        注意：创建数据库之前要先连接Mysql服务器
        命令：create database <数据库名>
        例1：建立一个名为xhkdb的数据库 mysql> create database stu;

# 显示数据库

        show databases （注意：最后有个s） mysql> show databases;
# 删除数据库

        drop database <数据库名> 例如：删除名为 xhkdb的数据库 mysql> drop database xhkdb;
# 使用数据库

        命令： use <数据库名>

## 创建数据表

命令：create table <表名> ( <字段名1> <类型1> [,..<字段名n> <类型n>]);

```sql
mysql> create table information(sno char(15) not null primary key,sname char(20),sage int default 20,schoolno char(15),foreign key (schoolno) references school(schoolno));
```

## 显示数据库中的表

在use数据库的情况下

        命令：show tables;
        
## 表结构

    desc 表名 //查看表格结构

## 删除表

    命令：drop table <表名>

## 表插入数据

    命令：insert into <表名> [( <字段名1>[,..<字段名n > ])] values ( 值1 )[, ( 值n )]
    insert into course(cno,cname) values('01','java');

## 查询表中的数据

    查询所有行 命令： select <字段1，字段2，...> from < 表名 > where < 表达式 > 
    select * frmo course where cno = '01';

## 修改表中数据

    update 表名 set 字段=新值,... where 条件 
update MyClass set name='Mary' where id=1;






