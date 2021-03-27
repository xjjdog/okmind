# 事务处理

## ACID

- Atomicity（原子性）
- Consistency（一致性）
- Isolation（隔离性）
- Durability（持久性）

## 事务隔离级别

- READ_UNCOMMITED 读未提交
- READ_COMMITED 读提交
- REPEATABLE_READ 重复读
- SERIALIZABLE 序列化

## Spring事务传播

- PROPAGATION_REQUIRED 默认事务传播行为
- PROPAGATION_REQUIRES_NEW 新建事务
- PROPAGATION_NESTED 嵌套事务
- PROPAGATION_SUPPORTS 看调用者
- PROPAGATION_NOT_SUPPORTED 不开启事务
- PROPAGATION_MANDATORY 必须要有事务

## Spring事务原理

- threadlocal
- 不支持跨线程

## 分布式事务

- 2pc
- 3pc
- tcc
- 异步补偿
- 最大努力通知
- sagas事务模型

### 理论

#### CAP

- 一致性（Consistency）
- 可用性（Availability）
- 分区容错性（Partition tolerance）

#### BASE

- 基本可用
- 软状态
- 最终一致性

### 一致性级别

- 强一致性
- 弱一致性
- 最终一致性

### 难点在哪里? 

- 通信异常
- 网络分区
- 三态
- 节点故障


## 作者
### xjjdog
#### ![](/qrcode_for_gh_183eb256f8af_258.jpg)

