---
layout:     post
title:      internet｜捷径｜安卓RAM管理机制
subtitle:   
date:       2020-7-19
author:     廉一鸣
header-img: 
catalog: true
tags:
    - 捷径

---

## internet｜捷径｜安卓RAM管理机制

他就看到这一次的文章的脸，肯定发现还是没找到模板的备份……，木的事，不打紧这次咱聊安卓的内存管理机制。

------

***前言：\***

注册周志手机分运行内存和存储内存，软件或者系统运行都需要占用运行内存，所以不同的操作系统也有不同的分配方式，咱这次讲的就是安卓系统关于运行内存的分配***
\***

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMqB6tso2hv0slvMC8iaX1Tu6YvTzytSKs6DlJHlgstXJGAS7lzb9AGEMY1EbdPepfQ20G823eACUA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



------

***特点：\***

Android沿用了Linux（一种很奈斯的操作系统，安卓可以理解为Linux的孩子）的内存管理方案～低内存回收机制～也就是不开应用，也会占内存（ram），在空载状态下（啥也不开），Android P（安卓9，10是Q）占用下限约为500mb(大概，我测试可以正常运行)，上限为设备物理内存的1/2，即开机占用一半内存（并且多任务界面的剩余内存显示是骗人的，真的呢，不信各大内参论坛搜搜🤣）

so安卓应用不存在关闭一说，退出之后仍然会留在内存中。直至剩余内存过低，才会由系统机制将其杀掉，回收它占用的那部分内存

这就是安卓内存管理机制（windos是开多少就占多少，不会像安卓一样满）

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)推荐大家试试，挺好用的🥰

app进程的分类（部分搬运）

Android进程种类

\1. 前台进程（foreground）

目前正在屏幕上显示的进程和一些系统进程。举例来说，Dialer，Storage，Google Search等系统进程就是前台进程；再举例来说，当你运行一个程序，如浏览器，当浏览器界面在前台显示时，浏览器属于前台进程（foreground），但一旦你按home（也就是最初的，有按键的手机的小房子）回到主界面，浏览器就变成了后台程序（background）。我们最不希望终止的进程就是前台进程。

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMqB6tso2hv0slvMC8iaX1TuWgE9FdpBhbWkDyicPZmnYnKOKngI3MIgBUNAckYvLr57hVV87VuXBFw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
是吧你知道这是啥

\2. 可见进程（visible）

可见进程是一些不再前台，但用户依然可见的进程，举个例来说：widget、输入法等，都属于visible。这部分进程虽然不在前台，但与我们的使用也密切相关，我们也不希望它们被终止（你肯定不希望时钟、天气，新闻等widget被终止，那它们将无法同步，你也不希望输入法被终止，否则你每次输入时都需要重新启动输入法（并且把MIUI优化关了之后，每次重启都需要再启动一遍输入法不知道为啥））

![img](https://mmbiz.qpic.cn/mmbiz_gif/tMsLbdfwxoMqB6tso2hv0slvMC8iaX1TuibIX6vOIa6uKCCn4FicEKgkSbNrxhodpNzORHpNsDZmE1NiaQ9wiaXzYew/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

\3. 桌面进程（home app）

即launcher，保证在多任务切换之后，可以快速返回到home界面而不需重新加载launcher

![img](https://mmbiz.qpic.cn/mmbiz_gif/tMsLbdfwxoMqB6tso2hv0slvMC8iaX1TuRqRRibmXhXsxhMuKx4UPvic9CEvAz7ibJzmUYib1R2ZRDK7cbeiczicLFj8w/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

\4. 次要服务（secondary server）

目前正在运行的一些服务（主要服务，如拨号等，是不可能被进程管理终止的，故这里只谈次要服务），举例来说：谷歌企业套件，Gmail内部存储，联系人内部存储等。这部分服务虽然属于次要服务，但很一些系统功能依然息息相关，我们时常需要用到它们，所以也不太希望他们被终止

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)

可带劲了

\5. 后台进程（hidden）

即是后台进程（background），就是我们通常意义上理解的启动后被切换到后台的进程，如浏览器，阅读器等。当程序显示在屏幕上时，他所运行的进程即为前台进程（foreground），一旦我们按home返回主界面（注意是按home，不是按back（也就是退出键，直接按退出键退出，貌似有些app可以杀后台）），程序就驻留在后台，成为后台进程（background）。后台进程的管理策略有多种：有较为积极的方式，一旦程序到达后台立即终止，这种方式会提高（其他）程序的运行速度，但无法加速程序的再次启动（比如说在微信运行的时候突然强行关闭，第2次打开就会卡两秒，或者开发者设置里边限制一个应用不让在后台运行也会这样）；也有较消极的方式，尽可能多的保留后台程序，虽然可能会影响到单个程序的运行速度，但在再次启动已启动的程序时，速度会有所提升。（比如绿色守护的普通休眠，就比默认启动的快）这里就需要用户根据自己的使用习惯找到一个平衡点

![img](https://mmbiz.qpic.cn/mmbiz_gif/tMsLbdfwxoMqB6tso2hv0slvMC8iaX1Tuo2ltMLvnfGU2DiavahD6bhsIeHPeBkUo1nC0SqRcPgk9Vbs6l7VDNlw/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

老坛酸菜牛肉面

\6. 内容供应节点（content provider）

没有程序实体，进提供内容供别的程序去用的，比如日历供应节点，邮件供应节点等。在终止进程时，这类程序应该有较高的优先权

![img](https://mmbiz.qpic.cn/mmbiz_gif/tMsLbdfwxoMqB6tso2hv0slvMC8iaX1TuqZImD9dqKiceZflQHiaB2VBfLibNn8TX6ByQB3CDqA1AGJBu3b5WG30QA/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)



\7. 空进程（empty）

没有任何东西在内运行的进程，有些程序，比如BTE，在程序退出后，依然会在进程中驻留一个空进程，这个进程里没有任何数据在运行，作用往往是提高该程序下次的启动速度或者记录程序的一些历史信息。这部分进程无疑是应该最先终止的。

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)
emmm明天继续（哈哈哈哈哈哈这几张刚刷到xswl🤣）

