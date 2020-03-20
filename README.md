# AndroidInterview
本仓库仅用于收集和整理面试问题
[TOC]
## TL;DR
1. 一共分为4大类，Java相关、Android相关、数据结构和算法、其他
## 暂行细则
1. 所有题目以4级标题<####>提供,类似[Q] XXXX
2. 所有题目回答以[A]标记作为开始，分为A1 A2 A3 ...
3. 优先推荐官方文档。
4. 如果要贴图，请将原图(附带水印)至于[</res/images/>](https://github.com/rabbitknight/AndroidInterview/tree/master/res/images)目录
5. 如果要PDF文档，请将文档，至于 [</res/pdfs/>](https://github.com/rabbitknight/AndroidInterview/tree/master/res/pdfs)
6. 等级使用 三级描述：
![低](https://img.shields.io/badge/L-BASE-green)
![中](https://img.shields.io/badge/L-MIDDLE-blue)
![高](https://img.shields.io/badge/L-HARD-red)
7. 特殊标识：
![推荐-官方](https://img.shields.io/badge/rating-官方-orange)
![推荐-XXXX](https://img.shields.io/badge/rating-XXX-orange)

## 清单
### Java相关
<details>
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
2. A2: 两个Activity之间跳转时必然会执行的是哪几个方法？](https://blog.csdn.net/m_xiaoer/article/details/72881082)

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
#### [Q] service和activity怎么进行数据交互？
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
#### [Q] Application 和 Activity 的 Context 对象的区别
1. A1: [Application context和Activity context的区别](https://www.jianshu.com/p/4f97baa0e8f7)
2. A2: [Context 都没弄明白，还怎么做 Android 开发？](https://zhuanlan.zhihu.com/p/24847247)

#### [Q] Android属性动画特性
1. 官方:[属性动画概览](https://developer.android.com/guide/topics/graphics/prop-animation?hl=zh-cn)
3. [HenCoder Android 自定义 View 1-7：属性动画 Property Animation（进阶篇）](https://hencoder.com/ui-1-7/)
#### [Q] 如何导入外部数据库?
#### [Q] LinearLayout、RelativeLayout、FrameLayout的特性及对比，并介绍使用场景。
#### [Q] 谈谈对接口与回调的理解回调的原理写一个回调demo
#### [Q] 介绍下SurfView
#### [Q] RecycleView的使用序列化的作用，以及Android两种序列化的区别
#### [Q] 差值器
#### [Q] 估值器
#### [Q] Android中数据存储方式 
#### [Q] Android动画框架实现原理
#### [Q] Android各个版本API的区别
#### [Q] Requestlayout，onlayout，onDraw，DrawChild区别与联系
#### [Q] invalidate和postInvalidate的区别及使用
#### [Q] Activity-Window-View三者的差别
#### [Q] 谈谈对Volley的理解
#### [Q] 如何优化自定义View低版本SDK如何实现高版本api？
#### [Q] 描述一次网络请求的流程
#### [Q] HttpUrlConnection 和 okhttp关系
#### [Q] Bitmap对象的理解
#### [Q] looper架构
#### [Q] ActivityThread，AMS，WMS的工作原理
#### [Q] 自定义View如何考虑机型适配
#### [Q] 自定义View的事件
1. A1: []
#### [Q] AstncTask+HttpClient 与 AsyncHttpClient有什么区别？
#### [Q] LaunchMode应用场景
#### [Q] AsyncTask 如何使用?
#### [Q] SpareArray原理
#### [Q] 请介绍下ContentProvider 是如何实现数据共享的？
#### [Q] AndroidService与Activity之间通信的几种方式
#### [Q] IntentService原理及作用是什么？
#### [Q] 说说Activity、Intent、Service 是什么关系
#### [Q] ApplicationContext和ActivityContext的区别
#### [Q] SP是进程同步的吗?有什么方法做到同步？
#### [Q] 谈谈多线程在Android中的使用
#### [Q] 进程和 Application 的生命周期
#### [Q] 封装View的时候怎么知道view的大小
#### [Q] RecycleView原理
#### [Q] AndroidManifest的作用与理解
#### [Q] 内存泄漏优化
</details>


### 数据结构和算法

<details>
</details>

### 其他

<details>
</details>

## Thanks

## 推荐链接
1. [最全的BAT大厂面试题整理](https://www.jianshu.com/p/c70989bd5f29)
2. [Hencoder全系](https://hencoder.com/)