# redis内部实现

## 内存指标

- info memory 查看内存使用情况
- used_memory 分配的内存
- used_memory_rss 操作系统级别显示内存
- mem_fragmentation_ratio 内存碎片率
  - 内存分配器jemalloc
  - 数据长度差异，删除和更新造成
  - 重启可恢复

## redisObject

- 对象类型
- 内部编码
- LRU计时时钟
- 引用计数器
- 数据指针

## 数据结构

### 字符串 string

- SDS
- \O结尾
- O(1)获取len

####  存储结构

- int 整数
- raw 大于32byte
- embstr 小于32byte


### list列表 

- 双端
- 无环

#### 存储结构

- ziplist 元素个数小于512，元素小于64byte
- linkedlist

### 压缩列表

- 列表键、hash键底层实现
- ziplist 

### hash字典

- 链地址解决冲突
- 两个Hash，另一个做rehash用
- 渐进式rehash

#### 存储结构

- ziplist 元素个数小于512，元素小于64byte
- hashtable

### zset跳表

#### 存储结构

- ziplist 元素个数小于128，元素小于64byte
- skiplist


## cluster

### 节点

- CLUSTER MEET ip port
  - 1.客户端向结点 A 发送该消息
  - 2.收到命令的A将与结点B进行握手(发送 MEET 消息)
  - 3.结点B收到后，返回A一条 PONG 消息
  - 4.结点A收到后，A 向B 发送 PING 消息，此时握手完成
  - 5.A通过Gossip广播此消息

### 槽指派

- slot 16384个
- CLUSTER ADDSLOTS 


### 从节点设置

- CLUSTER REPLICATE node_id

### 故障处理

- 检测，广播ping消息
- 半数节点报告PFAIL，会将节点标记为FAIL
- 从机会选中一台成为主， 执行SLAVEOF no one
- 槽重新指派
- 广播消息进行通知

### 命令寻址

- 连接集群任意节点可执行命令
- 计算槽位置 slot = CRC16(key) & 16383
- 当前节点直接执行
- 其他节点返回MVOED错误
- redirect到正确节点，重新发起命令


### 复制

#### 过程

- 保存master信息
- 建立socket连接
- 发送ping命令
- 权限验证
- 同步数据
- 同步命令
  
#### PSYNC

- 心跳检测，1秒1次， REPLCONF ACK replication_offset
- 主从双方都会维持一个复制偏移量(offset)
- 主服务器的复制积压缓冲区，约1MB
- 根据offset确定部分同步还是全同步

## 哨兵

- 奇数个节点
- 可监视多套集群

### 原理

- 三个定时任务
  - 间隔10s，info指令更新拓扑
  - 间隔2s，判断主节点和自身
  - 间隔1s，对所有节点发送ping
- 哨兵主节点选举 max（quorum，num（sentinels）/2+1）

## 存储

### RDB

- SAVE 阻塞，无法处理请求
- BGSAVE 根据参数自动执行
- rdbLoad 启动加载，每加载1000处理新请求
- 结构
  - REDIS 固定
  - RDB-VERSION
  - SELECT-DB 数据库号码
  - KEY-VALUE-PAIRS
  - EOF
  - CHECK-SUM

### AOF

- 记录原始指令
- aof重写


## 作者
### xjjdog
#### ![](/qrcode_for_gh_183eb256f8af_258.jpg)
