# AndroidInterview
本仓库仅用于收集和整理面试问题

[TOC]

## TL;DR
1. 一共分为4大类，Java相关、Android相关、数据结构和算法、其他
2. 尽量不推荐直接告诉答案(除非很简单)，尽可能收集相关文档
3. 后期强烈考虑对文档进行评级。
4. 优先推荐官方文档。

## 暂行细则
1. 所有题目以4级标题<####>提供,类似[Q] XXXX
2. 所有题目回答以[A]标记作为开始，分为A1 A2 A3 ...
3. 如果要贴图，请将原图(附带水印)至于[</res/images/>](https://github.com/rabbitknight/AndroidInterview/tree/master/res/images)目录
4. 如果要PDF文档，请将文档，至于 [</res/pdfs/>](https://github.com/rabbitknight/AndroidInterview/tree/master/res/pdfs)
5. 等级标识 三级描述：

标识 | 说明
--- | ---
![低](https://img.shields.io/badge/level-BASE-green) | 低 
![中](https://img.shields.io/badge/level-MIDDLE-blue) | 中 
![高](https://img.shields.io/badge/level-HARD-red) | 高 

6. 特殊标识：

标识|说明
---|---
![推荐-官方](https://img.shields.io/badge/rating-官方-orange) | 官方文档
![推荐-XXXX](https://img.shields.io/badge/rating-XXX-orange) | 等级推荐
![不推荐](https://img.shields.io/badge/rating-不推荐-RED) | 不推荐


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
    + A 里面激活B 组件的时候, A会调用onPause()方法,然后B调用onCreate() ,onStart(), onResume()。B覆盖了A的窗体, A会调用onStop()方法。
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

#### [Q] looper架构
1. 推荐@Gityuan大佬的全系文章: [Android消息机制1-Handler(Java层)](http://gityuan.com/2015/12/26/handler-message-framework/)

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

#### [Q] OkHttp缓存机制
1. A1: [OKHttp全解析系列（五） --OKHttp的缓存机制](https://www.jianshu.com/p/fb81207af121)


#### [Q] 如何提升Activity开启速度
1. A1: [提升进入界面的速度](https://zmywly8866.github.io/2015/09/28/promote-enter-activity-speed.html)

#### [Q] Handler机制和底层实现
#### [Q] Handler、Thread和HandlerThread的差别
#### [Q] handler发消息给子线程，looper怎么启动？
#### [Q] 关于Handler，在任何地方new Handler 都是什么线程下?
#### [Q] ThreadLocal原理，实现及如何保证Local属性？
#### [Q] 请解释下在单线程模型中Message、Handler、Message Queue、Looper之间的关系
#### [Q] 请描述一下View事件传递分发机制
#### [Q] Touch事件传递流程
#### [Q] 事件分发中的onTouch 和onTouchEvent 有什么区别，又该如何使用？
#### [Q] View和ViewGroup分别有哪些事件分发相关的回调方法
#### [Q] View刷新机制
#### [Q] View绘制流程
#### [Q] 自定义控件原理
#### [Q] 自定义View如何提供获取View属性的接口？
#### [Q] Android代码中实现WAP方式联网
#### [Q] AsyncTask机制
#### [Q] AsyncTask原理及不足
#### [Q] 如何取消AsyncTask？
#### [Q] 为什么不能在子线程更新UI？
#### [Q] ANR产生的原因是什么？
#### [Q] ANR定位和修正
#### [Q] oom是什么？
#### [Q] 什么情况导致oom？
#### [Q] 有什么解决方法可以避免OOM？
#### [Q] Oom 是否可以try catch？为什么？
#### [Q] 内存泄漏是什么？
#### [Q] 什么情况导致内存泄漏？
#### [Q] 如何防止线程的内存泄漏？
#### [Q] 内存泄露场的解决方法
#### [Q] 内存泄漏和内存溢出区别？
#### [Q] LruCache默认缓存大小
#### [Q] ContentProvider的权限管理(解答：读写分离，权限控制-精确到表级，URL控制)
#### [Q] 如何通过广播拦截和abort一条短信？
#### [Q] 广播是否可以请求网络？
#### [Q] 广播引起anr的时间限制是多少？
#### [Q] 计算一个view的嵌套层级
#### [Q] Activity栈
#### [Q] Android线程有没有上限？
#### [Q] 线程池有没有上限？
#### [Q] ListView重用的是什么？
#### [Q] Android为什么引入Parcelable？
#### [Q] 有没有尝试简化Parcelable的使用？
#### [Q] （四）开发中常见的一些问题
#### [Q] ListView 中图片错位的问题是如何产生的?
#### [Q] 混合开发有了解吗？
#### [Q] 知道哪些混合开发的方式？说出它们的优缺点和各自使用场景？（解答：比如:RN，weex，H5，小程序，WPA等。做Android的了解一些前#### [Q] 端js等还是很有好处的)；
#### [Q] 屏幕适配的处理技巧都有哪些?
#### [Q] 服务器只提供数据接收接口，在多线程或多进程条件下，如何保证数据的有序到达？
#### [Q] 动态布局的理解
#### [Q] 怎么去除重复代码？
#### [Q] 画出 Android 的大体架构图
#### [Q] Recycleview和ListView的区别
#### [Q] ListView图片加载错乱的原理和解决方案
#### [Q] 动态权限适配方案，权限组的概念
#### [Q] Android系统为什么会设计ContentProvider？
#### [Q] 下拉状态栏是不是影响activity的生命周期
#### [Q] 如果在onStop的时候做了网络请求，onResume的时候怎么恢复？
#### [Q] Bitmap 使用时候注意什么？
#### [Q] Bitmap的recycler()
#### [Q] Android中开启摄像头的主要步骤
#### [Q] ViewPager使用细节，如何设置成每次只初始化当前的Fragment，其他的不初始化？
#### [Q] 点击事件被拦截，但是想传到下面的View，如何操作？
#### [Q] 微信主页面的实现方式
#### [Q] 微信上消息小红点的原理
#### [Q] CAS介绍（这是阿里巴巴的面试题，我不是很了解，可以参考博客: CAS简介）
</details>


### 数据结构和算法

<details>

#### [Q] 如何判断链表有回环
1. [为什么用快慢指针找链表的环，快指针和慢指针一定会相遇？](https://www.zhihu.com/question/23208893)

#### [Q] 常用排序算法
1. A1: [十大经典排序算法（动图演示）](https://www.cnblogs.com/onepixel/p/7674659.html)
#### [Q] 二叉树遍历和搜索
1. A1: [二叉树遍历(先序、中序、后序)](https://www.jianshu.com/p/456af5480cee)
2. A2: [二叉树遍历（前序、中序、后序、层次遍历、深度优先、广度优先）](https://blog.csdn.net/My_Jobs/article/details/43451187)
3. A3: [通俗易懂讲解 二叉搜索树](https://zhuanlan.zhihu.com/p/29867652)

</details>

### 其他

<details>
</details>

## Thanks

## 推荐链接
1. [@扔物线:Hencoder全系](https://hencoder.com/)
2. [@Gityuan:Android 操作系统架构](http://gityuan.com/android/)
3. [最全的BAT大厂面试题整理](https://www.jianshu.com/p/c70989bd5f29)