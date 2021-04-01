# MySQL InnoDB

## what's this

- 一个存储引擎
- B+ Tree为主

## MySQL主要存储引擎

- InnoDB
- MyISAM
- NDB
- Memory
- Archive

## InnoDB和MyISAM

### InnoDB

- OLTP
- 支持事务
- 支持行锁、外键、非锁定读
- 支持标准隔离级别
- next-key策略避免幻读
- 存储方式是聚集索引(clustered)
- MVCC

### MyISAM

- OLAP
- 不支持事务
- 表锁
- MYD存放数据文件，MYI存放索引文件

## 事务四个特性

- 原子性（atomicity)
- 一致性（consistency)
- 隔离性（isolation）
- 持久性（durability）

## 事务隔离级别

- Read uncommitted(读未提交)
- Read Committed(读已提交)
- Repeatable read(可重复读) 默认
- Serializable(串行化)

## 日志

- 错误日志
- 查询日志
- 慢查询日志
- Binlog
  - statement
  - row
  - mixed
  - 复制方式
    - 强同步
    - 半同步
    - 异步

## 核心存储方式

### 表

- 1.tablespace 表空间
- 2.segment 段
- 3.extent 区
- 4.page/block 页，默认16k

### 行

- compact
- 行溢出
- compressed 、 dynamic
- CHAR 、 VARCHAR

## 锁

### show status like 'innodb_row_lock%';

### 类型

- SLock 共享锁
- XLock 排他锁
- Intention Lock 意向锁

### 行锁

- 快照读（snapshot read）
- 当前读（current read）
- Record Lock Note:单行记录上锁
- Gap Lock Note:间隙锁
- Next-Key Lock 

## 约束

- 主键
- 联合约束
- 唯一约束
- 外键


## 数据类型

- 整数
- 定点数
- 浮点数
- 二进制
- 字符串
- 枚举
- set
- 时间日期

## 常见问题

- 脏读
- 不可重复读
- 幻读


## 作者
### xjjdog
#### ![](/qrcode_for_gh_183eb256f8af_258.jpg)
