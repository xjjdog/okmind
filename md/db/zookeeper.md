# Zookeeper

## CAP

- 一致性（C）
- 可用性（A）
- 分区容忍性（P）


## 作用

- 配置中心
- 命名服务
- 分布式锁
- 负载均衡
- 集群管理
- 分布式队列
- 分布式通知/协调
- 集群Master选举


## 重要概念

### 会话

### Znode

- PERSISTENT 持久化节点
- EPHEMERAL 临时节点
- EPHEMERAL_SEQUENTIAL 临时自动编号节点

### Watcher事件监听器

### ACL

### Leader

### Follower

## 特点

- 顺序一致性
- 原子性
- 单一系统映像
- 可靠性

## 主要配置

- myid 判断自己是哪个server
- initLimit 判断客户端下线的心跳时间 
- syncLimit leader和follower的应答时间


## [Curator](https://mp.weixin.qq.com/s/4WEJH5kALVtXKF6BtvaUhg)

### 事件监听

- Node Cache
- Path Cache
- Tree Cache

### 选举

- Leader Latch
- Leader Election

### 分布式锁

- 可重入锁Shared Reentrant Lock
- 不可重入锁Shared Lock
- 可重入读写锁Shared Reentrant Read Write Lock
- 信号量Shared Semaphore
- 多锁对象Multi Shared Lock

### 栅栏barrier

### 计数器Counters

- SharedCount
- DistributedAtomicLong


## 作者
### xjjdog
#### ![](/qrcode_for_gh_183eb256f8af_258.jpg)
