---
description: 此章节主要为Java 虚拟机原理相关
---

# Java 虚拟机

### TL;DR

啥是Java？

### 清单

#### [Q]ClassLoader.loadClass()与Class.forName()区别?
1. A1: Class.forName加载类是将类进了初始化，而ClassLoader的loadClass并没有对类进行初始化，只是把类加载到了虚拟机中
2. A2: [Class.forName和ClassLoader区别](https://mp.weixin.qq.com/s/g5DLNzLSMAmdIIo4dwcpdA)

#### [Q] Java，栈内存堆内存理解？栈如何转为堆
1. A1 [【JVM】对象并不一定都是在堆上分配内存的（JIT、逃逸分析）](https://blog.csdn.net/l18848956739/article/details/98853958)

#### [Q] java中的四种引用的区别以及使用场景
1. A1: [Java 四种引用介绍及使用场景](https://blog.csdn.net/u014532217/article/details/79184412)
2. A2: [Java中的强引用，软引用，弱引用，虚引用有什么用？](https://www.zhihu.com/question/37401125)
#### [Q] 强引用置为null，会不会被回收？
1. A1: [Java 中将对象引用置 null 的作用？](https://segmentfault.com/q/1010000000668646)
2. A2: [java 里对象使用后设置为NULL会减少内存占用吗？](https://www.zhihu.com/question/21356272)

#### [Q] 内存回收机制 什么样的会被GC回收
1. A1: [Java gc(垃圾回收机制)小结，以及Android优化建议](https://juejin.im/post/5bd01d235188255e3d25f5b5)
2. A2: [如何回答Android面试中java垃圾回收机制](https://juejin.im/post/5b17a5475188257d6225a7a2)
3. A3: [Android 垃圾回收机制](https://www.jianshu.com/p/99070b239827)

#### [Q] Java虚拟机的特性 谈谈对jvm的理解
1. A1: [关于Jvm知识看这一篇就够了](https://zhuanlan.zhihu.com/p/34426768)

#### [Q] JVM内存区域，开线程影响哪块内存 JVM内存模型，内存区域
1. A1: [可能是把Java内存区域讲的最清楚的一篇文章](https://juejin.im/post/5b7d69e4e51d4538ca5730cb)
2. A2: [JVM内存区域与多线程](https://www.jianshu.com/p/ece1bb5fa88b)
3. A3: [浅谈JVM虚拟机内存区域](https://www.yimipuzi.com/1036.html)

#### [Q] 虚拟机原理，如何自己设计一个虚拟机(内存管理，类加载，双亲委派)
1. A1: [如何实现一个简单的虚拟机？](https://www.zhihu.com/question/33084689)
2. A2: [从虚拟机架构到编译器实现](https://zhuanlan.zhihu.com/p/72356928)

#### [Q] 谈谈你对双亲委派模型理解 
1. A1: [浅谈双亲委派模型](https://www.jianshu.com/p/353c26c744df)

#### [Q] 类加载机制 谈谈对ClassLoader(类加载器)的理解
1. A1: [Android虚拟机框架：类加载机制](https://juejin.im/post/5a686596f265da3e2d339bb4)
2. A2: [经典回归：自定义 ClassLoader 和双亲委派机制](https://juejin.im/entry/58afce1a570c3500695d09b5)
3. A3: [JVM 类加载机制及双亲委派模型](https://juejin.im/post/5b3cc84ee51d4519873f08da)
4. A4: [深入理解Android中的ClassLoader](https://juejin.im/post/5a28e7e86fb9a045117105c3)

#### [Q] 谈谈对动态加载（OSGI）的理解
1. A1: [安卓平台中的动态加载技术分析](https://juejin.im/post/5a533c8df265da3e236651f3)

#### [Q] 内存对象的循环引用及避免
1. A1: [Android内存泄漏场景及解决方法](https://www.jianshu.com/p/f35ca324c285)
2. A2: [垃圾回收器如何处理循环引用](https://droidyue.com/blog/2015/06/05/how-garbage-collector-handles-circular-references/)

#### [Q] 内存回收机制、GC回收策略、GC原理时机以及GC对象
1. A1: [系统剖析Android中的内存泄漏](https://droidyue.com/blog/2016/11/23/memory-leaks-in-android/)
2. A2: [怎么在面试时回答Java垃圾回收机制（GC）相关问题？](https://www.zhihu.com/question/35164211)
3. A3: [Android 操作系统的内存回收机制](https://www.ibm.com/developerworks/cn/opensource/os-cn-android-mmry-rcycl/index.html)
4. A4: [2019-05-07：谈一谈JAVA垃圾回收机制](https://github.com/Moosphan/Android-Daily-Interview/issues/46)
5. A5: [Java gc(垃圾回收机制)小结，以及Android优化建议](https://www.jianshu.com/p/214e42fc0d37)
6. A6: [Android GC原理探究](https://zhuanlan.zhihu.com/p/24835977)
7. A7: [老大难的GC原理及调优，这下全说清楚了](https://juejin.im/post/5b6b986c6fb9a04fd1603f4a)

#### [Q] 垃圾回收机制与调用System.gc()区别
1. A1: [Why is it bad practice to call System.gc()?](https://stackoverflow.com/questions/2414105/why-is-it-bad-practice-to-call-system-gc)

#### [Q] 逻辑地址与物理地址，为什么使用逻辑地址？
1. A1: [逻辑地址、线性地址和物理地址](https://vosamo.github.io/2016/01/VA2PA/)
2. A2: [操作系统 内存地址（逻辑地址、线性地址、物理地址）概念](https://blog.51cto.com/laoxu/1166661)

#### [Q] 用户态和核心态
1. A1: [怎样去理解Linux用户态和内核态？](https://zhuanlan.zhihu.com/p/69554144)
#### [Q] Linux系统地址空间
1. A1: [Linux的进程地址空间（一）](https://zhuanlan.zhihu.com/p/66794639)

#### [Q] GC算法(各种算法的优缺点以及应用场景)
1. [JVM常见的几种GC算法](https://russxia.com/2019/07/25/JVM%E5%B8%B8%E8%A7%81%E7%9A%84%E5%87%A0%E7%A7%8DGC%E7%AE%97%E6%B3%95/)
