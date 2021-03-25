# Java并发

## [线程池](http://mind.xjjdog.cn/mind/java-threadpool)

## JMM

### 工作内存 主内存

### volatile

- 保持可见性
- 禁止指令重排
- 保证32机器64位操作原子性

### happends before语义

- 单一线程原则 Note: 一个线程内前面的操作先行发生于后面的操作
- 线程锁定规则 Note: 一个unlock操作先行发生于后面同一个锁的lock操作
- volatile规则 Note: 对一个volatile变量的写操作先行发生于后面的读操作
- 线程启动guise Note: start()方法的调用先行发生于后面的每一个动作
- 线程加入规则 Note: Thread对象的结束先行发生于join方法返回
- 线程中断规则 Note: interrupt()方法的调用先行发生于被中断线程的代码检测到事件发生
- 对象终结规则 Note: 一个对象的初始化，先行发生于它的finalize方法 (此关键字已废弃)
- 传递规则 Note: A先行与B、B先行与C，则A先行与C

  
## 线程要素

### 线程状态

- New
- Runable
- Waiting
- Timed Waiting
- Blocked
- Terminated

### 创建方法

- Runable
- Thread
- 线程池 （Runable、Callable）

### 同步方式

- synchronized
- wait/notify
- ReentrantLock
- Collections.synchronizedXx
- CAS

## 常用锁和工具

### AQS 核心

### ReetrantLock可重入锁

- 公平锁
- 非公平锁
- tryLock()
- lock()
- lockInterruptibly()
- Condition
  - await
  - signal
  - signalAll
  - awaitUniterruptibly

### ReadWriteLock读写锁

### Semaphore信号量

### CountDownLatch

- 赛马问题
- 倒计时

### CyclicBarrier

- 循环栅栏

## 常用并发容器

- ConcurrentHashMap
- CopyOnWriteArrayList 写时复制
- ArrayBlockingQueue
- LinkedBlockingQueue
- SynchronousQueue
- ConcurrentSkipListMap 跳表，有序
- DelayQueue 延时队列


## 锁优化措施

- CAS自旋锁
  - ABA问题
- 锁消除
- 锁粗化
- 锁升级
  - 轻量级锁
  - 偏向锁
  - 重量级锁



## 作者
### xjjdog
#### ![](/qrcode_for_gh_183eb256f8af_258.jpg)
