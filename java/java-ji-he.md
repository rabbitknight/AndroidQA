---
description: 此章节主要为Java容器相关
---

# Java容器

### TL;DR

容器是啥应该都知道吧

### 清单

#### HashMap实现原理,扩容过程
1. A1: [Java HashMap工作原理及实现](https://yikun.github.io/2015/04/01/Java-HashMap%E5%B7%A5%E4%BD%9C%E5%8E%9F%E7%90%86%E5%8F%8A%E5%AE%9E%E7%8E%B0/)
2. A2:
    + 当put容量到达factor*cap进行扩容，扩大2倍
    + 已存储的不需要重新计算hash值，仅判断hash高位是否为1

#### HashMap、ConcurrentHashMap、HashTable区别
1. [HashMap、ConcurrentHashMap、HashTable的区别](https://www.jianshu.com/p/c00308c32de4)

#### [Q] 删除List中的Target
1. A1: 避免在for循环中使用remove直接删除
2. A2: [java 中删除list元素的四种方法(remove)](https://blog.csdn.net/qq_36412715/article/details/84071160)
