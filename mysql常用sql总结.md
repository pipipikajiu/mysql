## 1 . 
```javascript
greatest(字段1，字段2，字段3，..，字段n)  取最大值
least(字段1，字段2，字段3，...，字段n)   取最小值

示例：
SELECT GREATEST(2,3,4);   结果：4
SELECT LEAST(2,3,4);   结果：2

SELECT GREATEST(DATE('2016-05-02'), DATE('2015-05-02'), DATE('2017-05-02'));   结果：2017-05-02
SELECT LEAST(DATE('2016-05-02'), DATE('2015-05-02'), DATE('2017-05-02'));   结果：2015-05-02
```