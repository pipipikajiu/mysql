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
