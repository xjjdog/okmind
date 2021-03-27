# [Redis面面观](https://mp.weixin.qq.com/s/5zi0ib0SZ3Qv3LTzF9dfKg)

## 能力

- 10w/s QPS
- 1w+ 长链接
- 持久化

## 数据结构

### 主要

- string
- hash
- list
- set
- zset

### 其他

- pub/sub
- bitmap
- geo
- stream
  - radix-tree
- hyperloglog

## 协议

- RESP
- RESP3
- 属于文本协议

## 持久化方式

- rdb 推荐
- aof
- rdb+aof

## 性能优化

- unlink
- pipeline
- 不用mset,hmset等
- 关掉aof

## 扩展方式

- lua
- redis-module

## 问题排查

- monitor
- keyspace-events
- slow log
- --bigkeys
- memory usage $key
- memory stats
- info
- redis-rdb-tools

## 淘汰策略

- volatile-lru （默认）
- volatile-ttl
- volatile-random
- volatile-lfu
- allkeys-lru
- allkeys-lfu
- allkeys-random
- no-enviction

## 集群模式

- 单机
- 单机多实例
- 主从1+n
- 主从1+n + 哨兵
- redis cluster（推荐）

### 大规模

- twemproxy
- codis
- cachecloud

## 使用场景

- 分布式锁 redlock
- 分布式限流
- session管理
- zset 排行榜
- bitmap 用户签到
- geo 地理位置
- stream 类kafka消息
- hyperloglog 每日访问ip数统计

## 缓存问题

- 缓存一致性 
  - 建议cache aside pattern
- 缓存击穿
- 缓存穿透
  - 缓存空对象
  - 布隆过滤器
- 缓存雪崩
  - 保证高可用
  - 限流降级
  - 提前演练

## 主要java客户端

- lettuce 
- jedis
- redisson

## 基本规范

- 使用连接池，不要频繁创建关闭客户端连接
- 消息大小限制 消息体在10kb以下，可以使用snappy、msgpack等压缩
- 避免大key和hot key
- 不使用O(n)指令
- 不使用不带范围的Zrange指令
- 不使用database（容易覆盖数据）
- 不使用高级数据结构（使用基本的5种）
- 不使用事务操作
- 禁止长时间monitor



## 作者
### xjjdog
#### ![](/qrcode_for_gh_183eb256f8af_258.jpg)


