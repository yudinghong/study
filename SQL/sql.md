# sql study

## field types

### **数值类型**

|   **类型**   | 大小（bytes）                            |                        范围（有符号）                        |                        范围（无符号）                        | 用途           |
| :----------: | :--------------------------------------- | :----------------------------------------------------------: | :----------------------------------------------------------: | -------------- |
|   TINYINT    | 1                                        |                         (-128，127)                          |                           (0，255)                           | 小整数值       |
|   SMALLINT   | 2                                        |                       (-32768，32767)                        |                          (0，65535)                          | 大整数值       |
|  MEDIUMINT   | 3                                        |                     (-8388608，8388607)                      |                     (-8388608，8388607)                      | 大整数值       |
| INT或INTEGER | 4                                        |                  (-2147483648,2147483647 )                   |                       (0, 4294967295)                        | 大整数值       |
|    BIGINT    | 8                                        |   (-9,223,372,036,854,775,808，9 223 372 036 854 775 807)    |               (0，18 446 744 073 709 551 615)                | 极大整数值     |
|    FLOAT     | 4  bytes                                 | (-3.402 823 466 E+38，-1.175 494 351 E-38)，0，(1.175 494 351 E-38，3.402 823 466 351 E+38) |         0，(1.175 494 351 E-38，3.402 823 466 E+38)          | 单精度浮点数值 |
|    DOUBLE    | 8                                        | (-1.797 693 134 862 315 7 E+308，-2.225 073 858 507 201 4 E-308)，0，(2.225 073 858 507 201 4 E-308，1.797 693 134 862 315 7 E+308) | 0，(2.225 073 858 507 201 4 E-308，1.797 693 134 862 315 7 E+308) | 双精度浮点数值 |
|   DECIMAL    | 对DECIMAL(M,D) ，如果M>D，为M+2否则为D+2 |                        依赖于M和D的值                        |                        依赖于M和D的值                        | 小数值         |



### **日期和时间类型**

| **类型** | **大小( bytes)** | **范围** | 格式 | 用途 |
| -------- | -------------------- | ---- | ---- | ---- |
| DATE | 3 | 1000-01-01/9999-12-31 | YYYY-MM-DD | 日期值 |
| TIME | 3 | '-838:59:59'/'838:59:59' | HH:MM:SS | 时间值或持续时间 |
| YEAR | 1 | 1901/2155 | YYYY | 年份值 |
| DATETIME | 8 | 1000-01-01 00:00:00/9999-12-31 23:59:59 | YYYY-MM-DD HH:MM:SS | 混合日期和时间值 |
| TIMESTAMP | 4 | 1970-01-01 00:00:00/2038 | YYYYMMDD HHMMSS | 混合日期和时间值，时间戳 |



### **字符串类型**

| **类型**   | **大小**（bytes） | 用途                            |
| ---------- | ----------------- | ------------------------------- |
| CHAR       | 0-255             | 定长字符串                      |
| VARCHAR    | 0-65535           | 变长字符串                      |
| TINYBLOB   | 0-255             | 不超过 255 个字符的二进制字符串 |
| TINYTEXT   | 0-255             | 短文本字符串                    |
| BLOB       | 0-65 535          | 二进制形式的长文本数据          |
| TEXT       | 0-65 535          | 长文本数据                      |
| MEDIUMBLOB | 0-16 777 215      | 二进制形式的中等长度文本数据    |
| MEDIUMTEXT | 0-16 777 215      | 中等长度文本数据                |
| LONGBLOB   | 0-4 294 967 295   | 二进制形式的极大文本数据        |
| LONGTEXT   | 0-4 294 967 295   | 极大文本数据                    |



## 创建数据表

```mysql
CREATE TABLE table_name (column_name column_type);
```

```mysql
CREATE TABLE IF NOT EXISTS `runoob_tbl`(
   `runoob_id` INT UNSIGNED AUTO_INCREMENT,
   `runoob_title` VARCHAR(100) NOT NULL,
   `runoob_author` VARCHAR(40) NOT NULL,
   `submission_date` DATE,
   PRIMARY KEY ( `runoob_id` )
)ENGINE=InnoDB DEFAULT CHARSET=utf8;
```



## 删除数据表

```mysql
DROP TABLE table_name ;
```



## 插入数据表

```mysql
INSERT INTO table_name  (field1, field2,...fieldN)  VALUES  (valueA1,valueA2,...valueAN),(valueB1,valueB2,...valueBN),(valueC1,valueC2,...valueCN)......;
```



## 增加字段

```mysql
ALTER TABLE <表名> ADD <新字段名><数据类型>[约束条件];
ALTER TABLE <表名> ADD <新字段名> <数据类型> [约束条件] FIRST;
ALTER TABLE <表名> ADD <新字段名> <数据类型> [约束条件] AFTER <已经存在的字段名>;
```



## 查看表结构

```mysql
DESCRIBE <表名>;
DESC <表名>;
SHOW CREATE TABLE <表名>;
```



## 约束条件
* 主键约束

  ```mysql
  <字段名> <数据类型> PRIMARY KEY [默认值]
  # 联合主键
  PRIMARY KEY [字段1，字段2，…,字段n]
  ALTER TABLE <数据表名> ADD PRIMARY KEY(<字段名>);
  ALTER TABLE <数据表名> DROP PRIMARY KEY;
  ```

  

* 外键约束

  ```mysql
  [CONSTRAINT <外键名>] FOREIGN KEY 字段名 [，字段名2，…]
  REFERENCES <主表名> 主键列1 [，主键列2，…]
ALTER TABLE <数据表名> ADD CONSTRAINT <外键名>
  FOREIGN KEY(<列名>) REFERENCES <主表名> (<列名>);
ALTER TABLE <表名> DROP FOREIGN KEY <外键约束名>;
  ```
  
  
  
* 唯一约束

  ```mysql
  <字段名> <数据类型> UNIQUE
  ALTER TABLE <数据表名> ADD CONSTRAINT <唯一约束名> UNIQUE(<列名>);
  ALTER TABLE <表名> DROP INDEX <唯一约束名>;
  ```

  

* 检查约束

  ```mysql
  CHECK <表达式>
  CREATE TABLE tb_emp7
  (
  id INT(11) PRIMARY KEY,
  name VARCHAR(25),
  deptId INT(11),
  salary FLOAT,
  CHECK(salary>0 AND salary<100),
  FOREIGN KEY(deptId) REFERENCES tb_dept1(id)
  );
  ALTER TABLE tb_emp7 ADD CONSTRAINT <检查约束名> CHECK(<检查约束>)
  ALTER TABLE <数据表名> DROP CONSTRAINT <检查约束名>;
  ```

  

* 非空约束

  ```mysql
  <字段名> <数据类型> NOT NULL;
  ALTER TABLE <数据表名>
  CHANGE COLUMN <字段名>
  <字段名> <数据类型> NOT NULL;
  ALTER TABLE <数据表名>
  CHANGE COLUMN <字段名> <字段名> <数据类型> NULL;
  ```

  

* 默认值约束

  ```mysql
  <字段名> <数据类型> DEFAULT <默认值>;
  ALTER TABLE <数据表名>
  CHANGE COLUMN <字段名> <数据类型> DEFAULT <默认值>;
  ALTER TABLE <数据表名>
  CHANGE COLUMN <字段名> <字段名> <数据类型> DEFAULT NULL;
  ```

(case when conditions then .... else .... end)