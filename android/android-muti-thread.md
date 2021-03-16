---
description: 此章节主要为Android多线程相关
---

# Android 多线程

### TL;DR

除去Java多线程外的特异Android线程如Handler

### 清单


### 清单


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

#### [Q] 如何在子线程操作UI
1. A1: [Android只在UI主线程修改UI，是个谎言吗？ 为什么这段代码能完美运行？](https://www.zhihu.com/question/24764972)
2. A2: [Android-在子线程中显示Toast和Dialog](https://blog.csdn.net/u012230055/article/details/54289280)
3. A3: [android 关于子线程更新 UI 的一些事](https://juejin.im/entry/582d5587a0bb9f0067a6f02a)

#### [Q] 为何Handler可以操作UI，Handler线程切换原理
1. A1: [Android消息分发及多线程切换之Handler、Message的细枝末节（二）](https://www.jianshu.com/p/a842b8d815d8)
2. A2: [通过学习Handler源码，手写子线程间的通信](https://mp.weixin.qq.com/s?__biz=MzU3NzQ0MzYxMg==&mid=2247483708&idx=1&sn=e81d8d4e2d920fa783e6ec686937bd38&chksm=fd05c34fca724a59471a26d9f037b6423684f2c2a5a6cc5ef8907712aa67c167fbbb95f92bf4&mpshare=1&scene=1&srcid=&sharer_sharetime=1585648474813&sharer_shareid=faa5430ddf8e3a72161f970023d7de03&key=c967bf038ee4b9073471d47fe0e3a2112403c9db6c3abde3ccab1da023b98e659ee50b048d7a1bdd2054ec6a2923e64c4030fef68e356d7892556383484cc7def9195b428f5bcd4cc94926373ee39229&ascene=1&uin=MTEyNTM1NjEzMg%3D%3D&devicetype=Windows+10&version=62080079&lang=zh_CN&exportkey=A7sKMq1ne1EDaEr9Dl%2BPU%2BE%3D&pass_ticket=0iku%2FkvhX9MVQv2%2BuLZfzJxteUkt0ZTaaOrk980uVza4MYxtH7%2F4MaLhB5Ke6loV)

#### [Q] Handler#postDelay实现原理
1. A1. 源码参考[frameworks/base/core/java/android/os/Handler.java](https://cs.android.com/android/platform/superproject/+/master:frameworks/base/core/java/android/os/Handler.java;drc=master;l=719?q=Handler.java)
2. A2: Runnable最后都会被转为Message对象。
    + #postDelay方法最终转成调用#sendMessageAtTime，Time指的就是当前的时间+Delay的时间。
    + MessageQueue#enqueueMessage方法指定一个唤醒时间。入队时，根据唤醒时间插入相应位置。
    + 在MessageQueue#next方法中，死循环获取下一个Message。
    + 根据最后一个msg计算阻塞等待时间 nextPollTimeoutMillis，直到 nextPollTimeoutMillis唤醒再取Message完成延迟消息。

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

#### [Q] 请解释下在单线程模型中Message、Handler、Message Queue、Looper之间的关系
1. A1: 了解下Handler机制即可[Message、Handler、Message Queue、Looper之间的关系](https://www.jianshu.com/p/352877cd61c1)

#### [Q] ThreadLocal原理，实现及如何保证Local属性？
1. A1: 问题搜索N篇都是这老哥答案。[ThreadLocal原理，实现及如何保证Local属性](https://blog.csdn.net/github_37130188/article/details/89483246)

#### [Q] ThreadLocal的ThreadLocalMap和WeakHashMap对比
1. A1:ThreadLocal由内部的ThreadLocalMap存储。Key为ThreadLocal；Value为保存的值，对比如下


| ---      | ThreadLocalMap | WeakHashMap |
| -------- | -------------- | ----------- |
| 对象持有 | 弱引用         | 弱引用      |

#### [Q] AsyncTask 如何使用?
1. A1: [AsyncTask](https://developer.android.com/reference/android/os/AsyncTask)

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

#### [Q] Android线程有没有上限？
1. A1: [57、Android线程有没有上限](https://blog.csdn.net/FDoubleman/article/details/98599279)

#### [Q] 如果在onStop的时候做了网络请求，onResume的时候怎么恢复？
1. A0: 问题没头没脑，不回答。

#### [Q] Java多线程引发的性能问题，怎么解决？
1. A1: [Android性能优化典范之多线程篇](https://juejin.im/entry/59f82808f265da43346f36fd)

