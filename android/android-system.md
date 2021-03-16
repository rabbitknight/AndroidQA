---
description: 此章节主要为Android 系统原理相关
---

# Android 系统

### TL; DR

啥是Android？

### 清单

#### [Q] 画出 Android 的大体架构图
1. A1: Gityuan开篇俩张图，别的不用。[Android 操作系统架构开篇](http://gityuan.com/android/)
2. A2: 官方图。[平台架构](https://developer.android.com/guide/platform?hl=zh-cn)

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

#### [Q] 低版本SDK如何实现高版本api？
1. A1: [RequiresApi](https://developer.android.com/reference/android/support/annotation/RequiresApi)
2. A2: [Android 高版本API方法在低版本系统上的兼容性处理](https://www.jianshu.com/p/6ad6490c8375)

#### [Q] 如何提升Activity开启速度
1. A1: [提升进入界面的速度](https://zmywly8866.github.io/2015/09/28/promote-enter-activity-speed.html)

#### [Q] AndroidManifest的作用与理解
1. A1: [AndroidManifest.xml详解](https://www.jianshu.com/p/3b5b89d4e154)

#### [Q] AlertDialog, popupWindow, Activity区别
1. A1: 不要人言亦言~ [关于坑爹的PopupWindow的“阻塞”争议问题：Android没有真正的“阻塞式”对话框](https://blog.csdn.net/zhengxiaoyao0716/article/details/48768407)
2. A2: 该篇文章才真正描述了实际区别: [从问题出发，解析Activity、Window、View三者关系](https://juejin.im/entry/59a3ab465188252445327481)

#### [Q] Activity-Window-View三者的差别
1. A1: [从问题出发，解析Activity、Window、View三者关系](https://juejin.im/entry/59a3ab465188252445327481)

#### [Q] Application 和 Activity 的 Context 对象的区别 ; ApplicationContext和ActivityContext的区别

1. A1: [Application context和Activity context的区别](https://www.jianshu.com/p/4f97baa0e8f7)
2. A2: [Context 都没弄明白，还怎么做 Android 开发？](https://zhuanlan.zhihu.com/p/24847247)

#### [Q] 说说Activity、Intent、Service 是什么关系
1. A0: 没啥关系。单独看Activity/Service即可。
2. A1: [Intent 和 Intent 过滤器](https://developer.android.com/guide/components/intents-filters)

#### [Q] ActivityThread，AMS，WMS的工作原理
0. 关于Android底层实现，全系推荐[gityuan](http://gityuan.com/)的文章，其他杂七杂八的先省略了！
1. A1: [理解Application创建过程](http://gityuan.com/2017/04/02/android-application/)
2. A2: [ActivityManagerService启动过程](http://gityuan.com/2016/02/21/activity-manager-service/)

#### [Q] Android硬件加速
1. [Android硬件加速原理与实现简介---美团技术团队](https://tech.meituan.com/2017/01/19/hardware-accelerate.html)

| 渲染场景 | 纯软件绘制 | 硬件加速 | 加速效果分析 |
| ---|---|---|---|
| 页面初始化 | 绘制所有View | 创建所有DisplayList | GPU分担了复杂计算任务 |
| 在一个复杂页面调用背景透明TextView的setText()，且调用后其尺寸位置不变 | 重绘脏区所有View | TextView及每一级父View重建DisplayList | 重叠的兄弟节点不需CPU重绘，GPU会自行处理 |
| TextView逐帧播放Alpha / Translation / Scale动画 | 每帧都要重绘脏区所有View | 除第一帧同场景2，之后每帧只更新TextView对应RenderNode的属性 | 刷新一帧性能极大提高，动画流畅度提高 |
| 修改TextView透明度 | 重绘脏区所有View | 直接调用RenderNode.setAlpha()更新 | 加速前需全页面遍历，并重绘很多View；加速后只触发DecorView.updateDisplayListIfDirty，不再往下遍历，CPU执行时间可忽略不计 |

#### [Q] View刷新机制
1. A1: [Android 屏幕刷新机制](https://www.jianshu.com/p/0d00cb85fdf3)
2. A2: [Android View刷新机制](https://blog.csdn.net/chenzhiqin20/article/details/8628952)

#### [Q] View渲染
1. A1: [Android进阶——性能优化之布局渲染原理和底层机制机详解及卡顿根源探究（四）](https://blog.csdn.net/CrazyMo_/article/details/80038948)
2. A2: [深入Android渲染机制](https://www.jianshu.com/p/1ef2a9e5aa91)

#### [Q] 内存泄漏优化
1. A1: [Android性能优化之内存优化](https://jsonchao.github.io/2019/08/18/Android%E6%80%A7%E8%83%BD%E4%BC%98%E5%8C%96%E4%B9%8B%E5%86%85%E5%AD%98%E4%BC%98%E5%8C%96/)

#### [Q] ANR产生的原因是什么？
1. A1: [ANR产生的原因及定位分析](https://juejin.im/entry/597026806fb9a06bcb7fc660)

#### [Q] ANR定位和修正
1. A1: [五、ANR产生的原因及其定位分析](https://www.jianshu.com/p/b015cb71e059)

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

#### [Q] OOM是什么？
1. A1: [什么是OOM？如何解决OOM问题!](https://www.jianshu.com/p/41ffbf31b20c)
#### [Q] 什么情况导致OOM？
1. A1: [Android OOM原因总结](https://blog.csdn.net/boyupeng/article/details/47726765)
#### [Q] 有什么解决方法可以避免OOM？
1. A1: [Android避免OOM（内存优化）](https://www.jianshu.com/p/f5d8d3066b36)
2. A2: [Android 初级探讨 OOM问题 以及解决优化之道](https://juejin.im/post/59cafa7351882531b21f0fba)

#### [Q] OOM 是否可以try catch？为什么？
1. A1: [OOm是否可以try catch](https://blog.csdn.net/gvvbn/article/details/79454701)


#### [Q] 屏幕适配的处理技巧都有哪些?
1. A1: [今日头条屏幕适配方案落地研究](https://juejin.im/post/5cf869aaf265da1b8b2b4e14)
2. A2: [今日头条屏幕适配方案终极版正式发布!](https://juejin.im/post/5bce688e6fb9a05cf715d1c2)

#### [Q] 怎么去除重复代码？
0. A0: 个人感觉 扯一点封装/继承/多态的OOP比较好。
1. [Android-Interview/bak/resources/sourcefile/深入知识点3中高级/性能优化/-105-怎么去除重复代码.md](https://github.com/android-exchange/Android-Interview/blob/master/bak/resources/sourcefile/%E6%B7%B1%E5%85%A5%E7%9F%A5%E8%AF%86%E7%82%B93%E4%B8%AD%E9%AB%98%E7%BA%A7/%E6%80%A7%E8%83%BD%E4%BC%98%E5%8C%96/-105-%E6%80%8E%E4%B9%88%E5%8E%BB%E9%99%A4%E9%87%8D%E5%A4%8D%E4%BB%A3%E7%A0%81.md)

#### [Q] 谈谈你对安卓签名的理解。
1. A1: [安卓应用签名机制分析](https://juejin.im/post/5c9a25fce51d455bea55fa1f)

#### [Q] 请解释安卓为啥要加签名机制?
1. A1: [为您的应用签名](https://developer.android.com/studio/publish/app-signing?hl=zh-cn)

#### [Q] App 是如何沙箱化，为什么要这么做？
1. A1: [浅析Android沙箱模型](https://blog.csdn.net/ljheee/article/details/53191397)

#### [Q] 权限管理系统（底层的权限是如何进行 grant 的）？
1. A1: [Android动态权限管理原理（6.0及以上）](http://skyacer.github.io/2018/09/06/Android%E5%8A%A8%E6%80%81%E6%9D%83%E9%99%90%E7%AE%A1%E7%90%86%E5%8E%9F%E7%90%86%EF%BC%886-0%E5%8F%8A%E4%BB%A5%E4%B8%8A%EF%BC%89/)
2. A2: [Android: 动态运行时权限(危险权限)源码分析、封装、及9.0权限改动](https://blog.csdn.net/qq_39969226/article/details/104188173)


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

#### [Q] Binder机制及底层实现
1. A1: [Binder系列—开篇](http://gityuan.com/2015/10/31/binder-prepare/)
2. A2: 该文似乎评价很高[Android Bander设计与实现 - 设计篇](https://blog.csdn.net/universus/article/details/6211589)

#### [Q] Binder机制
1. A1: [Android跨进程通信：图文详解 Binder机制 原理](https://blog.csdn.net/carson_ho/article/details/73560642)
 
#### [Q] 对于应用更新这块是如何做的？(解答：灰度，强制更新，分区域更新)？
1. A1: [MS(5)：android之进阶篇](https://www.jianshu.com/p/e8a4d65ea2d9)
2. A2: [https://blog.csdn.net/ddnosh/article/details/100091866](https://blog.csdn.net/ddnosh/article/details/100091866)

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

#### [Q] 如何保持应用的稳定性
1. A1: [Android APP性能优化的一些思考](https://juejin.im/entry/5a37a74b5188257d391d2665)

#### [Q] 请介绍一下NDK 什么是NDK库? JNI 用过吗？
1. A1: [NDK 入门指南](https://developer.android.com/ndk/guides)

#### [Q] 如何JNI中注册native函数，有几种注册方式?
1. A1: [Andoid NDK编程 1 － 注册native函数](http://zhixinliu.com/2015/07/01/2015-07-01-jni-register/)
2. A2: [JNI两种注册过程实战](https://blog.csdn.net/XSF50717/article/details/54693802)

#### [Q] Java如何调用c、c++语言？
1. A1: [怎么实现Java调用C++代码？](https://www.zhihu.com/question/36666057)
#### [Q] JNI如何调用java层代码？
1. A1: [[JNI]开发之旅（7）JNI函数中调用java对象的方法](https://blog.csdn.net/honjane/article/details/53958166)

#### [Q] 对Dalvik、ART虚拟机有什么了解？Art和Dalvik对比
1. A1: [Android Runtime (ART) 和 Dalvik](https://source.android.google.cn/devices/tech/dalvik)
2. A2: [art和dalvik的区别？](https://www.zhihu.com/question/29406156)

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

#### [Q] Android ART上GC算法
1. A1: [Android GC 从dalvik到ART的改进分析](https://cruise1008.github.io/2016/03/30/Android-GC-%E4%BB%8Edalvik%E5%88%B0ART%E7%9A%84%E6%94%B9%E8%BF%9B%E5%88%86%E6%9E%90/)
2. A2: [Android GC原理探究](https://zhuanlan.zhihu.com/p/24835977)
3. A3: [Android-浅析-GC-基础原理](https://jasonzhong.github.io/2017/09/28/Android-%E6%B5%85%E6%9E%90-GC-%E5%9F%BA%E7%A1%80%E5%8E%9F%E7%90%86/)

#### [Q] 如何监控应用性能
1. A1: [Android Choreographer 源码分析](https://www.jianshu.com/p/996bca12eb1d)
2. A2: [Android 基于 Choreographer 的渲染机制详解](https://www.androidperformance.com/2019/10/22/Android-Choreographer/)

#### [Q] RenderScript有无使用过
1. A1: [RenderScript 概览](https://developer.android.com/guide/topics/renderscript/compute)