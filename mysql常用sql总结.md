## 1 . 获取最大值/最小值
```javascript
greatest(字段1，字段2，字段3，..，字段n)  取最大值
least(字段1，字段2，字段3，...，字段n)   取最小值

示例：
SELECT GREATEST(2,3,4);   结果：4
SELECT LEAST(2,3,4);   结果：2

SELECT GREATEST(DATE('2016-05-02'), DATE('2015-05-02'), DATE('2017-05-02'));   结果：2017-05-02
SELECT LEAST(DATE('2016-05-02'), DATE('2015-05-02'), DATE('2017-05-02'));   结果：2015-05-02
```

## 2 . 查看sql 执行时间:
```javascript
    - 1 . 执行sql语句,看执行时间 : time php 文件名
    - 2 . show profiles(mysql 5.0.37之后添加的),在此之前要打开profiling : set profiling=on;
```
## 3 . 删除数据表内容:
```javascript
    truncate 表名.
```
## 4 . 按照长度排序:
```javascript
    select * from abc order by length(word) desc limit 2; 

    只取左边一个值:

    select left(name,1) from abc limit 2; 
```
##5 . 取不重复的值 :
```javascript
    distinct:
    select distinct left(name,1) from abc limit 2;
```

### 6 . MySQL数据库如何切换MyISAM和Innodb模式？
```javascript
    - 1. 登录PhpMyAdmin，可以看到当前默认引擎为：MyISAM，并且Innodb模式已被禁用，打开MySQL安装路径， 
    重命名 my.ini 和 my-innodb.ini ， 将my.ini 命名为 my-myisam.ini 将 my-innodb.ini 命名为 my.ini,然后重启apache
    - 2 . MySQL一般提供多种存储引擎，可以通过执行以下指令查看:
        首先进入MySQL命令行模式
        查看MySQL提供什么存储引擎:
        mysql> show engines;

        查看MySQL当前默认的存储引擎:
        mysql> show variables like '%storage_engine%';

        你要看wp_posts表用了什么引擎(在显示结果里参数engine后面的就表示该表当前用的存储引擎):
        mysql> show create table wp_posts;

        将wp_posts表修为InnoDB存储引擎(也可以此命令将InnoDB换为MyISAM)：
        mysql> ALTER TABLE wp_posts ENGINE=INNODB;
        
        如果要更改整个数据库表的存储引擎，一般要一个表一个表的修改，比较繁琐，可以采用先把数据库导出，得到SQL，把MyISAM全部替换为INNODB，再导入数据库的方式。

        转换完毕后重启mysql
        > service mysqld restart
```
