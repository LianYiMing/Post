---
layout:     post
title:      internet｜存储重定向（2）初识
subtitle:   完美到重定向！
date:       2020-9-3
author:     AGZX
header-img: 
catalog: true
tags:
    - 存储重定向

---

## internet｜存储重定向（2）初识


你好吖～

昨天聊到了，通过存储重定向可以根治[毒瘤APP的滥用存储](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247484963&idx=1&sn=198845dad7f6e0e4dc87007c725aa6ae&scene=21#wechat_redirect)，今天就来介绍一下什么是存储重定向叭

------

顾名思义



存储重定向，也就是重新来给存储找方向，就是用来解决这个问题→

把有用的文件夹目录全部定向一个文件夹里，把没有用的文件定向到缓存分区（不是用户能看到的存储分区，缓存分区正常情况下用户是看不到的）里，再配合之后聊到的一个可以定时清理的清理应用来定期清理没有用的文件，整个手机的存储目录就会整洁如新，找文件效率极大提升

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoM3pSVhlEfI5vtkF8kEydcWgOpqn3iaEbZicggZDVXETLwuMwicQTXaGsUFm59po8diaJs0nRibfmfCCOA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



**主要的运作原理就是→**类似于原来电脑的沙箱，把选了存储空间隔离的应用放到一个独立的空间里，这个应用往我们手机里放的任何文件都不会在我们的sdcard（也就是平常使用时候放东西的目录）看到

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoM3pSVhlEfI5vtkF8kEydcWIu5SAKciaGgEqI7YupjmAnKR15tVmqpauy59ib9kda0ic7lezxH2LHnFw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
而会是在这个小空间里，小空间又可以设置让它隶属于data分区（也就是应用数据分区）或者是缓存分区（也就是用系统清理默认清掉的缓存放的地方，一般存在我们可以看到的存储空间的Android文件夹里），那问题就来了，那这些应用我就读取不到其他手机上的文件了嘛，，，

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoM3pSVhlEfI5vtkF8kEydcW9liaVc4DoPkXucLYcKlLOekcrrAEdNqHFBktlx9U0xNZYR4Pz9UCMXw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

So

会有功能可以把文件导入与导出，也就是可以让这个应用访问到这个小空间以外的文件，并且把一些文件再导出到sdcard里，路径也可以自己定义，所以也就可以达到手机里只有几个大文件夹的方便局面

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMiao1iaP56V1aNxN54Xt2IvqvWkUy0sLJ5FMF3PrcezAa0zqHAxdqibvbAlrPRl7pWftlYKT9Bmg9sg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



