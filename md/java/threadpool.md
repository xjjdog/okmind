# 线程池

## 要点

- 会用线程池
- 知道线程池的主要参数
- 了解常用阻塞队列

## 解决问题

- 为减少频繁创建和销毁线程导致的系统开销
- 通过线程池来使得线程可以复用
- 暂存等待执行的任务

## 阻塞队列


### 常见队列

- 有界队列：ArrayBlockingQueue Note: 一个用数组实现的有界阻塞队列，按照先入先出(FIFO)的原则对元素进行排序。 不保证线程公平访问队列，使用较少
- 优先队列：PriorityBlockingQueue Note: 支持优先级的无界阻塞队列
- 无界队列：LinkedBlockingQueue Note: 一个用链表实现的有界阻塞队列，无界
- 同步移交：SynchronousQueue Note: 不储存元素，常用于生产者，消费者模型，吞吐量较高，使用较多

## 主要参数

### 核心参数

- corePoolSize 
- maximumPoolSize
- keepAliveTime 保活时间
- unit 单位
- workQueue 阻塞队列
- threadFactory 线程工厂，一般用来起名

### 拒绝策略

- AbortPolicy（默认）  中断策略，直接抛出异常
- CallerRunsPolicy 调用者运行策略，让调用者所在线程来运行策略
- DiscardOldestPolicy 舍弃最旧任务策略
- DiscardPolicy 舍弃策略，不处理
- 自定义策略

## 大小建议

### 计算密集型

- CPU数量+1


### I/O密集型

- 2*CPU数量（常规）
- 具体根据并发数调整

## 快捷创建方式

### FixedThreadPool
- 问题：使用LinkedBlockingQueue，无界

### SingleThreadExecutor
### CachedThreadExecutor
- 问题：线程无界
- 使用了SynchronousQueue

## 创建流程

- 1.当前线程数 小于 核心线程数(corePoolSize)
- 2.当前线程数 大于等于 核心线程数(corePoolSize) 且缓存队列未填满
- 3.当前线程数 大于等于 核心线程数(corePoolSize) 且缓存队列已填满  且线程数 小于 最大线程数(maximumPoolSize)
- 4.线程数 大于 最大线程数(maximumPoolSize)，触发拒绝策略

## 作者
### xjjdog
#### ![](/qrcode_for_gh_183eb256f8af_258.jpg)
