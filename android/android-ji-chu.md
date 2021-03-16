---
description: 此章节主要为Android基础
---

# Android 基础

### TL;DR

对于基础的定义：**使用**时的区别，不求甚解

### 清单

#### [Q] 四大组件是什么
1. A1: Acitivity、Service、Broadcast、ContentProvider
2. A2: [「Android」四大组件，你真的都掌握了？ - 掘金](https://juejin.im/post/5db12d926fb9a0205e766cc2)

#### [Q] 四大组件的生命周期和简单用法
1. A1: 官网必看文档
    + Activity: [了解 Activity 生命周期](https://developer.android.com/guide/components/activities/activity-lifecycle?hl=zh-cn)
    + Service: [服务概览](https://developer.android.com/guide/components/services?hl=zh-cn​)
    + Boradcast: [广播概览](https://developer.android.com/guide/components/broadcasts)
    + ContentProvider: [内容提供程序基础知识](https://developer.android.com/guide/topics/providers/content-provider-basics)

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

#### [Q] 下拉状态栏是不是影响activity的生命周期
1. A1: [Android 下拉通知栏时Activity的生命周期——重新理解onPause()](https://www.jianshu.com/p/781bc86f8042)

#### [Q] Activity的四种启动模式对比
1. A1: 官方文档！[了解任务和返回堆栈](https://developer.android.com/guide/components/activities/tasks-and-back-stack)
2. A2: [说说 Activity 的四种启动模式](https://www.jianshu.com/p/b60d8097e519) 包含launchmode和IntentFlag

#### [Q] LaunchMode应用场景
1. [深入讲解Android中Activity launchMode](https://droidyue.com/blog/2015/08/16/dive-into-android-activity-launchmode/)

#### [Q] Activity状态保存与恢复
1. A1: [Android的状态保存和恢复](https://www.jianshu.com/p/90cf59f22f40)

#### [Q] Activity栈
1. A1: [Android Activity 全局管理 终极解决方案](https://blog.csdn.net/blogblj/article/details/52068457)

#### [Q] fragment各种情况下的生命周期
1. A1: [Fragment 在各种情况下的生命周期](https://www.geek-share.com/detail/2718616379.html)

#### [Q] Activity和Fragment状态
1. A1: [保存/恢复 Activity和Fragment状态的最佳实践](https://segmentfault.com/a/1190000006691830)

#### [Q] Fragment状态保存startActivityForResult是哪个类的方法，在什么情况下使用？
1. A1: [彻底搞懂startActivityForResult在FragmentActivity和Fragment中的异同](https://blog.csdn.net/barryhappy/article/details/53229238)

#### [Q] 如何实现Fragment的滑动？
1. A1: [ViewPager+Fragment实现页面滑动效果](https://www.jianshu.com/p/87134516445c)

#### [Q] Activity 怎么和Service 绑定？
1. A1:[谈一谈startService和bindService的区别，生命周期以及使用场景](https://github.com/Moosphan/Android-Daily-Interview/issues/53)

#### [Q] 怎么在Activity 中启动自己对应的Service？
1. A1: [Activity怎么和service绑定，怎么在activity中启动自己对应的service？](https://github.com/Sogrey/Android_QA/issues/92)

#### [Q] Service的开启方式
1. A1: [Android Service两种启动方式详解](https://www.jianshu.com/p/4c798c91a613)

#### [Q] 请描述一下Service 的生命周期
1. A1: [Android Service两种启动方式详解](https://www.jianshu.com/p/4c798c91a613)

#### [Q] IntentService原理及作用是什么？
1. A1: [理解 IntentService 原理](https://juejin.im/post/5c75f3e851882540a702ea8f)

#### [Q] 谈谈你对ContentProvider的理解
1. A1: [Android：关于ContentProvider的知识都在这里了！](https://www.jianshu.com/p/ea8bc4aaf057)

#### [Q] 说说ContentProvider、ContentResolver、ContentObserver 之间的关系
1. A1: [ContentProvider、ContentResolver、ContentObserver之间的关系](https://www.cnblogs.com/anni-qianqian/p/8391887.html)

#### [Q] 请介绍下ContentProvider 是如何实现数据共享的？
1. A1: [[问答]请介绍下ContentProvider是如何实现数据共享的](https://github.com/android-cn/android-discuss/issues/24)

#### [Q] Android系统为什么会设计ContentProvider？
1. A1: [Android系统为什么会设计ContentProvider](https://blog.csdn.net/github_37130188/article/details/89648175)


#### [Q] ContentProvider的权限管理(解答：读写分离，权限控制-精确到表级，URL控制)
1. A1: [Content Provider的权限](https://www.cnblogs.com/622698abc/p/6033080.html)
2. A2: [ContentProvider数据库共享之——读写权限与数据监听](https://blog.csdn.net/harvic880925/article/details/44651967)

#### [Q] 请描述一下广播BroadcastReceiver的理解
1. A1: ["BroadcastReceiver"-安卓面试必问技能点大总结"](https://blog.csdn.net/nzfxx/article/details/51835743)


#### [Q] 广播的分类广播使用的方式和场景
1. A1: [Android：BroadcastRecevicer广播类型汇总](https://blog.csdn.net/carson_ho/article/details/53160580)

#### [Q] 如何通过广播拦截和abort一条短信？
1. A1: [广播接收器(BroadcastReceiver)](https://www.jianshu.com/p/25def4ca10e2)
2. A2: [Android的BroadcastReceiver 广播 短信拦截](https://www.cnblogs.com/chenxibobo/p/6136689.html)

#### [Q] 在manifest 和代码中如何注册和使用BroadcastReceiver?
1. A1: [Android：在AndroidManifest中注册BroadcastReceiver的权限问题](https://blog.csdn.net/books1958/article/details/39472385)

#### [Q] 本地广播和全局广播有什么差别？BroadcastReceiver，LocalBroadcastReceiver区别
1. A1: [本地广播和全局广播的差别](https://www.jianshu.com/p/bfbb6ebc1c04)

#### [Q] Android属性动画特性
1. A1: 官方:[属性动画概览](https://developer.android.com/guide/topics/graphics/prop-animation?hl=zh-cn)
2. A2: [HenCoder Android 自定义 View 1-7：属性动画 Property Animation（进阶篇）](https://hencoder.com/ui-1-7/)

#### [Q] 差值器和估值器
1. [Animation总结(差值器和估值器)](https://www.jianshu.com/p/f18517076b40)

#### [Q] Android动画框架实现原理
1. A1: [Android三种动画实现](http://gityuan.com/2015/09/04/android-anaimator-1/)
2. A2: [源码解读Android属性动画](http://gityuan.com/2015/09/06/android-anaimator-4/)

#### [Q] 谈谈对接口与回调的理解回调的原理写一个回调demo
1. A1: [回调的原理 ？写一个回调demo](https://blog.csdn.net/qq_26358311/article/details/79607768)

#### [Q] LinearLayout、RelativeLayout、FrameLayout的特性及对比，并介绍使用场景。
1. A1: [Android UI之五种基本布局详解](https://blog.csdn.net/github_37130188/article/details/89113243)
2. A2: [帧布局（FrameLayout）](https://www.jianshu.com/p/a169cce78340)

#### [Q] 介绍下SurfaceView
1. A1: [Android中的SurfaceView详解](https://www.jianshu.com/p/b037249e6d31)

#### [Q] RecyclerView的使用
1. A1: [使用 RecyclerView 创建列表](https://developer.android.com/guide/topics/ui/layout/recyclerview?hl=zh-cn)
2. A2: [Android RecyclerView 使用完全解析 体验艺术般的控件](https://blog.csdn.net/lmj623565791/article/details/45059587)
3. A3: [图解 RecyclerView 的缓存机制](https://blog.csdn.net/weixin_43130724/article/details/90068112)

#### [Q] RecyclerView和ListView对别
1. A1: [RecyclerView 和 ListView 使用对比分析](https://www.jianshu.com/p/f592f3715ae2?utm_campaign=haruki&utm_content=note&utm_medium=reader_share&utm_source=weixin&from=singlemessage&isappinstalled=1)


#### [Q] 动态权限适配方案，权限组的概念
1. A1: 官方 [Permissions overview](https://developer.android.com/guide/topics/permissions/overview?hl=zh-cn)
2. A2: [Android动态权限总结](https://juejin.im/post/5bdd25386fb9a049b13da206)

#### [Q] @TargetApi,@RequiresApi,@SuppressLint区别
1. A1: 这三个都是面向Lint的。代码运行该崩还是会崩。
    + @TargetApi:声明代码指向哪个版本的API，不关心build.gradle指定的版本,用了压制警告，但实际低版本运行会报错。
    + @RequiresApi:声明代码需要哪个版本的API才能运行。常见如6.0权限相关的。
    + @SuppressLint：忽略Lint提示的黄色警告⚠。





