# JVM (HotSpot VM)

## 种类

- HotSpot VM
- JRockit VM
- IBM JVM

## 垃圾回收器

- ZGC Java11可用
- G1 推荐
- CMS 不推荐
- Parallel Collector , 8默认

### 回收种类

- Minor GC
- Major GC
- Full GC, 比如 Metaspace 扩容引起年轻代和老年代的回收

## 主要参数

### 容量相关

- -Xmx 堆最大值
- -Xms 初始大小
- -Xmn 年轻代大小
- -XX:MaxMetaspaceSize 元空间大小，默认无上限
- -XX:MaxDirectMemorySize 直接内存上限
- -XX:ReservedCodeCacheSize JIT编译后代码存放区

### 内存调优

- -XX:+AlwaysPreTouch 启动前预分配
- -XX:SurvivorRatio 默认为8，伊甸区和幸存区比例
- -XX:MaxTenuringThreshold 对象提升阈值

### G1优化

- -XX:MaxGCPauseMillis
- -XX:G1HeapRegionSize 2的次幂
- -XX:InitiatingHeapOccupancyPercent
- -XX:ConcGCThreads

### 诊断工具

- jps
- jstat
- jmap
- jmc
- arthas
- gceasy.io

## 内存布局

### 虚拟机栈

#### 栈帧

- 局部变量表
- 操作数栈
- 动态连接
- 返回地址

### 程序计数器

### 堆

- 年轻代
- 老年代
- TLAB

#### 何时进入老年代

- 对象提升
- 分配担保
- 大对象直接在老年代分配
- 动态对象年龄判定

### 元空间

## 类加载

### 加载过程

- 加载
- 验证
- 准备
- 解析
- 初始化

### 加载器

- Bootstrap ClassLoader
- Extention ClassLoader
- App ClassLoader

### 双亲委派

#### 打破案例

- tomcat
- SPI
- OSGi


## GC Roots

### 谁是Roots

- 活动线程相关的各种引用
- 类的静态变量的引用
- JNI 引用

### 引用级别

- 强引用
- 弱引用
- 软引用
- 虚引用


## 专业划分堆（xjjdog独家）


### JVM进程内存

#### 堆内存

#### 堆外内存

##### 元空间

- 方法区

##### CodeCache

- JIT编译
- JNI代码

##### 本地内存

- 网络内存
- 线程内存
- JNI内存
- 直接内存

#### 操作系统剩余内存

#### SWAP



## 作者
### xjjdog
#### ![](/qrcode_for_gh_183eb256f8af_258.jpg)
