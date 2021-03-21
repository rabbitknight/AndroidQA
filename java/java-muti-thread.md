---
description: 此章节主要为Java多线程相关
---

# Java 多线程

### TL;DR

多线程方方面面

### 清单
#### [Q] 进程和线程的区别

#### [Q] sychronied修饰普通方法和静态方法的区别
1. A1: 普通方法和实例化对象Object相关，静态方法和类Class相关。
2. A2: [Synchronized关键字加在普通方法上和加在静态方法上有什么区别?_学习中啊哈哈的博客-CSDN博客](https://blog.csdn.net/weixin_43658899/article/details/107230699)

#### [Q] 什么是可见性Visibility?原子性、可见性、有序性
1. A1: 核心是多线程访问同一变量。
   + 可见性：当一个线程修改了共享变量的值，其他线程能够立即得知这个修改
   + 原子性：一个操作或者多个操作，要么全部执行并且执行的过程不会被任何因素打断，要么就都不执行。
   + 顺序性：程序执行的顺序按照代码的先后顺序执行。
2. A2: [并发编程三大特性——原子性、可见性、有序性 - Ye_yang - 博客园]（https://www.cnblogs.com/yeyang/p/13576636.html）

#### [Q] 锁分为哪几类?
1. A1：
   + 是否抢占。直接锁：悲观；不锁：乐观。
   + 抢失败，是否阻塞:。不阻塞：自旋&适应性自旋；
   + 怎么抢？不锁重试：无锁；自动抢：偏向锁；没抢到自旋等待：轻量级锁，没抢到阻塞等待：重量级锁
   + 排队抢？排:公平锁；插队：非公平锁
   + 抢到了，再抢。能再抢：可重入；不能再抢：非可重入锁
   + 共享？共享：共享锁；不共享：排他锁
2. A2: [不可不说的Java“锁”事-美团技术团队](https://tech.meituan.com/2018/11/15/java-lock.html)

#### [Q] AQS原理？AbstractQueuedSynchronizer
1. A1: [从ReentrantLock的实现看AQS的原理及应用-美团技术团队](https://tech.meituan.com/2019/12/05/aqs-theory-and-apply.html)

#### [Q] ReentrantLock介绍
1. A1: [彻底理解ReentrantLock](https://juejin.cn/post/6844903601542807559)

#### [Q] Synchronized与ReentrantLoack区别

#### [Q] volatile能否保证线程安全
1. A1: volatile变量是一种同步机制；volatile能够确保可见性
2. A2: 除了可见性还有原子性与顺序性。
3. [volatile是什么？volatile能保证线程安全性吗？如何正确使用volatile？](https://www.cnblogs.com/laipimei/p/11857786.html)

#### [Q]什么是守护线程？
1. A1：[java 用户线程和守护线程](https://www.cnblogs.com/myseries/p/12078413.html)
  
#### [Q]如何退出一个线程？
1. A1: [如何正确地停止一个线程？](https://www.cnblogs.com/greta/p/5624839.html)

#### [Q] CAS介绍。CAS无锁编程
1. A0: 这题确定不是 Compare And Swap吗。。[无锁机制----比较交换CAS Compare And Swap](https://blog.csdn.net/yanluandai1985/article/details/82686486)  
2. A1: 原链接。[这是阿里巴巴的面试题，我不是很了解，可以参考博客: CAS简介](https://blog.csdn.net/jly4758/article/details/46673835)

#### [Q] sleep/wait/yield的区别。wait线程如何唤醒他?
1. A1: sleep 让出CPU资源，不释放锁。wait让出cpu资源和锁。yield 回归可执行状态。
2. A2: [[译]Java中Wait、Sleep和Yield方法的区别ZacharyJia](https://www.jianshu.com/p/25e959037eed)

#### [Q] sleep可中断吗？
1. A1: 可以，因为需要catch InterruptedException。

#### [Q] 线程生命周期
1. A1: 新建、就绪、运行、阻塞、销毁。
2. A2: [JAVA面试题 线程的生命周期包括哪几个阶段？](https://www.cnblogs.com/marsitman/p/11228684.html)

#### [Q] 线程池有没有上限？
1. A1: [线程池有没有上限](https://blog.csdn.net/github_37130188/article/details/89504500)

#### [Q] 线程池基本原理，参数定义。
1. A1: [图解 | 你管这破玩意叫线程池？](https://blog.csdn.net/coderising/article/details/112690662)

| 参数            | 说明                                                                                                                            |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| corePoolSize    | 核心线程数量，线程池维护线程的最少数量                                                                                          |
| maximumPoolSize | 线程池维护线程的最大数量                                                                                                        |
| keepAliveTime   | 当线程池线程的数量超过corePoolSize的时候，多余的空闲线程存活的时间，如果超过了corePoolSize，在keepAliveTime的时间之后，销毁线程 |
| unit            | keepAliveTime的单位，TimeUnit中的几个静态属性：NANOSECONDS、MICROSECONDS、MILLISECONDS、SECONDS                                 |
| workQueue       | 工作队列，将被提交但尚未执行的任务缓存起来                                                                                      |
| threadFactory   | 线程工厂，用于创建线程，不指定为默认线程工厂DefaultThreadFactory                                                                |
| handler         | 线程池对拒绝任务的处理策略                                                                                                      |
| ---             | ---                                                                                                                             |

#### [Q] 如何确保三个线程顺序执行？
1. A1: [如何确保三个线程顺序执行？](https://blog.csdn.net/Evankaka/article/details/80800081)
    + join
    + CountDownLatch
    + CachedThreadPool
    + blockingQueue

#### [Q] Java Condition 是啥
1. A1: Conditio类，类似Object的wait/notify机制[java condition使用及分析
](https://blog.csdn.net/bohu83/article/details/51098106#:~:text=Condition%E6%98%AF%E5%9C%A8java%201.5,%E5%8D%8F%E4%BD%9C%E6%9B%B4%E5%8A%A0%E5%AE%89%E5%85%A8%E5%92%8C%E9%AB%98%E6%95%88%E3%80%82)

#### [Q] Java Semphore使用场景
1. A1: 限制并发总数,获取到信号量的才能执行。可用于限制最大并发数量
2. A2: acquire/release [Semaphore 使用详解](https://www.jianshu.com/p/38630b7dbe73)
