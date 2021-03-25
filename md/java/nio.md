# NIO（主要关注网络NIO）

## 要点

- 了解5种IO模型
- 了解3个核心概念
- 会用SocketChannel等
- 了解Epoll
- 了解Netty

## 《Unix网络编程》IO模型

- 阻塞IO模型
- 非阻塞IO模型
- 多路复用IO模型
- 信号驱动IO模型
- 异步IO模型
- 1.Java NIO属于多路复用

## 特点

### BIO

- 阻塞. 等待
- 每个连接一个线程

### NIO特点

- 缓冲区
- 非阻塞
- 多路复用

## 核心概念

- 通道 (Channel)
- 缓冲区 (Buffer)
- 选择器 (Selector)

## Epoll

### 演进
- poll
- select
- epoll

### 模式

- LT 水平触发
- ET 边缘触发
- Netty是高效ET

## 1.Channel

### 举例

- FileChannel
- DatagramChannel
- SocketChannel
- ServerSocketChannel

### 使用方式

- channel.configureBlocking(false)
- accept() 
- 处理SocketChannel

## 2.缓冲区

### 举例

- MappedByteBuffer
- HeapByteBuffer
- DirectByteBuffer
- ByteBuffer等

### 主要标志位

#### capacity
- 缓冲区数组的总长度
#### position
- 下一个要操作的数据元素的位置
#### limit
- 缓冲区数组中不可操作的下一个元素的位置
#### mark
- 记录当前 position 的前一个位置


### 主要方法

#### allocate 
- 分配
#### channel.read 
- 读取数据到buf
#### flip 
- 反转缓冲区
#### get 
- 读取数据
#### clear 
- 清空数据
#### compact 
- 未读数据拷贝到起始处
#### mark
- 标记特定position
#### rewind 
- 重复读取


## 3.Selector

### 事件

- OP_ACCEPT
- OP_WRITE
- OP_CONNECT
- OP_ACCEPT

### select()方法

- 可设置超时时间
- 阻塞等待
- 就绪后可通过selectKeys()获取集合

### selectKeys()方法

- 获取就绪的 SelectionKey 的集合
- 读取完毕，务必删除remove()，否则发生死循环


## 作者
### xjjdog
#### ![](/qrcode_for_gh_183eb256f8af_258.jpg)
