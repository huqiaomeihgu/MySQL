
## 学生信息表设计

| 中文名称 | 英文名称 | 数据类型 | 默认值 | 备注 |
|---------|---------|---------|-------|-----|
| 学号 | sno | varchar(20) | 必填 | 主键 |
| 姓名 | sname | varchar(20) | 必填 | 无 |
| 年龄 | sage | int | 必填 | 无 |
| 系号 | schoolno | varchar(20) | 必填 | 外键级联删除修改 |
| 状态 | state | varchar(4) | 1 | 不空 |

## 课程表设计

| 中文名称 | 英文名称 | 数据类型 | 默认值 | 备注 |
|---------|---------|---------|-------|-----|
| 课程号 | cno | varchar(20) | 必填 | 主键 |
| 课程名 | cname | varchar(20) | 必填 | 无 |

## 院系表设计

| 中文名称 | 英文名称 | 数据类型 | 默认值 | 备注 |
|---------|---------|---------|-------|-----|
| 院系号 | schoolno | char(20) | 必填 | 主键 |
| 院系名 | schoolname | char(20) | 必填 | 无 |

## 成绩表设计

| 中文名称 | 英文名称 | 数据类型 | 默认值 | 备注 |
|---------|---------|---------|-------|-----|
| 学号 | sno | varchar(20) | 必填 | 主键外键级联删除修改 |
| 课程号 | cno | varchar(20) | 必填 | 主键外键级联删除修改 |
| 成绩 | grade | int | 必填 | 无 |


## 创建数据表

命令：create table <表名> ( <字段名1> <类型1> [,..<字段名n> <类型n>]);

```sql
mysql> create table information(sno char(15) not null primary key,sname char(20),sage int default 20,schoolno char(15),foreign key (schoolno) references school(schoolno));
```

## 表结构

    desc 表名 //查看表格结构

## 删除表

    命令：drop table <表名>

## 表插入数据

    命令：insert into <表名> [( <字段名1>[,..<字段名n > ])] values ( 值1 )[, ( 值n )]
    insert into course(cno,cname) values('01','java');

## 查询表中的数据

    查询所有行 命令： select <字段1，字段2，...> from < 表名 > where < 表达式 > 
    select * from course where cno = 'c1';

## 修改表中数据

    update 表名 set 字段=新值,... where 条件 
    update MyClass set name='Mary' where id=1;
    
## 增加字段

    alter table 表名 add字段 类型 其他;
    alter table information add sage int ;
    
## 涉及到多个表的连接的查询插入操作

1. 多个表之间的查询操作：

        select sname from information,score where information.sno = score.sno and grade = 80;
        两个表之间是通过sno属性进行连接的。
        
2. 多个表之间的插入操作

    schoolno属性在school中是作为主键存在的，在information表中是作为外键存在的，所以插入的schoolno必须在school表中存在。
    
         insert into information values('11','zhang',22,'01');
         
     执行下面的插入操作是无法执行成功的，因为04这个系号在school表中是不存在的。
     
        insert into information values('14','zhg',23,'04');
        
 
 
