# Java后端

## 一、基础知识

### 1. 数据结构

- 队列
- 栈
- 数组
- 字典
- 图
- 二叉树
- 平衡二叉树
- 红黑树
- B+树
- LSM数



### 2. 常用算法

- 排序算法
- 贪心算法
- 动态规划
- 回溯算法
- 剪枝算法
- 图算法
- 冒泡排序
- 快速排序
- 归并排序
- 插入排序
- 选择排序
- 堆排序



**书籍**

- 《算法导论》
- 《编程之美》
- 《数学之美》



###  3. 数据库基础



- InnoDB && MyISAM
- 字符集差别
- 索引优化
- 数据库范式
- 事务隔离级别
- 脏读 & 幻读
- MVCC
- 数据库锁



**书籍**



- 《MySQL技术内幕——InnoDB存储引擎》
- 《高性能MySQL》
- 《高可用MySQL》



### 4. 网络基础



- 网络协议TCP/UDP，三次握手四次握手
- HTTP/HTTPS区别
- 网络状态TIME_WAIT/CLOSE_WAIT
- 长连接 & 短连接优劣
- 滑动窗口
- 网络参数配置
- 通信模型
- 序列化工具
- 爬虫
- Netty

**书籍**

- 《HTTP权威指南》
- 《TCP/IP详解 卷一》



### 5. 操作系统Linux



- CPU、内存、网络、I/O
- 进程与线程
- 调度算法
- Shell变成
- 正则表达式
- 日常运维
- Python脚本
- 计算机组成与结构

**书籍**

- 《UNIX环境高级编程（第3版）》
- 《鸟哥的Linux私房菜》
- 《Linux内核设计与实现》
- 《Linux命令行大全》



### 6. Java基础 (JDK)

- 集合
- 文件操作
- 多线程
- NIO
- 反射
- Lambda
- JDBC
- JNDI
- RMI
- JMX
- JMS



**书籍**

- 《Effective Java 中文版》
- 《数据结构与算法分析：Java语言描述》



###  7. SSM && SSP

- IOC
- AOP
- SpringBoot starter
- MyBatis
- Tomcat
- 日志组件
- GoF设计模式23种
- UML
- DDD
- Restful



**书籍**



- 《Head First 设计模式》
- 《Spring揭秘》
- 《SpringBoot揭秘》
- 《MyBatis技术内幕》
- 《深入剖析Tomcat》



### 8. JVM

- 内存模型
- 垃圾回收器G1
- Class文件结构
- JVM主要参数调优
- 字节码的构成
- JVM锁的升级
- JMM概念
- 内存泄露排查的支持工具
- JVM并发
- JIT



**书籍**

- 《深入理解Java虚拟机》



### 9. 并发编程



- 线程安全的概念
- 线程池的配置参数
- AQS底层原理
- 锁的类型和用法
- 悲观锁和乐观锁的区别
- 公平锁和非公平锁的区别
- Concurrent工具包用法
- 无锁队列的概念和用法
- 多线程的ABA问题
- 多线程的伪共享问题
- 线程死锁原因和发生条件



**书籍**



- 《Java核心技术系列：Java多线程编程核心技术》
- 《Java性能权威指南》
- 《Java并发编程实战》



### 10. 性能优化 & 故障排查

- 内核参数调优
- JVM调优
- 网络参数调优
- 事务优化
- 数据库优化
- 池化处理
- 内存溢出排查
- 堆外内存排查
- 网络问题排查
- I/O问题排查
- 高负载问题排查
- 流量录制



**书籍**

- 《性能之巅：洞悉系统、企业与云计算》
- 《高性能Linux服务器构建实战》



## 二、Java进阶

### 1. 缓存Redis

- String
- Hash
- List
- Set
- Zset
- 其他
- 集群高可用方案
- 千万级排行榜方案
- 分布式锁方案
- 限流方案
- 缓存同步问题
- Redis使用规范



**书籍**

- 《Redis实战 》
- 《Redis开发与运维》
- 《Redis设计与实现》



### 2. 消息队列



- ActiveMQ
- RabbitMQ
- Kafka
- 消息可靠性的保证
- 事务消息保证
- 监控



### 3. 微服务

- SpringCloud
- Dubbo
- 注册中心
- 网关
- Feign rpc
- 熔断&限流使用场景
- 负载均衡
- 灰度测试
- 日志收集ELKB
- 监控报警
- 调用链
- 配置中心
- Job系统



**书籍**

- 《可伸缩服务架构：框架与中间件》
- 《Spring Cloud与Docker微服务架构实战》
- 《架构修炼之道》



### 4. 分布式系统



- CAP/BASE
- Raft协议
- Paxos协议
- Gossip协议
- Zookeeper和Zab协议
- 两阶段提交
- TCC
- 分布式要素：分片和副本
- Quorum/NWR
- 幂等处理
- 一致性Hash
- 分布式ID生成器 & 雪花算法



**书籍**

- 《NoSQL精粹》
- 《ZooKeeper：分布式过程协同技术详解》
- 《从Paxos到Zookeeper分布式一致性原理与实践》



## 三、系统支撑

### 1. 基本运维

- Ansiable
- 虚拟化
- 容器Docker
- 自动化脚本
- CI/CD
- 监控系统
- Devops
- 流程规范
- 成本管理
- Nginx
- K8s



**书籍**

- 《奔跑吧Ansible》
- 《Docker——容器与容器云》
- 《Kubernetes权威指南》
- 《Jenkins权威指南》
- 《深入理解Nginx》

### 2. 安全

- Spring Sercurity 
- SSO
- SQL注入
- XSS & CSRF
- DDoS
- 加密解密
- 证书体系
- 网络隔离及工具
- OAuth2



## 作者
### xjjdog
#### ![](/qrcode_for_gh_183eb256f8af_258.jpg)
