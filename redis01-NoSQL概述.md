# NOSql概述

## 为什么要用Nosql

>1、单机Mysql的年代：数据库访问量不大，单个数据库完全足够，静态网页，服务器压力小

![image-20201117204211254](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20201117204211254.png)

**那么网站达到瓶颈时会怎样？**

1、数据库数量太大

2、数据库索引，一个机器内存不够

3、读写混合，服务器受不了

>2、Memcache(缓存)+Mysql+垂直拆分（读写分离）

为了减轻数据库的压力，可以使用缓存。网站80%都在查

![image-20201117204820592](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20201117204820592.png)

> 3、分库分表+水平分离+Mysql集群

![image-20201117205410482](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20201117205410482.png)

> 4、技术爆炸，Mysql关系型数据库不够用了  

# 什么是NOSql

NoSQL=Not Only SQL

解耦!
1、方便扩展（数据之间没有关系，很好扩展!)
2、大数据量高性能 (Redis一秒写8万次，读取11万，NoSQL的缓存记录级，是一种细粒度的缓存，性能会比较高!)

3、数据类型是多样型的!(不需要事先设计数据库!随取随用!如果是数据量十分大的表，很多人就无法设计了! )

4、传统 RDBMS和NoSQL（安装数据库安装）

```
传统的RDBMS
-结构化组织- sQL
-数据和关系都存在单独的表中
-操作操作，数据定义语言
-严格的一致性
-基础的事务
```

```
Nosq7
-不仅仅是数据
-没有固定的查询语言
-键值对存储，列存储，文档存储，图形数据库〈社交关系)
-最终一致性，
- CAP定理和BASE（异地多活）
- 高性能，高可用
```

# Nosql四大分类

**KV键值对**

- 美团：Redis+Tair
- 阿里百度：Redis+memecache

**文档型数据库**（bson格式和json格式一样）

- MongoDB
  - 非分布式文件存储的数据库，c++编写，用于处理大量的文档
  - 介于关系型数据库和非关系型数据库的产品

**列存储数据库**

- HBase
- 分布式文件系统

**图关系数据库**

- 存放的不是图，而是关系，比如朋友社交网络
- Neo4j











