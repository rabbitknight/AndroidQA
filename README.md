# AndroidInterview
本仓库仅用于收集和整理面试问题

[TOC]

## TL;DR
1. 一共分为4大类，Java相关、Android相关、数据结构和算法、其他
2. 尽量不推荐直接告诉答案(除非很简单)，尽可能收集相关文档
3. 后期强烈考虑对文档进行评级。
4. 优先推荐官方文档。
5. 食用方式: 1. 搜搜浏览[Ctrl+F]; 2. 逐行浏览

## 暂行细则
1. 所有题目以4级标题<####>提供,类似[Q] XXXX
2. 所有题目回答以[A]标记作为开始，分为A1 A2 A3 ...
3. 如果要贴图，请将原图(附带水印)至于[</res/images/>](https://github.com/rabbitknight/AndroidInterview/tree/master/res/images)目录
4. 如果要PDF文档，请将文档，至于 [</res/pdfs/>](https://github.com/rabbitknight/AndroidInterview/tree/master/res/pdfs)
5. 等级标识 三级描述：

| 标识                                                  | 说明 |
| ----------------------------------------------------- | ---- |
| ![低](https://img.shields.io/badge/level-BASE-green)  | 低   |
| ![中](https://img.shields.io/badge/level-MIDDLE-blue) | 中   |
| ![高](https://img.shields.io/badge/level-HARD-red)    | 高   |

6. 特殊标识：

| 标识                                                          | 说明     |
| ------------------------------------------------------------- | -------- |
| ![推荐-官方](https://img.shields.io/badge/rating-官方-orange) | 官方文档 |
| ![推荐-XXXX](https://img.shields.io/badge/rating-XXX-orange)  | 等级推荐 |
| ![不推荐](https://img.shields.io/badge/rating-不推荐-RED)     | 不推荐   |


## 清单
### Java相关
<details>

#### [Q] java中==和equals和hashCode的区别
#### [Q] int、char、long各占多少字节数
#### [Q] int与integer的区别
#### [Q] 谈谈对java多态的理解
#### [Q] String、StringBuffer、StringBuilder区别
#### [Q] 什么是内部类？内部类的作用
#### [Q] 抽象类和接口区别
#### [Q] 抽象类的意义
#### [Q] 抽象类与接口的应用场景
#### [Q] 抽象类是否可以没有方法和属性？
#### [Q] 接口的意义
#### [Q] 泛型中extends和super的区别
#### [Q] 父类的静态方法能否被子类重写
#### [Q] 进程和线程的区别
#### [Q] final，finally，finalize的区别
#### [Q] 序列化的方式
#### [Q] Serializable 和Parcelable 的区别
#### [Q] 静态属性和静态方法是否可以被继承？是否可以被重写？以及原因？
#### [Q] 静态内部类的设计意图
#### [Q] 成员内部类、静态内部类、局部内部类和匿名内部类的理解，以及项目中的应用
#### [Q] 谈谈对kotlin的理解
#### [Q] 闭包和局部内部类的区别
#### [Q] string 转换成 integer的方式及原理
#### [Q] TCP的3次握手和四次挥手
#### [Q] TCP与UDP的区别
#### [Q] TCP与UDP的应用
#### [Q] HTTP协议
#### [Q] HTTP1.0与2.0的区别
#### [Q] HTTP报文结构
#### [Q] HTTP与HTTPS的区别以及如何实现安全性
#### [Q] 如何验证证书的合法性?
#### [Q] https中哪里用了对称加密，哪里用了非对称加密，对加密算法（如RSA）等是否有了解?
#### [Q] client如何确定自己发送的消息被server收到?
#### [Q] 谈谈你对WebSocket的理解
#### [Q] WebSocket与socket的区别
#### [Q] 泛型擦除是什么，会带来什么问题？
1. A1: [面试官问我：“泛型擦除是什么，会带来什么问题？”](https://mp.weixin.qq.com/s/i6ZXpjBfS-kSszF-dstZlw)

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
1. A1: 
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

####  ClassLoader.loadClass()与Class.forName()区别?
1. A1: Class.forName加载类是将类进了初始化，而ClassLoader的loadClass并没有对类进行初始化，只是把类加载到了虚拟机中
2. A2: [Class.forName和ClassLoader区别](https://mp.weixin.qq.com/s/g5DLNzLSMAmdIIo4dwcpdA)
</details>

### Android相关
<details>

#### [Q] 四大组件是什么
1. A1: Acitivity、Service、Broadcast、ContentProvider
2. A2: [「Android」四大组件，你真的都掌握了？ - 掘金](https://juejin.im/post/5db12d926fb9a0205e766cc2)

#### [Q] 四大组件的生命周期和简单用法
1. A1: 官网必看文档
    + Activity: [了解 Activity 生命周期](https://developer.android.com/guide/components/activities/activity-lifecycle?hl=zh-cn)
    + Service: [服务概览](https://developer.android.com/guide/components/services?hl=zh-cn​)
    + Boradcast: [广播概览](https://developer.android.com/guide/components/broadcasts)
    + ContentProvider: [内容提供程序基础知识](https://developer.android.com/guide/topics/providers/content-provider-basics)

#### [Q] Activity之间的通信方式
1. A1: 
    + startActivity,startActivityForResult
    + Broadcast或者LocalBroadcast
    + 其他任何进程内通信的方式。
2. A2: 
    + [Activity之间的通信方式](https://juejin.im/post/5a9509ef6fb9a06337575d4b)
    + [Activity之间的通信方式](https://www.jianshu.com/p/12438e23c6b8)

#### [Q] Activity各种情况下的生命周期
1. A1: [关于Activity各种情况下的生命周期](https://www.jianshu.com/p/e46d449467d5)
2. A2: [Activity 的生命周期](https://www.dazhuanlan.com/2019/11/15/5dce694806cad/)

#### [Q] Activity与Fragment之间生命周期比较
1. A1: [比较Activity与Fragment的生命周期](https://blog.csdn.net/k_bb_666/article/details/74995582)

#### [Q] Activity上有Dialog的时候按Home键时的生命周期
1. A1: 有 Dialog 和 无 Dialog 按 Home 键效果一样。
2. A2: 示例测试：[Activity上有Dialog的时候按Home键时的生命周期](https://blog.csdn.net/xiyoucode/article/details/79595815)

#### [Q] 两个Activity 之间跳转时必然会执行的是哪几个方法？
1. A1:　A->B
    + A 里面激活B 组件的时候, A会调用onPause()方法,然后B调用onCreate() ,onStart(),  ()。B覆盖了A的窗体, A会调用onStop()方法。
    + B是个透明的窗口,或者是对话框的样式, 就不会调用A的onStop()方法。
    + B已经存在于Activity栈中，B就不会调用onCreate()方法。
2. A2: [两个Activity之间跳转时必然会执行的是哪几个方法？](https://blog.csdn.net/m_xiaoer/article/details/72881082)

#### [Q] 前台切换到后台，然后再回到前台，Activity生命周期回调方法。弹出Dialog，生命值周期回调方法。
1. A1: [前台切换到后台，然后再回到前台，Activity生命周期回调方法](https://blog.csdn.net/yz_cfm/article/details/85476263)
2. A2: 此题目直接看[Activity各种情况下的生命周期]

#### [Q] Activity的四种启动模式对比
1. A1: 官方文档！[了解任务和返回堆栈](https://developer.android.com/guide/components/activities/tasks-and-back-stack)
2. A2: [说说 Activity 的四种启动模式](https://www.jianshu.com/p/b60d8097e519) 包含launchmode和IntentFlag


#### [Q] Activity状态保存与恢复
1. A1: [Android的状态保存和恢复](https://www.jianshu.com/p/90cf59f22f40)
#### [Q] fragment各种情况下的生命周期
1. A1: [Fragment 在各种情况下的生命周期](https://www.geek-share.com/detail/2718616379.html)

#### [Q] Activity和Fragment状态
1. A1: [保存/恢复 Activity和Fragment状态的最佳实践](https://segmentfault.com/a/1190000006691830)

#### [Q] Fragment状态保存startActivityForResult是哪个类的方法，在什么情况下使用？
1. A1: [彻底搞懂startActivityForResult在FragmentActivity和Fragment中的异同](https://blog.csdn.net/barryhappy/article/details/53229238)

#### [Q] 如何实现Fragment的滑动？
1. A1: [ViewPager+Fragment实现页面滑动效果](https://www.jianshu.com/p/87134516445c)
#### [Q] fragment之间传递数据的方式？
1. A1: 官方指南：[与其他 Fragment 通信](https://developer.android.google.cn/training/basics/fragments/communicating#java),一句话：接口回调。

#### [Q] Activity 怎么和Service 绑定？
1. A1:[谈一谈startService和bindService的区别，生命周期以及使用场景](https://github.com/Moosphan/Android-Daily-Interview/issues/53)
#### [Q] 怎么在Activity 中启动自己对应的Service？
1. A1: [Activity怎么和service绑定，怎么在activity中启动自己对应的service？](https://github.com/Sogrey/Android_QA/issues/92)

#### [Q] service和activity怎么进行数据交互？AndroidService与Activity之间通信的几种方式
1. A1: 同一个进程：任何进程内同步方式。
2. A2: 不同进程：AIDL、Messenger、Socket等任何IPC方式。
#### [Q] Service的开启方式
1. A1: [Android Service两种启动方式详解](https://www.jianshu.com/p/4c798c91a613)

#### [Q] 请描述一下Service 的生命周期
1. A1: [Android Service两种启动方式详解](https://www.jianshu.com/p/4c798c91a613)

#### [Q] 谈谈你对ContentProvider的理解
1. A1: [Android：关于ContentProvider的知识都在这里了！](https://www.jianshu.com/p/ea8bc4aaf057)

#### [Q] 说说ContentProvider、ContentResolver、ContentObserver 之间的关系
1. A1: [ContentProvider、ContentResolver、ContentObserver之间的关系](https://www.cnblogs.com/anni-qianqian/p/8391887.html)
#### [Q] 请描述一下广播BroadcastReceiver的理解
1. A1: ["BroadcastReceiver"-安卓面试必问技能点大总结"](https://blog.csdn.net/nzfxx/article/details/51835743)

#### [Q] 广播的分类广播使用的方式和场景
1. A1: [Android：BroadcastRecevicer广播类型汇总](https://blog.csdn.net/carson_ho/article/details/53160580)
#### [Q] 在manifest 和代码中如何注册和使用BroadcastReceiver?
1. A1: [Android：在AndroidManifest中注册BroadcastReceiver的权限问题](https://blog.csdn.net/books1958/article/details/39472385)
#### [Q] 本地广播和全局广播有什么差别？BroadcastReceiver，LocalBroadcastReceiver区别
1. A1: [本地广播和全局广播的差别](https://www.jianshu.com/p/bfbb6ebc1c04)

#### [Q] AlertDialog,popupWindow,Activity区别
1. A1: 不要人言亦言~ [关于坑爹的PopupWindow的“阻塞”争议问题：Android没有真正的“阻塞式”对话框](https://blog.csdn.net/zhengxiaoyao0716/article/details/48768407)
2. A2: 该篇文章才真正描述了实际区别: [从问题出发，解析Activity、Window、View三者关系](https://juejin.im/entry/59a3ab465188252445327481)

#### [Q] Activity-Window-View三者的差别
1. A1: [从问题出发，解析Activity、Window、View三者关系](https://juejin.im/entry/59a3ab465188252445327481)

#### [Q] Application 和 Activity 的 Context 对象的区别 ; ApplicationContext和ActivityContext的区别
1. A1: [Application context和Activity context的区别](https://www.jianshu.com/p/4f97baa0e8f7)
2. A2: [Context 都没弄明白，还怎么做 Android 开发？](https://zhuanlan.zhihu.com/p/24847247)

#### [Q] Android属性动画特性
1. A1: 官方:[属性动画概览](https://developer.android.com/guide/topics/graphics/prop-animation?hl=zh-cn)
2. A2: [HenCoder Android 自定义 View 1-7：属性动画 Property Animation（进阶篇）](https://hencoder.com/ui-1-7/)

#### [Q] LinearLayout、RelativeLayout、FrameLayout的特性及对比，并介绍使用场景。
1. A1: [Android UI之五种基本布局详解](https://blog.csdn.net/github_37130188/article/details/89113243)
2. A2: [帧布局（FrameLayout）](https://www.jianshu.com/p/a169cce78340)

#### [Q] 谈谈对接口与回调的理解回调的原理写一个回调demo
1. A1: [回调的原理 ？写一个回调demo](https://blog.csdn.net/qq_26358311/article/details/79607768)
#### [Q] 介绍下SurfaceView
1. A1: [Android中的SurfaceView详解](https://www.jianshu.com/p/b037249e6d31)

#### [Q] RecyclerView的使用
1. A1: [使用 RecyclerView 创建列表](https://developer.android.com/guide/topics/ui/layout/recyclerview?hl=zh-cn)
2. A2: [Android RecyclerView 使用完全解析 体验艺术般的控件](https://blog.csdn.net/lmj623565791/article/details/45059587)
3. A3: [图解 RecyclerView 的缓存机制](https://blog.csdn.net/weixin_43130724/article/details/90068112)
#### [Q] RecyclerView和ListView对别
1. A1: [RecyclerView 和 ListView 使用对比分析](https://www.jianshu.com/p/f592f3715ae2?utm_campaign=haruki&utm_content=note&utm_medium=reader_share&utm_source=weixin&from=singlemessage&isappinstalled=1)
#### [Q] RecyclerView原理
1. A1: [深入浅出 RecyclerView](https://www.kymjs.com/code/2016/07/10/01/)
2. A2: [RecyclerView缓存原理，有图有真相](https://juejin.im/post/5b79a0b851882542b13d204b)
3. A3: [Android RecyclerView 原理解析](https://www.okcode.net/article/27992)
#### [Q] RecyclerView优化
1. A1: [RecyclerView一些你可能需要知道的优化技术](https://www.jianshu.com/p/1d2213f303fc)
#### [Q] 列表卡顿问题怎么优化
1. A1: [Andriod性能优化之列表卡顿——以“简书”APP为例](https://www.jianshu.com/p/336362b23c30)
2. A2: [Android 中的卡顿丢帧原因概述 - 系统篇](https://zhuanlan.zhihu.com/p/82521327)
#### [Q] 序列化的作用，以及Android两种序列化的区别
1. A1: [序列化Serializable和Parcelable的理解和区别](https://www.jianshu.com/p/a60b609ec7e7)
#### [Q] 差值器和估值器
1. [Animation总结(差值器和估值器)](https://www.jianshu.com/p/f18517076b40)
#### [Q] Android中数据存储方式 
1. A1: [Android五种数据存储方式- 简书](https://www.jianshu.com/p/536ca489a7f4)

#### [Q] Android动画框架实现原理
1. A1: [Android三种动画实现](http://gityuan.com/2015/09/04/android-anaimator-1/)
2. A2: [源码解读Android属性动画](http://gityuan.com/2015/09/06/android-anaimator-4/)

#### [Q] Android各个版本API的区别
0. 关于Android版本更新 行为变更 很多同学可能都没有阅读过相关文档 就人云亦云。我在调研10关于后台Service变更时，发现还是官方文档讲的最清楚。所以这里只有官方文档。请结合代码调试来熟悉。
1. A1: [Kitkat](https://developer.android.com/about/versions/kitkat)
2. A2: [Lollipop](https://developer.android.com/about/versions/lollipop)
3. A3: [Marshmallow](https://developer.android.com/about/versions/marshmallow)
4. A4: [Nougat](https://developer.android.com/about/versions/nougat)
5. A5: [Oreo](https://developer.android.com/about/versions/oreo)
6. A6: [Pie](https://developer.android.com/about/versions/pie)
7. A7: [10/Q](https://developer.android.com/about/versions/10)
8. A8: [11/Preview](https://developer.android.com/preview)

#### [Q] Requestlayout，onlayout，onDraw，DrawChild区别与联系
1 A1: [requestLayout()与onLayout()；onDraw()与drawChild()的区别和联系](https://blog.csdn.net/weixin_41101173/article/details/79726311)

#### [Q] invalidate和postInvalidate的区别及使用
1. A1: [invalidate()和postInvalidate() 的区别及使用](https://www.jianshu.com/p/e147f381190c)

#### [Q] 如何优化自定义View
1. A1: [Custom Views and Performance](https://www.kancloud.cn/redzealot2008/android-performance-patterns/345950)
2. A2: [你最需要知道的View优化](https://zhuanlan.zhihu.com/p/28198804)
3. A3: [Android性能优化典范 - 第1季](http://hukai.me/android-performance-patterns/)
4. A4: [正确认识onMeasure方法！](https://mp.weixin.qq.com/s/7FE0a9UI5sB538pA6kxpQA)
#### [Q] 低版本SDK如何实现高版本api？
1. A1: [RequiresApi](https://developer.android.com/reference/android/support/annotation/RequiresApi)
2. A2: [Android 高版本API方法在低版本系统上的兼容性处理](https://www.jianshu.com/p/6ad6490c8375)

#### [Q] 描述一次网络请求的流程
1. A1: [NetWork——描述一次完整的网络请求过程](https://blog.csdn.net/SEU_Calvin/article/details/53304406)

#### [Q] HttpUrlConnection 和 okhttp关系
1. A1: [Android 网络(三) HttpURLConnection OkHttp](https://www.jianshu.com/p/2fa728c8b366)

#### [Q] Bitmap对象的理解
1. A1: [Android Bitmap理解](https://blog.csdn.net/wangcheng_/article/details/78253953)
2. A2: [彻底理解Bitmap的高效加载策略](https://www.jianshu.com/p/5f02db4a225d)
3. A3: [Android O Bitmap 内存分配](https://www.cnblogs.com/xiaji5572/p/7794083.html)

#### [Q] Bitmap对象占用内存计算
1. A1: [Android坑档案：你的Bitmap究竟占多大内存？](https://zhuanlan.zhihu.com/p/20732309)
2. A2: [Bitmap究竟占多大内存](https://xiongcen.github.io/2017/01/04/AndroidBitmapMemory/)

#### [Q] ActivityThread，AMS，WMS的工作原理
0. 关于Android底层实现，全系推荐[gityuan](http://gityuan.com/)的文章，其他杂七杂八的先省略了！
1. A1: [理解Application创建过程](http://gityuan.com/2017/04/02/android-application/)
2. A2: [ActivityManagerService启动过程](http://gityuan.com/2016/02/21/activity-manager-service/)

#### [Q] 自定义View如何考虑机型适配
1. A1: [自定义View尺寸进行适配](https://www.jianshu.com/p/4100ccacf385)
2. A2: [自定义View如何考虑机型适配](https://blog.csdn.net/github_37130188/article/details/89075837)

#### [Q] 自定义View的事件
1. A1: [@GcsSloop](https://www.gcssloop.com/)大佬的文章[安卓自定义View进阶-事件分发机制详解](https://www.gcssloop.com/customview/dispatch-touchevent-source)

#### [Q] AstncTask+HttpClient 与 AsyncHttpClient有什么区别？
1. A0: 没有任何关系
2. A1: [AsyncTask](https://developer.android.com/reference/android/os/AsyncTask)
3. A2: ~~[HttpClient]~~ 404 NOT FOUND
4. A3: [async-http-client](https://github.com/AsyncHttpClient/async-http-client)

#### [Q] LaunchMode应用场景
1. [深入讲解Android中Activity launchMode](https://droidyue.com/blog/2015/08/16/dive-into-android-activity-launchmode/)

#### [Q] AsyncTask 如何使用?
1. A1: [AsyncTask](https://developer.android.com/reference/android/os/AsyncTask)

#### [Q] SpareArray 和 ArrayMap
1. A1: [Android学习笔记之性能优化SparseArray](https://www.cnblogs.com/RGogoing/p/5095168.html)
2. A2: [深度解读ArrayMap优势与缺陷](http://gityuan.com/2019/01/13/arraymap/)

#### [Q] 请介绍下ContentProvider 是如何实现数据共享的？
1. A1: [[问答]请介绍下ContentProvider是如何实现数据共享的](https://github.com/android-cn/android-discuss/issues/24)

#### [Q] IntentService原理及作用是什么？
1. A1: [理解 IntentService 原理](https://juejin.im/post/5c75f3e851882540a702ea8f)

#### [Q] 说说Activity、Intent、Service 是什么关系
1. A0: 没啥关系。单独看Activity/Service即可。
2. A1: [Intent 和 Intent 过滤器](https://developer.android.com/guide/components/intents-filters)

#### [Q] SP是进程同步的吗?有什么方法做到同步？
1. [SP（SharedPreferences）是进程同步的吗?有什么方法做到同步？](https://blog.csdn.net/github_37130188/article/details/89483154)

#### [Q] SP线程同步
1. [SharedPreferences与线程安全](https://phantomvk.github.io/2019/03/25/Why_SharedPrefs_thread_safe/)

#### [Q] 谈谈多线程在Android中的使用
1. A1: Android特有
    + AsyncTask
    + Handler
    + IntentService
2. A2: 任何Java中多线程的方法。
3. A3: ![不推荐](https://img.shields.io/badge/rating-不推荐-RED) [Android多线程：理解和简单使用总结l](https://www.jianshu.com/p/56163a3beb4a)

#### [Q] 进程和 Application 的生命周期
1. A1: ![推荐-官方](https://img.shields.io/badge/rating-官方-orange)
[进程和应用生命周期](https://developer.android.com/guide/components/activities/process-lifecycle?hl=zh-cn)

#### [Q] 封装View的时候怎么知道view的大小
1. A1: [Android 浅谈View的测量measure](https://www.yimipuzi.com/1057.html)

#### [Q] AndroidManifest的作用与理解
1. A1: [AndroidManifest.xml详解](https://www.jianshu.com/p/3b5b89d4e154)

#### [Q] 内存泄漏优化
1. A1: [Android性能优化之内存优化](https://jsonchao.github.io/2019/08/18/Android%E6%80%A7%E8%83%BD%E4%BC%98%E5%8C%96%E4%B9%8B%E5%86%85%E5%AD%98%E4%BC%98%E5%8C%96/)

#### [Q] 如何在子线程操作UI
1. A1: [Android只在UI主线程修改UI，是个谎言吗？ 为什么这段代码能完美运行？](https://www.zhihu.com/question/24764972)
2. A2: [Android-在子线程中显示Toast和Dialog](https://blog.csdn.net/u012230055/article/details/54289280)
3. A3: [android 关于子线程更新 UI 的一些事](https://juejin.im/entry/582d5587a0bb9f0067a6f02a)

#### [Q] 为何Handler可以操作UI，Handler线程切换原理
1. A1: [Android消息分发及多线程切换之Handler、Message的细枝末节（二）](https://www.jianshu.com/p/a842b8d815d8)
2. A2: [通过学习Handler源码，手写子线程间的通信](https://mp.weixin.qq.com/s?__biz=MzU3NzQ0MzYxMg==&mid=2247483708&idx=1&sn=e81d8d4e2d920fa783e6ec686937bd38&chksm=fd05c34fca724a59471a26d9f037b6423684f2c2a5a6cc5ef8907712aa67c167fbbb95f92bf4&mpshare=1&scene=1&srcid=&sharer_sharetime=1585648474813&sharer_shareid=faa5430ddf8e3a72161f970023d7de03&key=c967bf038ee4b9073471d47fe0e3a2112403c9db6c3abde3ccab1da023b98e659ee50b048d7a1bdd2054ec6a2923e64c4030fef68e356d7892556383484cc7def9195b428f5bcd4cc94926373ee39229&ascene=1&uin=MTEyNTM1NjEzMg%3D%3D&devicetype=Windows+10&version=62080079&lang=zh_CN&exportkey=A7sKMq1ne1EDaEr9Dl%2BPU%2BE%3D&pass_ticket=0iku%2FkvhX9MVQv2%2BuLZfzJxteUkt0ZTaaOrk980uVza4MYxtH7%2F4MaLhB5Ke6loV)

#### [Q] OkHttp缓存机制
1. A1: [OKHttp全解析系列（五） --OKHttp的缓存机制](https://www.jianshu.com/p/fb81207af121)


#### [Q] 如何提升Activity开启速度
1. A1: [提升进入界面的速度](https://zmywly8866.github.io/2015/09/28/promote-enter-activity-speed.html)

#### [Q] Handler机制和底层实现 looper架构
1. A1: 推荐@Gityuan大佬的全系文章
    + [Android消息机制1-Handler(Java层)](http://gityuan.com/2015/12/26/handler-message-framework/)
    + [Android消息机制2-Handler(Native层)](http://gityuan.com/2015/12/27/handler-message-native/)

#### [Q] Handler、Thread和HandlerThread的差别
1. A1: [Handler、Thread、HandlerThread三者的区别](https://blog.csdn.net/weixin_41101173/article/details/79687313)

#### [Q] Handler发消息给子线程，looper怎么启动？
1. A1: 感觉这问题 问的 没头没脑
1. A2: [Android-Interview/bak/resources/sourcefile/深入知识点3中高级/消息队列/-203-handler发消息给子线程，looper怎么启动.md](https://github.com/android-exchange/Android-Interview/blob/master/bak/resources/sourcefile/%E6%B7%B1%E5%85%A5%E7%9F%A5%E8%AF%86%E7%82%B93%E4%B8%AD%E9%AB%98%E7%BA%A7/%E6%B6%88%E6%81%AF%E9%98%9F%E5%88%97/-203-handler%E5%8F%91%E6%B6%88%E6%81%AF%E7%BB%99%E5%AD%90%E7%BA%BF%E7%A8%8B%EF%BC%8Clooper%E6%80%8E%E4%B9%88%E5%90%AF%E5%8A%A8.md)

#### [Q] 关于Handler，在任何地方new Handler 都是什么线程下?
1. A0: 看一下Handler的构造方法即可获得答案。
2. A1: [android在线程中创建handler应注意什么](https://github.com/android-cn/android-discuss/issues/44)

#### [Q] ThreadLocal原理，实现及如何保证Local属性？
1. A1: 问题搜索N篇都是这老哥答案。[ThreadLocal原理，实现及如何保证Local属性](https://blog.csdn.net/github_37130188/article/details/89483246)

#### [Q] 请解释下在单线程模型中Message、Handler、Message Queue、Looper之间的关系
1. A1: 了解下Handler机制即可[Message、Handler、Message Queue、Looper之间的关系](https://www.jianshu.com/p/352877cd61c1)
#### [Q] 请描述一下View事件传递分发机制 Touch事件传递流程
1. A1: [Android事件分发机制](http://gityuan.com/2015/09/19/android-touch/)
2. A2: [Android事件分发机制——从基础深入源码解析](https://www.jianshu.com/p/e6ceb7f767d8)

#### [Q] 事件分发中的onTouch 和onTouchEvent 有什么区别，又该如何使用？
1. A1: [事件处理之onTouchEvent()和onTouch()方法精炼详解](https://blog.csdn.net/weixin_41101173/article/details/80460632)
2. A2: [android onTouch()与onTouchEvent()的区别](https://blog.csdn.net/guyuealian/article/details/51637033)
3. A3: [事件分发中的onTouch 和onTouchEvent 有什么区别?](https://qqabby.github.io/2019/01/21/事件分发中的onTouch-和onTouchEvent-有什么区别/)

#### [Q] View和ViewGroup分别有哪些事件分发相关的回调方法
1. A1: [View & ViewGroup 之 事件分发](https://blog.csdn.net/crazy1235/article/details/70767884)
2. A2: [View和ViewGroup分别有哪些事件分发相关的回调方法](https://blog.csdn.net/github_37130188/article/details/89112835)

#### [Q] View刷新机制
1. A1: [Android 屏幕刷新机制](https://www.jianshu.com/p/0d00cb85fdf3)
2. A2: [Android View刷新机制](https://blog.csdn.net/chenzhiqin20/article/details/8628952)
#### [Q] View绘制流程
1. A1: [深入理解Android之View的绘制流程](https://www.jianshu.com/p/060b5f68da79)

#### [Q] 自定义控件原理
1. A1: [【Android】自定义控件之View原理与使用](https://www.jianshu.com/p/a3014f8442b0)

#### [Q] 自定义View如何提供获取View属性的接口？
1. A1: [Android自定义View属性，使用或获取自定义View属性，获取View默认属性](https://blog.csdn.net/ShareUs/article/details/85879789)

#### [Q] Android代码中实现WAP方式联网
1. A0: 不懂就问：什么场景会用到这个？
2. A1: [Android代码中实现WAP方式联网](https://blog.csdn.net/asce1885/article/details/7844159)

#### [Q] AsyncTask机制
1. A0: [【Android】AsyncTask机制](https://www.cnblogs.com/milovetingting/p/10643742.html)

#### [Q] AsyncTask原理及不足
1. A1: [Android 多线程：AsyncTask的原理 及其源码分析](https://www.jianshu.com/p/37502bbbb25a)
2. A2: [AsyncTask的缺陷和问题](https://blog.csdn.net/goodlixueyong/article/details/45895997)

#### [Q] 如何取消AsyncTask？
1. A1: [Android多线程-AsyncTask的使用和问题(取消，并行和串行，屏幕切换)](https://blog.csdn.net/qq_25806863/article/details/72782050)
2. A2: [【Android基础】AsyncTask学习——如何取消掉AsyncTask](https://blog.csdn.net/zgljl2012/article/details/47258301)

#### [Q] 为什么不能在子线程更新UI？
1. A1: [android子线程不能更新UI？](https://blog.csdn.net/qingchunweiliang/article/details/84727465)

#### [Q] ANR产生的原因是什么？
1. A1: [ANR产生的原因及定位分析](https://juejin.im/entry/597026806fb9a06bcb7fc660)

#### [Q] ANR定位和修正
1. A1: [五、ANR产生的原因及其定位分析](https://www.jianshu.com/p/b015cb71e059)
#### [Q] OOM是什么？
1. A1: [什么是OOM？如何解决OOM问题!](https://www.jianshu.com/p/41ffbf31b20c)
#### [Q] 什么情况导致OOM？
1. A1: [Android OOM原因总结](https://blog.csdn.net/boyupeng/article/details/47726765)
#### [Q] 有什么解决方法可以避免OOM？
1. A1: [Android避免OOM（内存优化）](https://www.jianshu.com/p/f5d8d3066b36)
2. A2: [Android 初级探讨 OOM问题 以及解决优化之道](https://juejin.im/post/59cafa7351882531b21f0fba)

#### [Q] OOM 是否可以try catch？为什么？
1. A1: [OOm是否可以try catch](https://blog.csdn.net/gvvbn/article/details/79454701)

#### [Q] 内存泄漏是什么？
1. A1: [内存泄漏和内存溢出有啥区别？](https://www.zhihu.com/question/40560123)

#### [Q] 什么情况导致内存泄漏？内存泄露场的解决方法
1. A1: [[译]Android内存泄漏的八种可能（上）](https://www.jianshu.com/p/ac00e370f83d)
2. A2: [[译]Android防止内存泄漏的八种方法（下）](https://www.jianshu.com/p/c5ac51d804fa)

#### [Q] 如何防止线程的内存泄漏？
1. A1: [内存泄露：Thread是如何造成内存泄露的](https://www.jianshu.com/p/f50366145b4b)
2. A2: [Android性能优化：关于 内存泄露 的知识都在这里了](https://juejin.im/post/5afcebc3f265da0b7f44c10a)

#### [Q] 内存泄漏和内存溢出区别？
1. A1: [内存泄漏和内存溢出有啥区别？](https://www.zhihu.com/question/40560123)

#### [Q] LruCache默认缓存大小
1. A0: 需要自己指定，并重写相应方法做计算，源码中并没有规定默认多少。

#### [Q] ContentProvider的权限管理(解答：读写分离，权限控制-精确到表级，URL控制)
1. A1: [Content Provider的权限](https://www.cnblogs.com/622698abc/p/6033080.html)
2. A2: [ContentProvider数据库共享之——读写权限与数据监听](https://blog.csdn.net/harvic880925/article/details/44651967)

#### [Q] 如何通过广播拦截和abort一条短信？
1. A1: [广播接收器(BroadcastReceiver)](https://www.jianshu.com/p/25def4ca10e2)
2. A2: [Android的BroadcastReceiver 广播 短信拦截](https://www.cnblogs.com/chenxibobo/p/6136689.html)

#### [Q] 广播是否可以请求网络？
1. A1: onReceive回调在什么线程？[广播概览](https://developer.android.com/guide/components/broadcasts?hl=zh-cn)
2. A2: [Android主线程里不允许网络操作](https://blog.csdn.net/thl789/article/details/10628419)

#### [Q] 广播引起anr的时间限制是多少？
1. [理解Android ANR的触发原理](http://gityuan.com/2016/07/02/android-anr/)
2. [Android N 各种ANR的时间](https://blog.csdn.net/u013122625/article/details/74676666)

#### [Q] 计算一个view的嵌套层级
1. A1: [计算一个ViewGroup的嵌套层级](https://blog.csdn.net/zx_android/article/details/79558509)

#### [Q] Activity栈
1. A1: [Android Activity 全局管理 终极解决方案](https://blog.csdn.net/blogblj/article/details/52068457)

#### [Q] Android线程有没有上限？
1. A1: [57、Android线程有没有上限](https://blog.csdn.net/FDoubleman/article/details/98599279)

#### [Q] ListView重用的是什么？
1. A1: [ListView复用和优化详解](https://blog.csdn.net/u011692041/article/details/53099584)
2. A2: [Android ListView工作原理完全解析，带你从源码的角度彻底理解](https://blog.csdn.net/guolin_blog/article/details/44996879)

#### [Q] Android为什么引入Parcelable？
1. A1: [Serializable 都这么牛逼了，Parcelable，我还要你何用？](https://juejin.im/post/5a24fd8151882531ea651c37)

#### [Q] 有没有尝试简化Parcelable的使用？
1. A0: 很多回答都是讲插件..,实际AS上实现Parcelable的类名上，使用【ALT+ENTER】快捷键即可看到【Add Parcelable Implementation】选项，选择就可以完全自动创建好。。要啥插件？？？
1. A1: [kotlin使用Parcelize注解简化Parcelable的书写](https://juejin.im/entry/5a261a8c6fb9a0450167cf1b)
2. A2: 还是有一些插件选择，但没必要。
    + [Parceler](https://github.com/johncarl81/parceler)
    + [ParcelableGenerator](https://github.com/baoyongzhang/ParcelableGenerator)
    + [android-parcelable-intellij-plugin](https://github.com/mcharmas/android-parcelable-intellij-plugin)

#### [Q] ListView 中图片错位的问题是如何产生的?ListView图片加载错乱的原理和解决方案
1. A1: [Android ListView异步加载图片乱序问题，原因分析及解决方案](https://blog.csdn.net/guolin_blog/article/details/45586553)
2. A2: [listview图片加载错乱的原理和解决方案](https://blog.csdn.net/lilong_19880408/article/details/78160084)
#### [Q] 混合开发有了解吗？
1. [混合开发 框架对比](https://www.jianshu.com/p/8e99b4aed464)

#### [Q] 知道哪些混合开发的方式？说出它们的优缺点和各自使用场景？（解答：比如:RN，weex，H5，小程序，WPA等。做Android的了解一些前端js等还是很有好处的)；
1. A0: 这坑太大了。

#### [Q] 屏幕适配的处理技巧都有哪些?
1. A1: [今日头条屏幕适配方案落地研究](https://juejin.im/post/5cf869aaf265da1b8b2b4e14)
2. A2: [今日头条屏幕适配方案终极版正式发布!](https://juejin.im/post/5bce688e6fb9a05cf715d1c2)

#### [Q] 服务器只提供数据接收接口，在多线程或多进程条件下，如何保证数据的有序到达？
1. A0: 似乎没有百度到啥内容，各位答手似乎歇菜了。强答：多线程情形下可以考虑多线程同步方法，参考[LeetCode. 1114 按序打印](https://leetcode-cn.com/problems/print-in-order/),多进程的条件。。。是啥条件?文件锁?信号量?多进程同步?

#### [Q] 动态布局的理解
1. A1: [Android动态布局的实现](https://blog.csdn.net/sbl19940819/article/details/88891178?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)

#### [Q] 怎么去除重复代码？
0. A0: 个人感觉 扯一点封装/继承/多态的OOP比较好。
1. [Android-Interview/bak/resources/sourcefile/深入知识点3中高级/性能优化/-105-怎么去除重复代码.md](https://github.com/android-exchange/Android-Interview/blob/master/bak/resources/sourcefile/%E6%B7%B1%E5%85%A5%E7%9F%A5%E8%AF%86%E7%82%B93%E4%B8%AD%E9%AB%98%E7%BA%A7/%E6%80%A7%E8%83%BD%E4%BC%98%E5%8C%96/-105-%E6%80%8E%E4%B9%88%E5%8E%BB%E9%99%A4%E9%87%8D%E5%A4%8D%E4%BB%A3%E7%A0%81.md)

#### [Q] 画出 Android 的大体架构图
1. A1: Gityuan开篇俩张图，别的不用。[Android 操作系统架构开篇](http://gityuan.com/android/)
2. A2: 官方图。[平台架构](https://developer.android.com/guide/platform?hl=zh-cn)

#### [Q] 动态权限适配方案，权限组的概念
1. A1: 官方 [Permissions overview](https://developer.android.com/guide/topics/permissions/overview?hl=zh-cn)
2. A2: [Android动态权限总结](https://juejin.im/post/5bdd25386fb9a049b13da206)

#### [Q] Android系统为什么会设计ContentProvider？
1. A1: [Android系统为什么会设计ContentProvider](https://blog.csdn.net/github_37130188/article/details/89648175)

#### [Q] 下拉状态栏是不是影响activity的生命周期
1. A1: [Android 下拉通知栏时Activity的生命周期——重新理解onPause()](https://www.jianshu.com/p/781bc86f8042)

#### [Q] 如果在onStop的时候做了网络请求，onResume的时候怎么恢复？
1. A0: 问题没头没脑，不回答。

#### [Q] Bitmap 使用时候注意什么？Bitmap如何处理大图，如一张30M的大图，如何预防OOM
1. A1: [Bitmap 使用时候注意什么？](https://www.jianshu.com/p/fbf5a310788c)

#### [Q] Bitmap的recycle()
1. A1: [Android中有没有必要调用Bitmap的recycle()](https://www.jianshu.com/p/b84b1b5f2fe9)

#### [Q] Android中开启摄像头的主要步骤
1. A0: 前置步骤是申请权限，后面分为Camera，Camera2
2. A1: [Android 相机1 之Camera1的最简单的使用（预览、拍照、变焦、特效）](https://blog.csdn.net/Lingbulei/article/details/81280094)
3. A2: [Android Camera-Camera2使用](https://juejin.im/post/5e425a386fb9a07cc32135e1)
4. A3: [Android短视频中如何实现720P磨皮美颜录制？](http://yunxin.163.com/blog/video17-0905/)

#### [Q] Android Camera旋转适配
1. A1: [Android 相机开发中的尺寸和方向问题](https://glumes.com/post/android/android-camera-aspect-ratio--and-orientation/)

#### [Q] ViewPager使用细节，如何设置成每次只初始化当前的Fragment，其他的不初始化？
1. A1: [ViewPager懒加载极致优化](https://juejin.im/post/5d37bb8df265da1b8b2ba01a)

#### [Q] 点击事件被拦截，但是想传到下面的View，如何操作？
1. A1: [点击事件被拦截，但是想传到下面的View，如何操作](https://blog.csdn.net/github_37130188/article/details/89684468)

#### [Q] 微信主页面的实现方式
0. A0: 讲个笑话:给我写个APP就照着微信抄一下。
1. A1: [Android:TabLayout+ViewPager+Fragment实现底部导航](https://blog.csdn.net/ruancw/article/details/80494503)

#### [Q] 微信上消息小红点的原理
0. A0: 小红点UI实现很简单，关键在于UI怎么和消息绑定。后面又可以引申出长连接。
1. A1: [简单实现消息提示(小红点)](https://blog.csdn.net/qq_28268507/article/details/70314844)

#### [Q] 图片库对比
1. A1: [图片加载库比较](https://juejin.im/entry/5af9aabf51882542bd69d0c0)
2. A2: [Android 库 图片库比较](https://www.jianshu.com/p/44a4ee648ab4)

#### [Q] 图片库的源码分析
1. A1: [Android：这是一份全面 & 详细的图片加载库Glide源码分析](https://juejin.im/post/5ab061236fb9a028c979e043)
2. A2: [Glide 源码分析解读-基于最新版Glide 4.9.0](https://www.jianshu.com/p/9bb50924d42a)

#### [Q] 图片框架缓存实现
1. A1: [Glide 系列（四） Glide缓存机制](https://www.jianshu.com/p/17644406396b)

#### [Q] LRUCache原理
1. A1: [彻底解析Android缓存机制——LruCache](https://www.jianshu.com/p/b49a111147ee)

#### [Q] 图片加载原理
1. A1: [Android图片加载库的理解](https://www.cnblogs.com/cr330326/p/5585021.html)

#### [Q] 自己去实现图片库，怎么做？
1. [如何实现一个图片加载框架](https://juejin.im/post/5bca698751882576676f606a)

#### [Q] Glide源码解析
1. A1: 
    + [Glide源码解析(一)](https://yuqirong.me/2019/08/04/Glide%E6%BA%90%E7%A0%81%E8%A7%A3%E6%9E%90(%E4%B8%80)/)
    + [Glide源码解析(二)](https://yuqirong.me/2019/08/06/Glide%E6%BA%90%E7%A0%81%E8%A7%A3%E6%9E%90(%E4%BA%8C)/)
    + [Glide源码解析(三)](https://yuqirong.me/2019/08/07/Glide%E6%BA%90%E7%A0%81%E8%A7%A3%E6%9E%90(%E4%B8%89)/)

#### [Q] Glide使用什么缓存？
1. A1: [Glide中的缓存](https://www.jianshu.com/p/325bd2f56ca7)

#### [Q] Glide内存缓存如何控制大小？
1. A1: [Glide 这样用，更省内存！！！](https://juejin.im/post/59cf0f9e6fb9a00a4b0c73d4)

#### [Q] 网络框架对比和源码分析
1. A1: [网络框架分析 - 全是套路 | 掘金技术征文](https://juejin.im/entry/585279ac61ff4b006844f829)
2. A2: [okhttp,retrofit,android-async-http,volley应该选择哪一个？](https://www.zhihu.com/question/35189851)
3. A3: [Android主流网络请求开源库的对比（Android-Async-Http、Volley、OkHttp、Retrofit）](https://carson-ho.github.io/2016/08/12/%E7%BD%91%E7%BB%9C%E5%BC%80%E6%BA%90%E5%BA%93/)

#### [Q] 自己去设计网络请求框架，怎么做？
1. A1: [Android客户端HTTP网络框架设计与实践](https://ivonhoe.github.io/2018/07/08/network-architecture-design/)
2. A2: [一步步封装实现自己的网络请求框架](https://www.imooc.com/article/283168)

#### [Q] okhttp源码
1. A1: [针对知名网络库OkHttp3的源码分析系列文章](https://github.com/avenwu/okhttp-in-action)

#### [Q] 网络请求缓存处理，okhttp如何处理网络缓存的
1. A1: [Okhttp解析（五）缓存的处理](jianshu.com/p/00d281c226f6)
2. A2: [OkHttp 源码分析（二）—— 缓存机制](https://zhuanlan.zhihu.com/p/59765130)

#### [Q] 从网络加载一个10M的图片，说下注意事项
1. A1: [Android 大图加载](https://www.jianshu.com/p/7c81d3742c38)
2. A2: [Android高效加载大图、多图解决方案，有效避免程序OOM](https://blog.csdn.net/guolin_blog/article/details/9316683)

#### [Q] 谈谈你对安卓签名的理解。
1. A1: [安卓应用签名机制分析](https://juejin.im/post/5c9a25fce51d455bea55fa1f)

#### [Q] 请解释安卓为啥要加签名机制?
1. A1: [为您的应用签名](https://developer.android.com/studio/publish/app-signing?hl=zh-cn)

#### [Q] 视频加密传输
1. A1: [Android视频加密那点事儿！](https://blog.csdn.net/shenshibaoma/article/details/79003854)

#### [Q] App 是如何沙箱化，为什么要这么做？
1. A1: [浅析Android沙箱模型](https://blog.csdn.net/ljheee/article/details/53191397)

#### [Q] 权限管理系统（底层的权限是如何进行 grant 的）？
1. A1: [Android动态权限管理原理（6.0及以上）](http://skyacer.github.io/2018/09/06/Android%E5%8A%A8%E6%80%81%E6%9D%83%E9%99%90%E7%AE%A1%E7%90%86%E5%8E%9F%E7%90%86%EF%BC%886-0%E5%8F%8A%E4%BB%A5%E4%B8%8A%EF%BC%89/)
2. A2: [Android: 动态运行时权限(危险权限)源码分析、封装、及9.0权限改动](https://blog.csdn.net/qq_39969226/article/details/104188173)

#### [Q] sqlite升级，增加字段的语句
1. A1: [android sqlit数据库升级，添加字段](https://blog.csdn.net/mafei852213034/article/details/55096032)
2. A2: [Sqlite升级时向已有表中增加字段](https://blog.csdn.net/qq_26287435/article/details/82585597)

#### [Q] 数据库框架对比和源码分析
1. A1: [ORM数据库框架 SQLite 常用数据库框架比较 MD](https://www.cnblogs.com/baiqiantao/p/9492180.html)

#### [Q] 数据库的优化
1. A1: [android数据库优化](https://www.jianshu.com/p/3b4452fc1bbd)

#### [Q] 数据库数据迁移问题
1. A1: [Android 数据库综述（一） 数据库片的升级与数据的迁移操作](https://juejin.im/post/59e7e5856fb9a0451542fb19)

#### [Q] 对热修复和插件化的理解
1. A1: [2020 Android 大厂面试（五）插件化、模块化、组件化、热修复、增量更新、Gradle](https://juejin.im/post/5dd274515188254c6443815e)
2. 
#### [Q] 插件化原理分析 热修复,插件化
1. A1: 
    + [Android 插件化原理解析——概要](http://weishu.me/2016/01/28/understand-plugin-framework-overview/)
    + [Android 插件化原理解析——Hook机制之Binder Hook](http://weishu.me/2016/02/16/understand-plugin-framework-binder-hook/)
    + [Android 插件化原理解析——Hook机制之AMS&PMS](http://weishu.me/2016/03/07/understand-plugin-framework-ams-pms-hook/)
    + [Android 插件化原理解析——Activity生命周期管理](http://weishu.me/2016/03/21/understand-plugin-framework-activity-management/)
    + [Android 插件化原理解析——插件加载机制](http://weishu.me/2016/04/05/understand-plugin-framework-classloader/)
    + [Android 插件化原理解析——广播的管理](http://weishu.me/2016/04/12/understand-plugin-framework-receiver/)
    + [Android 插件化原理解析——Service的插件化](http://weishu.me/2016/05/11/understand-plugin-framework-service/)
    + [Android 插件化原理解析——ContentProvider的插件化](http://weishu.me/2016/07/12/understand-plugin-framework-content-provider/)
2. A2: [腾讯零反射全动态Android插件框架Shadow解析](https://juejin.im/post/5d0ed3b46fb9a07ef63fe730)
3. A3: [Android 插件化和热修复知识梳理](https://www.jianshu.com/p/704cac3eb13d)

#### [Q] 模块化实现（好处，原因）
1. A1: [关于Android模块化你需要知道的](https://juejin.im/post/5ac42a356fb9a028cf32acaf)
2. A2: [Android 模块化探索与实践](https://zhuanlan.zhihu.com/p/26744821)

#### [Q] 项目组件化的理解
1. A1: [谈谈我的理解-组件化/模块化](https://www.jianshu.com/p/79e4df63f31f)

#### [Q] 描述清点击 Android Studio 的 build 按钮后发生了什么
1. A1: [在 AndroidStudio 工程点击 Run 按钮， 实际上做了什么操作呢？](https://www.zhihu.com/question/65289196)
2. A2: [10分钟了解Android项目构建流程](https://juejin.im/post/5a69c0ccf265da3e2a0dc9aa)

#### [Q] 谈谈你对Android设计模式的理解
1. A1: [谈谈23种设计模式在Android源码及项目中的应用](https://www.jianshu.com/p/b2d62447c9ea)

#### [Q] MVC MVP MVVM原理和区别
1. A1: [MVC，MVP 和 MVVM 的图示](https://www.ruanyifeng.com/blog/2015/02/mvcmvp_mvvm.html)
2. A2: [Clean Architecture - 清晰简洁的Android 应用架构](https://www.jianshu.com/p/3edcf85539a6)
3. A3: [Android构架系列之二--MVP&&Clean理解与实践之MVP](https://limuzhi.com/2016/05/02/Android%E6%9E%84%E6%9E%B6%E7%B3%BB%E5%88%97%E4%B9%8B%E4%BA%8C-MVP&&Clean%E7%90%86%E8%A7%A3%E4%B8%8E%E5%AE%9E%E8%B7%B5%E4%B9%8BMVP/)

#### [Q] 你所知道的设计模式有哪些？项目中常用的设计模式
1. A1: [从Android代码中来记忆23种设计模式](https://www.jianshu.com/p/1a9f571ad7c0)
2. A2: [有哪些在实际 Android 项目中用到的设计模式？](https://www.zhihu.com/question/29575295)

#### [Q] 手写生产者/消费者模式
1. A1: [Java 生产者消费者实现 —— BlockingQueue](https://www.jianshu.com/p/a42b89287359)

#### [Q] 写出观察者模式的代码
1. A1: [基于Java的设计模式-观察者模式](https://panlf.github.io/2018/03/31/%E5%9F%BA%E4%BA%8EJava%E7%9A%84%E8%AE%BE%E8%AE%A1%E6%A8%A1%E5%BC%8F-%E8%A7%82%E5%AF%9F%E8%80%85%E6%A8%A1%E5%BC%8F/)

#### [Q] 适配器模式，装饰者模式，外观模式的异同？
1. A1: 装饰模式是“新增行为”，代理模式是“控制访问行为”，适配器模式是"转换行为"，外观模式是一种"简化行为"。
2. A2: [装饰器模式、代理模式、适配器模式和外观模式的联系与区别](https://www.jianshu.com/p/62799da46ac6)

#### [Q] 用到的一些开源框架，介绍一个看过源码的，内部实现过程。
1. A1: Glide源码分析.
2. A2: ButterKnife源码分析.
3. A3: EventBus源码分析.
    + [一文彻底搞懂EventBus 3.0原理](https://juejin.im/post/5da97188e51d4524a21c481f)
#### [Q] 谈谈对RxJava的理解
#### [Q] RxJava的功能与原理实现
#### [Q] RxJava的作用，与平时使用的异步操作来比的优缺点
#### [Q] 说说EventBus作用，实现方式，代替EventBus的方式
1. A1: [用LiveDataBus替代RxBus、EventBus——Android消息总线的演进之路](https://juejin.im/post/5b5ac0825188251acd0f3777)
2. A2: [greenrobot/EventBus](https://github.com/greenrobot/EventBus)
#### [Q] 从0设计一款App整体架构，如何去做？
1. A1: [Android项目开发如何设计整体架构？](https://www.zhihu.com/question/45517397)

#### [Q] 说一款你认为当前比较火的应用并设计(比如：直播APP，P2P金融，小视频等)
#### [Q] 谈谈对java状态机理解
1. A1: [状态机思维](http://blog.maihaoche.com/zhuang-tai-ji-si-wei/)
2. A2: [深入浅出理解有限状态机](https://www.jianshu.com/p/5eb45c64f3e3)

#### [Q] Fragment如果在Adapter中使用应该如何解耦？

#### [Q] Binder机制及底层实现
1. A1: [Binder系列—开篇](http://gityuan.com/2015/10/31/binder-prepare/)
2. A2: 该文似乎评价很高[Android Bander设计与实现 - 设计篇](https://blog.csdn.net/universus/article/details/6211589)
 
#### [Q] 对于应用更新这块是如何做的？(解答：灰度，强制更新，分区域更新)？
1. A1: [MS(5)：android之进阶篇](https://www.jianshu.com/p/e8a4d65ea2d9)
2. A2: [https://blog.csdn.net/ddnosh/article/details/100091866](https://blog.csdn.net/ddnosh/article/details/100091866)
#### [Q] 实现一个Json解析器(可以通过正则提高速度)
1. A1: [半小时实现一个 JSON 解析器](https://zhuanlan.zhihu.com/p/28049617)
2. A2: [JSON Parser](http://0x100.club/projects/json-parser.html)

#### [Q] 统计启动时长,标准
1. A1: [Android 开发之 App 启动时间统计](https://www.jianshu.com/p/c967653a9468)

#### [Q] 如何对Android 应用进行性能分析以及优化?
1. A1: [Android性能优化全方面解析](https://juejin.im/post/5a0d30e151882546d71ee49e)

#### [Q] ddms 和 traceView
1. A1: [利用 Android Profiler 测量应用性能](https://developer.android.com/studio/profile/android-profiler?hl=zh-cn)

#### [Q] 性能优化如何分析systrace？
1. A1: [Systrace 概览](https://developer.android.com/studio/profile/systrace.html)
2. A2: [使用Systrace分析UI性能](https://www.jianshu.com/p/b492140a555f)

#### [Q] 用IDE如何分析内存泄漏？
1. A1: [使用Android Studio和MAT进行内存泄漏分析](https://zhuanlan.zhihu.com/p/27593816)
#### [Q] Java多线程引发的性能问题，怎么解决？
1. A1: [Android性能优化典范之多线程篇](https://juejin.im/entry/59f82808f265da43346f36fd)

#### [Q] 启动页白屏及黑屏解决？
1. A1: [Android启动页黑屏及最优解决方案](https://juejin.im/post/58ad90518ac2472a2ad9b684)

#### [Q] 启动太慢怎么解决？怎么保证应用启动不卡顿？
1. A1: [Android性能优化（一）之启动加速35%](https://www.jianshu.com/p/f5514b1a826c)
2. A2 [应用启动时间](https://developer.android.com/topic/performance/vitals/launch-t)
3. A3: [面试官：今日头条启动很快，你觉得可能是做了哪些优化？](https://juejin.im/post/5d95f4a4f265da5b8f10714b)

#### [Q] 90hz 120hz 适配？影响?
1. A1: [Android 新的流畅体验，90Hz 漫谈](https://www.androidperformance.com/2019/05/15/90hz-on-android/)

#### [Q] App启动崩溃异常捕捉
1. A1: [Android开发之打造永不崩溃的APP——Crash防护](https://www.jianshu.com/p/01b69d91a3a8)

#### [Q] 自定义View注意事项
1. A1: [Android自定义View注意事项](https://www.jianshu.com/p/9862cddca1b3)
2. A2: [自定义视图组件](https://developer.android.com/guide/topics/ui/custom-components?hl=zh-cn)

#### [Q] 现在下载速度很慢,试从网络协议的角度分析原因,并优化(提示：网络的5层都可以涉及)。

#### [Q] Https请求慢的解决办法（提示：DNS，携带数据，直接访问IP）
1. A1: [弱网优化在支付宝的深度实践 | mPaaS 线下沙龙 CodeDay#1 分享实录](https://juejin.im/post/5ca5c174f265da30cc7919d1)
2. A2: 百度弱网优化
    + [百度 App 网络深度优化系列（一）：DNS 优化](https://www.infoq.cn/article/3QZ0o9Nmv*O0LoEPVRkN)
    + [百度 App 网络深度优化系列（二）：连接优化](https://www.infoq.cn/article/CDaih849Ao4rS_pctQ2T)
    + [百度 App 网络深度优化系列（三）：弱网优化](https://www.infoq.cn/article/pQmLUECekW*DsymqbGvy)
3. A3: [Android 使用OkHttp支持HttpDNS](https://blog.csdn.net/sbsujjbcy/article/details/50532797)

#### [Q] 如何保持应用的稳定性
1. A1: [Android APP性能优化的一些思考](https://juejin.im/entry/5a37a74b5188257d391d2665)

#### [Q] RecyclerView和ListView的性能对比
1. A1: [【腾讯Bugly干货分享】Android ListView 与 RecyclerView 对比浅析—缓存机制](https://zhuanlan.zhihu.com/p/23339185)
2. A2: [我们为什么要使用RecyclerView](http://zjutkz.net/2016/08/10/%E6%88%91%E4%BB%AC%E4%B8%BA%E4%BB%80%E4%B9%88%E8%A6%81%E4%BD%BF%E7%94%A8RecyclerView/)

#### [Q] ListView的优化
1. A1: [ListView的优化](https://www.jianshu.com/p/f0408a0f0610)

#### [Q] RecycleView优化
1. A1: [RecyclerView 性能优化 | 安卓 offer 收割基](https://blankj.com/2018/09/29/optimize-recycler-view/)
2. A2: [看完感觉我RecyclerView白学了！](https://www.itcodemonkey.com/article/13649.html)

#### [Q] View渲染
1. A1: [Android进阶——性能优化之布局渲染原理和底层机制机详解及卡顿根源探究（四）](https://blog.csdn.net/CrazyMo_/article/details/80038948)
2. A2: [深入Android渲染机制](https://www.jianshu.com/p/1ef2a9e5aa91)

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

#### [Q] 请介绍一下NDK 什么是NDK库? JNI 用过吗？
1. A1: [NDK 入门指南](https://developer.android.com/ndk/guides)

#### [Q] 如何JNI中注册native函数，有几种注册方式?
1. A1: [Andoid NDK编程 1 － 注册native函数](http://zhixinliu.com/2015/07/01/2015-07-01-jni-register/)
2. A2: [JNI两种注册过程实战](https://blog.csdn.net/XSF50717/article/details/54693802)

#### [Q] Java如何调用c、c++语言？
1. A1: [怎么实现Java调用C++代码？](https://www.zhihu.com/question/36666057)
#### [Q] JNI如何调用java层代码？
1. A1: [[JNI]开发之旅（7）JNI函数中调用java对象的方法](https://blog.csdn.net/honjane/article/details/53958166)

#### [Q] 进程间通信的方式？
1. A1: [【朝花夕拾】Android性能篇之（七）Android跨进程通信篇](https://www.cnblogs.com/andy-songwei/p/10256379.html)
2. A2: [Android 多进程通信](https://juejin.im/post/5aa08cb3f265da23766ad734)
#### [Q] Binder机制
1. A1: [Android跨进程通信：图文详解 Binder机制 原理](https://blog.csdn.net/carson_ho/article/details/73560642)

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
#### [Q] 什么是协程？
1. A1: [协程](https://www.liaoxuefeng.com/wiki/897692888725344/923057403198272)

#### [Q] Java虚拟机的特性 谈谈对jvm的理解
1. A1: [关于Jvm知识看这一篇就够了](https://zhuanlan.zhihu.com/p/34426768)

#### [Q] JVM内存区域，开线程影响哪块内存 JVM内存模型，内存区域
1. A1: [可能是把Java内存区域讲的最清楚的一篇文章](https://juejin.im/post/5b7d69e4e51d4538ca5730cb)
2. A2: [JVM内存区域与多线程](https://www.jianshu.com/p/ece1bb5fa88b)
3. A3: [浅谈JVM虚拟机内存区域](https://www.yimipuzi.com/1036.html)
#### [Q] 对Dalvik、ART虚拟机有什么了解？Art和Dalvik对比
1. A1: [Android Runtime (ART) 和 Dalvik](https://source.android.google.cn/devices/tech/dalvik)
2. A2: [art和dalvik的区别？](https://www.zhihu.com/question/29406156)

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

#### [Q] Ubuntu编译安卓系统
1. A2: [自己动手编译Android源码(超详细)](https://www.jianshu.com/p/367f0886e62b)

#### [Q] 系统启动流程是什么？（提示：Zygote进程 –> SystemServer进程 –> 各种系统服务 –> 应用进程）
1. A1: [Android 操作系统架构开篇](http://gityuan.com/android/) [系统启动架构图](http://gityuan.com/images/android-arch/android-boot.jpg)
2. A2: [群里收的一张图,请点击链接查看](https://raw.githubusercontent.com/rabbitknight/AndroidInterview/master/res/images/12575795F0092F2F5084C6A9BB3B7CD11AB9978E.png)

#### [Q] 大体说清一个应用程序安装到手机上时发生了什么
1. A1: [Android应用程序安装过程源代码分析](https://blog.csdn.net/Luoshengyang/article/details/6766010)
2. A2: [Android应用安装过程深度解析](http://4ch12dy.site/2019/08/01/android-apk-install-process/android-apk-install-process/)
3. A3: [Android应用安装流程分析](http://solart.cc/2016/10/30/install_apk/)

#### [Q] App启动流程，从点击桌面开始 简述Activity启动全部过程
1. A1: [startActivity启动过程分析](http://gityuan.com/2016/03/12/start-activity/)
2. A2: [App 启动过程（含 Activity 启动过程） | 安卓 offer 收割基](https://blankj.com/2018/09/29/the-process-of-app-start/)
3. A3: [Android进阶——Android四大组件启动机制之Activity启动过程](https://blog.csdn.net/qq_30379689/article/details/79611217)

#### [Q] 逻辑地址与物理地址，为什么使用逻辑地址？
1. A1: [逻辑地址、线性��址和物理地址](https://vosamo.github.io/2016/01/VA2PA/)
2. A2: [操作系统 内存地址（逻辑地址、线性地址、物理地址）概念](https://blog.51cto.com/laoxu/1166661)

#### [Q] 用户态和核心态
1. A1: [怎样去理解Linux用户态和内核态？](https://zhuanlan.zhihu.com/p/69554144)
#### [Q] Linux系统地址空间
1. A1: [Linux的进程地址空间（一）](https://zhuanlan.zhihu.com/p/66794639)

#### [Q] Android为每个应用程序分配的内存大小是多少？
1. A1: [Android为每个应用分配多少内存？](https://zhuanlan.zhihu.com/p/27269803)

#### [Q] Android中进程内存的分配，能不能自己分配定额内存？
1. A1: [Android中App可分配内存的大小](https://www.cnblogs.com/yaowen/p/6347682.html)

#### [Q] 进程保活的方式 如何保证一个后台服务不被杀死？ ;相同问题：如何保证service在后台不被kill？比较省电的方式是什么？ ;App中唤醒其他进程的实现方式
1. A1: [史上最强Android保活思路：深入剖析腾讯TIM的进程永生技术](https://www.jianshu.com/p/2e01569f8ba8)
2. A2: [2020年了，Android后台保活还有戏吗？看我如何优雅的实现！](http://www.52im.net/thread-2881-1-1.html)

#### [Q] epoll机制是啥
1. A1: [大话 Select、Poll、Epoll](https://cloud.tencent.com/developer/article/1005481)
2. A2: [IO多路复用之epoll总结](https://www.cnblogs.com/Anker/p/3263780.html)
#### [Q] Android 对于Input系统处理流程
1. A1: [Input系统—事件处理全过程](http://gityuan.com/2016/12/31/input-ipc/)

#### [Q] GC算法(各种算法的优缺点以及应用场景)
1. [JVM常见的几种GC算法](https://russxia.com/2019/07/25/JVM%E5%B8%B8%E8%A7%81%E7%9A%84%E5%87%A0%E7%A7%8DGC%E7%AE%97%E6%B3%95/)

#### [Q] Android ART上GC算法
1. A1: [Android GC 从dalvik到ART的改进分析](https://cruise1008.github.io/2016/03/30/Android-GC-%E4%BB%8Edalvik%E5%88%B0ART%E7%9A%84%E6%94%B9%E8%BF%9B%E5%88%86%E6%9E%90/)
2. A2: [Android GC原理探究](https://zhuanlan.zhihu.com/p/24835977)
3. A3: [Android-浅析-GC-基础原理](https://jasonzhong.github.io/2017/09/28/Android-%E6%B5%85%E6%9E%90-GC-%E5%9F%BA%E7%A1%80%E5%8E%9F%E7%90%86/)

#### [Q] RenderScript有无使用过
1. A1: [RenderScript 概览](https://developer.android.com/guide/topics/renderscript/compute)

#### [Q] 在Android中两个进程之间传输大数据，可以使用什么方式实现?这些方式中哪种方式最高效?请说明原因。
1. A1: 推荐使用MemoryFile,高版本修改为SharedMemory。核心都是通过Binder传输序列化的文件描述符，一边发送一边接收。

#### [Q] 如何监控应用性能
1. A1: [Android Choreographer 源码分析](https://www.jianshu.com/p/996bca12eb1d)
2. A2: [Android 基于 Choreographer 的渲染机制详解](https://www.androidperformance.com/2019/10/22/Android-Choreographer/)

</details>

### 数据结构和算法

<details>

#### [Q] 如何判断链表有回环
1. [为什么用快慢指针找链表的环，快指针和慢指针一定会相遇？](https://www.zhihu.com/question/23208893)

#### [Q] 常用排序算法; 排序算法有哪些;手写一个冒泡排序;手写快速排序代码;快速排序的过程、时间复杂度、空间复杂度;手写堆排序;堆排序过程、时间复杂度及空间复杂度 ;写出你所知道的排序算法及时空复杂度，稳定性
1. A1: [十大经典排序算法（动图演示）](https://www.cnblogs.com/onepixel/p/7674659.html)
2. A2: [[算法总结] 十大排序算法](https://zhuanlan.zhihu.com/p/42586566)
#### [Q] 二叉树遍历和搜索
1. A1: [二叉树遍历(先序、中序、后序)](https://www.jianshu.com/p/456af5480cee)
2. A2: [二叉树遍历（前序、中序、后序、层次遍历、深度优先、广度优先）](https://blog.csdn.net/My_Jobs/article/details/43451187)
3. A3: [通俗易懂讲解 二叉搜索树](https://zhuanlan.zhihu.com/p/29867652)

#### [Q] 最快的排序算法是哪个？
1. A1: [总结5种比较高效常用的排序算法](https://blog.csdn.net/hl_java/article/details/72499914)

#### [Q] 二叉树给出根节点和目标节点，找出从根节点到目标节点的路径
1. A0: 二叉树遍历+通过根节点获取路径

#### [Q] 给阿里2万多名员工按年龄排序应该选择哪个算法？
1. A1: 直接计数排序[对公司几万名员工按年龄排序（时间复杂度为O(N)）](https://blog.csdn.net/dai_wen/article/details/79961168)

#### [Q] 蚁群算法与蒙特卡洛算法
0. A0: 这似乎难度有点高
1. A1: 蚁群算法
    + [10分钟搞懂蚁群算法](https://juejin.im/post/5aa4ddf6f265da23870e73d1)
    + [干货|十分钟快速get蚁群算法（附代码） - 知乎](https://zhuanlan.zhihu.com/p/45985636)
2. A2: 蒙特卡洛算法
    1. [蒙特卡罗算法是什么？](https://www.zhihu.com/question/20254139)
    
#### [Q] 子串包含问题(KMP 算法)写代码实现
#### [Q] 一个无序，不重复数组，输出N个元素，使得N个元素的和相加为M，给出时间复杂度、空间复杂度。手写算法
#### [Q] 万亿级别的两个URL文件A和B，如何求出A和B的差集C(提示：Bit映射->hash分组->多文件读写效率->磁盘寻址以及应用层面对寻址的优#### [Q] 化)
#### [Q] 百度POI中如何试下查找最近的商家功能(提示：坐标镜像+R树)。
#### [Q] 两个不重复的数组集合中，求共同的元素。
#### [Q] 两个不重复的数组集合中，这两个集合都是海量数据，内存中放不下，怎么求共同的元素？
#### [Q] 一个文件中有100万个整数，由空格分开，在程序中判断用户输入的整数是否在此文件中。说出最优的方法
#### [Q] 一张Bitmap所占内存以及内存占用的计算
#### [Q] 2000万个整数，找出第五十大的数字？
#### [Q] 烧一根不均匀的绳，从头烧到尾总共需要1个小时。现在有若干条材质相同的绳子，问如何用烧绳的方法来计时一个小时十五分钟呢？
#### [Q] 求1000以内的水仙花数以及40亿以内的水仙花数
#### [Q] 5枚硬币，2正3反如何划分为两堆然后通过翻转让两堆中正面向上的硬8币和反面向上的硬币个数相同
#### [Q] 时针走一圈，时针分针重合几次
#### [Q] N*N的方格纸,里面有多少个正方形
#### [Q] x个苹果，一天只能吃一个、两个、或者三个，问多少天可以吃完？

</details>

### 其他

<details>
</details>

## Thanks

## 推荐链接
1. [@扔物线:Hencoder全系](https://hencoder.com/)
2. [@Gityuan:Android 操作系统架构](http://gityuan.com/android/)
3. [最全的BAT大厂面试题整理](https://www.jianshu.com/p/c70989bd5f29)
4. Android篇：2019初中级Android开发社招面试解答
    + [上](https://juejin.im/post/5c8211fee51d453a136e36b0)
    + [中](https://juejin.im/post/5c85cead5188257c6703af47)
    + [下](https://juejin.im/post/5c984e926fb9a070c975a9b4)
5. [XXXX题集](https://raw.githubusercontent.com/rabbitknight/AndroidInterview/master/res/pdfs/13E93ADE59269EE7CDD386C9602983A8CB0B6AC313B027B538E1BF214E54BE8C.pdf)
6. [Android Tech And Perf](https://www.androidperformance.com/2019/12/01/BlogMap/)