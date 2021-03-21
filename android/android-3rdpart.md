---
description: 此章节主要为Android 三方库相关
---

# Android 三方库

### TL;DR

Android常用三方库

### 清单

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

#### [Q] OkHttp缓存机制
1. A1: [OKHttp全解析系列（五） --OKHttp的缓存机制](https://www.jianshu.com/p/fb81207af121)

#### [Q] OkHttp连接池结构
1. A1: 

#### [Q] LruCache数据结构和自定义实现
1. A1:

#### [Q] (Glide)BitmapPool结构以及复用原理
1. A1: BitmapPool指的[com.bumptech.glide.load.engine.bitmap_recycle.BitmapPool](https://github.com/bumptech/glide/blob/master/library/src/main/java/com/bumptech/glide/load/engine/bitmap_recycle/BitmapPool.java),具体实现实现为：LruBitmapPool。
2. A2: BitmapPool定义如下接口

| 接口              | 描述                               | 备注             |
| ----------------- | ---------------------------------- | ---------------- |
| getMaxSize        | 获取池子最大内存                   | Byte为单位       |
| setSizeMultiplier | 设置调整乘数                       | 取值范围0-1      |
| put               | 回收缓存                           | “可回收”对象     |
| get               | 从缓存中获取指定尺寸的对象并做清零 | 若获取不到就创建 |
| getDirty          | 从缓存中直接获取指定尺寸对象       | 若获取不到就创建 |
| clearMemory       | 清理所有缓存                       | ---              |
| tirmMemory        | 根据回收等级 清理内存              | ---              |

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
