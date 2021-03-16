---
description: 此章节主要为Android view相关知识
---

# Android View 视图

### TL;DR

all about view.

### 清单

#### [Q] 列表卡顿问题怎么优化
1. A1: [Andriod性能优化之列表卡顿——以“简书”APP为例](https://www.jianshu.com/p/336362b23c30)
2. A2: [Android 中的卡顿丢帧原因概述 - 系统篇](https://zhuanlan.zhihu.com/p/82521327)

#### [Q] RecyclerView原理
1. A1: [深入浅出 RecyclerView](https://www.kymjs.com/code/2016/07/10/01/)
2. A2: [RecyclerView缓存原理，有图有真相](https://juejin.im/post/5b79a0b851882542b13d204b)
3. A3: [Android RecyclerView 原理解析](https://www.okcode.net/article/27992)

#### [Q] RecyclerView优化
1. A1: [RecyclerView一些你可能需要知道的优化技术](https://www.jianshu.com/p/1d2213f303fc)

#### [Q] ListView重用的是什么？
1. A1: [ListView复用和优化详解](https://blog.csdn.net/u011692041/article/details/53099584)
2. A2: [Android ListView工作原理完全解析，带你从源码的角度彻底理解](https://blog.csdn.net/guolin_blog/article/details/44996879)

#### [Q] ListView 中图片错位的问题是如何产生的?ListView图片加载错乱的原理和解决方案
1. A1: [Android ListView异步加载图片乱序问题，原因分析及解决方案](https://blog.csdn.net/guolin_blog/article/details/45586553)
2. A2: [listview图片加载错乱的原理和解决方案](https://blog.csdn.net/lilong_19880408/article/details/78160084)

#### [Q] RecyclerView和ListView的性能对比
1. A1: [【腾讯Bugly干货分享】Android ListView 与 RecyclerView 对比浅析—缓存机制](https://zhuanlan.zhihu.com/p/23339185)
2. A2: [我们为什么要使用RecyclerView](http://zjutkz.net/2016/08/10/%E6%88%91%E4%BB%AC%E4%B8%BA%E4%BB%80%E4%B9%88%E8%A6%81%E4%BD%BF%E7%94%A8RecyclerView/)

#### [Q] ListView的优化
1. A1: [ListView的优化](https://www.jianshu.com/p/f0408a0f0610)

#### [Q] RecycleView优化
1. A1: [RecyclerView 性能优化 | 安卓 offer 收割基](https://blankj.com/2018/09/29/optimize-recycler-view/)
2. A2: [看完感觉我RecyclerView白学了！](https://www.itcodemonkey.com/article/13649.html)

#### [Q] ViewPager使用细节，如何设置成每次只初始化当前的Fragment，其他的不初始化？
1. A1: [ViewPager懒加载极致优化](https://juejin.im/post/5d37bb8df265da1b8b2ba01a)

#### [Q] 如何优化自定义View
1. A1: [Custom Views and Performance](https://www.kancloud.cn/redzealot2008/android-performance-patterns/345950)
2. A2: [你最需要知道的View优化](https://zhuanlan.zhihu.com/p/28198804)
3. A3: [Android性能优化典范 - 第1季](http://hukai.me/android-performance-patterns/)
4. A4: [正确认识onMeasure方法！](https://mp.weixin.qq.com/s/7FE0a9UI5sB538pA6kxpQA)

#### [Q] 自定义View如何考虑机型适配
1. A1: [自定义View尺寸进行适配](https://www.jianshu.com/p/4100ccacf385)
2. A2: [自定义View如何考虑机型适配](https://blog.csdn.net/github_37130188/article/details/89075837)

#### [Q] 自定义控件原理
1. A1: [【Android】自定义控件之View原理与使用](https://www.jianshu.com/p/a3014f8442b0)

#### [Q] 自定义View如何提供获取View属性的接口？
1. A1: [Android自定义View属性，使用或获取自定义View属性，获取View默认属性](https://blog.csdn.net/ShareUs/article/details/85879789)

#### [Q] 自定义View的事件
1. A1: [@GcsSloop](https://www.gcssloop.com/)大佬的文章[安卓自定义View进阶-事件分发机制详解](https://www.gcssloop.com/customview/dispatch-touchevent-source)

#### [Q] 自定义View注意事项
1. A1: [Android自定义View注意事项](https://www.jianshu.com/p/9862cddca1b3)
2. A2: [自定义视图组件](https://developer.android.com/guide/topics/ui/custom-components?hl=zh-cn)


#### [Q] 请描述一下View事件传递分发机制 Touch事件传递流程
1. A1: [Android事件分发机制](http://gityuan.com/2015/09/19/android-touch/)
2. A2: [Android事件分发机制——从基础深入源码解析](https://www.jianshu.com/p/e6ceb7f767d8)

#### [Q] 封装View的时候怎么知道view的大小
1. A1: [Android 浅谈View的测量measure](https://www.yimipuzi.com/1057.html)

#### [Q] 微信主页面的实现方式
0. A0: 讲个笑话:给我写个APP就照着微信抄一下。
1. A1: [Android:TabLayout+ViewPager+Fragment实现底部导航](https://blog.csdn.net/ruancw/article/details/80494503)

#### [Q] 微信上消息小红点的原理
0. A0: 小红点UI实现很简单，关键在于UI怎么和消息绑定。后面又可以引申出长连接。
1. A1: [简单实现消息提示(小红点)](https://blog.csdn.net/qq_28268507/article/details/70314844)

#### [Q] 计算一个view的嵌套层级
1. A1: [计算一个ViewGroup的嵌套层级](https://blog.csdn.net/zx_android/article/details/79558509)

#### [Q] 点击事件被拦截，但是想传到下面的View，如何操作？
1. A1: [点击事件被拦截，但是想传到下面的View，如何操作](https://blog.csdn.net/github_37130188/article/details/89684468)

#### [Q] 事件分发中的onTouch 和onTouchEvent 有什么区别，又该如何使用？
1. A1: [事件处理之onTouchEvent()和onTouch()方法精炼详解](https://blog.csdn.net/weixin_41101173/article/details/80460632)
2. A2: [android onTouch()与onTouchEvent()的区别](https://blog.csdn.net/guyuealian/article/details/51637033)
3. A3: [事件分发中的onTouch 和onTouchEvent 有什么区别?](https://qqabby.github.io/2019/01/21/事件分发中的onTouch-和onTouchEvent-有什么区别/)

#### [Q] View和ViewGroup分别有哪些事件分发相关的回调方法
1. A1: [View & ViewGroup 之 事件分发](https://blog.csdn.net/crazy1235/article/details/70767884)
2. A2: [View和ViewGroup分别有哪些事件分发相关的回调方法](https://blog.csdn.net/github_37130188/article/details/89112835)



#### [Q] View绘制流程
1. A1: [深入理解Android之View的绘制流程](https://www.jianshu.com/p/060b5f68da79)

#### [Q] 动态布局的理解
1. A1: [Android动态布局的实现](https://blog.csdn.net/sbl19940819/article/details/88891178?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)

#### [Q] Requestlayout，onlayout，onDraw，DrawChild区别与联系
1 A1: [requestLayout()与onLayout()；onDraw()与drawChild()的区别和联系](https://blog.csdn.net/weixin_41101173/article/details/79726311)

#### [Q] invalidate和postInvalidate的区别及使用
1. A1: [invalidate()和postInvalidate() 的区别及使用](https://www.jianshu.com/p/e147f381190c)

#### [Q] Bitmap对象的理解
1. A1: [Android Bitmap理解](https://blog.csdn.net/wangcheng_/article/details/78253953)
2. A2: [彻底理解Bitmap的高效加载策略](https://www.jianshu.com/p/5f02db4a225d)
3. A3: [Android O Bitmap 内存分配](https://www.cnblogs.com/xiaji5572/p/7794083.html)

#### [Q] Bitmap对象占用内存计算
1. A1: [Android坑档案：你的Bitmap究竟占多大内存？](https://zhuanlan.zhihu.com/p/20732309)
2. A2: [Bitmap究竟占多大内存](https://xiongcen.github.io/2017/01/04/AndroidBitmapMemory/)

#### [Q] Bitmap 使用时候注意什么？Bitmap如何处理大图，如一张30M的大图，如何预防OOM
1. A1: [Bitmap 使用时候注意什么？](https://www.jianshu.com/p/fbf5a310788c)

#### [Q] Bitmap的recycle()
1. A1: [Android中有没有必要调用Bitmap的recycle()](https://www.jianshu.com/p/b84b1b5f2fe9)

#### [Q] Fragment如果在Adapter中使用应该如何解耦？
