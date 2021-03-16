---
description: 此章节主要为Android特异的I/O
---

# Android I/O

### TL;DR

文件、输入输出、进程通信、序列化等

### 清单

#### [Q] 序列化的作用，以及Android两种序列化的区别,Serializable 和Parcelable 的区别
1. A1: [序列化Serializable和Parcelable的理解和区别](https://www.jianshu.com/p/a60b609ec7e7)

#### [Q] Android为什么引入Parcelable？
1. A1: [Serializable 都这么牛逼了，Parcelable，我还要你何用？](https://juejin.im/post/5a24fd8151882531ea651c37)

#### [Q] 有没有尝试简化Parcelable的使用？
1. A0: 很多回答都是讲插件..,实际AS上实现Parcelable的类名上，使用【ALT+ENTER】快捷键即可看到【Add Parcelable Implementation】选项，选择就可以完全自动创建好。。要啥插件？？？
1. A1: [kotlin使用Parcelize注解简化Parcelable的书写](https://juejin.im/entry/5a261a8c6fb9a0450167cf1b)
2. A2: 还是有一些插件选择，但没必要。
    + [Parceler](https://github.com/johncarl81/parceler)
    + [ParcelableGenerator](https://github.com/baoyongzhang/ParcelableGenerator)
    + [android-parcelable-intellij-plugin](https://github.com/mcharmas/android-parcelable-intellij-plugin)

#### [Q] Activity之间的通信方式
1. A1: 
    + startActivity,startActivityForResult
    + Broadcast或者LocalBroadcast
    + 其他任何进程内通信的方式。
2. A2: 
    + [Activity之间的通信方式](https://juejin.im/post/5a9509ef6fb9a06337575d4b)
    + [Activity之间的通信方式](https://www.jianshu.com/p/12438e23c6b8)

#### [Q] service和activity怎么进行数据交互？AndroidService与Activity之间通信的几种方式
1. A1: 同一个进程：任何进程内同步方式。
2. A2: 不同进程：AIDL、Messenger、Socket等任何IPC方式。

#### [Q] fragment之间传递数据的方式？
1. A1: 官方指南：[与其他 Fragment 通信](https://developer.android.google.cn/training/basics/fragments/communicating#java),一句话：接口回调。

#### [Q] 广播是否可以请求网络？
1. A1: onReceive回调在什么线程？[广播概览](https://developer.android.com/guide/components/broadcasts?hl=zh-cn)
2. A2: [Android主线程里不允许网络操作](https://blog.csdn.net/thl789/article/details/10628419)

#### [Q] 广播引起anr的时间限制是多少？
1. [理解Android ANR的触发原理](http://gityuan.com/2016/07/02/android-anr/)
2. [Android N 各种ANR的时间](https://blog.csdn.net/u013122625/article/details/74676666)

#### [Q] Android中数据存储方式 
1. A1: [Android五种数据存储方式- 简书](https://www.jianshu.com/p/536ca489a7f4)

#### [Q] HttpUrlConnection 和 okhttp关系
1. A1: [Android 网络(三) HttpURLConnection OkHttp](https://www.jianshu.com/p/2fa728c8b366)

#### [Q] AstncTask+HttpClient 与 AsyncHttpClient有什么区别？
1. A0: 没有任何关系
2. A1: [AsyncTask](https://developer.android.com/reference/android/os/AsyncTask)
3. A2: ~~[HttpClient]~~ 404 NOT FOUND
4. A3: [async-http-client](https://github.com/AsyncHttpClient/async-http-client)

#### [Q] SP是进程同步的吗?有什么方法做到同步？
1. [SP（SharedPreferences）是进程同步的吗?有什么方法做到同步？](https://blog.csdn.net/github_37130188/article/details/89483154)

#### [Q] SP线程同步
1. [SharedPreferences与线程安全](https://phantomvk.github.io/2019/03/25/Why_SharedPrefs_thread_safe/)

#### [Q] Android代码中实现WAP方式联网
1. A0: 不懂就问：什么场景会用到这个？
2. A1: [Android代码中实现WAP方式联网](https://blog.csdn.net/asce1885/article/details/7844159)

#### [Q] LruCache默认缓存大小
1. A0: 需要自己指定，并重写相应方法做计算，源码中并没有规定默认多少。

#### [Q] 服务器只提供数据接收接口，在多线程或多进程条件下，如何保证数据的有序到达？
1. A0: 似乎没有百度到啥内容，各位答手似乎歇菜了。强答：多线程情形下可以考虑多线程同步方法，参考[LeetCode. 1114 按序打印](https://leetcode-cn.com/problems/print-in-order/),多进程的条件。。。是啥条件?文件锁?信号量?多进程同步?

#### [Q] 从网络加载一个10M的图片，说下注意事项
1. A1: [Android 大图加载](https://www.jianshu.com/p/7c81d3742c38)
2. A2: [Android高效加载大图、多图解决方案，有效避免程序OOM](https://blog.csdn.net/guolin_blog/article/details/9316683)

#### [Q] sqlite升级，增加字段的语句
1. A1: [android sqlit数据库升级，添加字段](https://blog.csdn.net/mafei852213034/article/details/55096032)
2. A2: [Sqlite升级时向已有表中增加字段](https://blog.csdn.net/qq_26287435/article/details/82585597)

#### [Q] 数据库框架对比和源码分析
1. A1: [ORM数据库框架 SQLite 常用数据库框架比较 MD](https://www.cnblogs.com/baiqiantao/p/9492180.html)

#### [Q] 数据库的优化
1. A1: [android数据库优化](https://www.jianshu.com/p/3b4452fc1bbd)

#### [Q] 数据库数据迁移问题
1. A1: [Android 数据库综述（一） 数据库片的升级与数据的迁移操作](https://juejin.im/post/59e7e5856fb9a0451542fb19)

#### [Q] 现在下载速度很慢,试从网络协议的角度分析原因,并优化(提示：网络的5层都可以涉及)。

#### [Q] Https请求慢的解决办法（提示：DNS，携带数据，直接访问IP）
1. A1: [弱网优化在支付宝的深度实践 | mPaaS 线下沙龙 CodeDay#1 分享实录](https://juejin.im/post/5ca5c174f265da30cc7919d1)
2. A2: 百度弱网优化
    + [百度 App 网络深度优化系列（一）：DNS 优化](https://www.infoq.cn/article/3QZ0o9Nmv*O0LoEPVRkN)
    + [百度 App 网络深度优化系列（二）：连接优化](https://www.infoq.cn/article/CDaih849Ao4rS_pctQ2T)
    + [百度 App 网络深度优化系列（三）：弱网优化](https://www.infoq.cn/article/pQmLUECekW*DsymqbGvy)
3. A3: [Android 使用OkHttp支持HttpDNS](https://blog.csdn.net/sbsujjbcy/article/details/50532797)

#### [Q] 进程间通信的方式？
1. A1: [【朝花夕拾】Android性能篇之（七）Android跨进程通信篇](https://www.cnblogs.com/andy-songwei/p/10256379.html)
2. A2: [Android 多进程通信](https://juejin.im/post/5aa08cb3f265da23766ad734)


#### [Q] 简述IPC？
1. A1: [Android IPC机制（进程间通信）](https://www.jianshu.com/p/96062c549b2a)

#### [Q] 什么是AIDL？
1. A1: [Android 接口定义语言 (AIDL)](https://developer.android.com/guide/components/aidl?hl=zh-cn)
2. A2: [Android AIDL使用详解](https://www.jianshu.com/p/29999c1a93cd)

#### [Q] AIDL解决了什么问题？
1. A1: [Android AIDL 原理解析](https://github.com/cundong/blog/blob/master/Android%20AIDL%20%E5%8E%9F%E7%90%86%E8%A7%A3%E6%9E%90.md)
2. A2: [Android开发中在哪些场合下会需要使用AIDL?](https://www.zhihu.com/question/20146972)
#### [Q] AIDL如何使用？
1. A1: [Android 接口定义语言 (AIDL)](https://developer.android.com/guide/components/aidl?hl=zh-cn)

#### [Q] Android 上的 Inter-Process-Communication 跨进程通信是如何工作的？
1. A1: [Android进程间通信-AIDL实现原理](https://www.cnblogs.com/wangqiang9/p/9517260.html)
1. A2: [Android 中的多进程通信机制](https://henleylee.github.io/posts/2019/20c92935.html)

#### [Q] 多进程场景遇见过么？
1. A1: [巧用Android多进程，微信，微博等主流App都在用](https://cjw-blog.net/2017/02/26/AIDL/)

#### [Q] Android进程分类？
1. A1: [进程和应用生命周期](https://developer.android.com/guide/components/activities/process-lifecycle?hl=zh-cn)

#### [Q] 进程和 Application 的生命周期？
1. A1: [喜闻乐见之Android应用的生命周期](https://juejin.im/post/5af0fa5d6fb9a07aa34a3246)
2. A2: [Android：全面解析 Application类](https://juejin.im/entry/59c30e0ff265da06611f7024)

#### [Q] 进程调度
1. A1: [从Linux 进程调度到 Android 线程管理](https://zhuanlan.zhihu.com/p/34799829)

#### [Q] 谈谈对进程共享和线程安全的认识
1. A1: [谈谈对进程,线程,线程安全和线程状态的理解](https://blog.csdn.net/weixin_43666051/article/details/103206017)
2. A2: [浅谈 Android 开发中多进程共享数据](https://juejin.im/entry/56f344c7da2f60004ccb4dfd)

#### [Q] 谈谈对多进程开发的理解以及多进程应用场景
1. A1: [面试题：谈谈对进程的理解？谈谈你对线程的理解？2.进程死锁的原因？如何解决进程死锁？](https://blog.csdn.net/linux12121/article/details/51786241)

#### [Q] 在Android中两个进程之间传输大数据，可以使用什么方式实现?这些方式中哪种方式最高效?请说明原因。
1. A1: 推荐使用MemoryFile,高版本修改为SharedMemory。核心都是通过Binder传输序列化的文件描述符，一边发送一边接收。
