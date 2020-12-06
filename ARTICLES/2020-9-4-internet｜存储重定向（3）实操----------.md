---
layout:     post
title:      internet｜存储重定向（3）实操
subtitle:   
date:       2020-9-4
author:     AGZX
header-img: 
catalog: true
tags:
    - 存储重定向

---

## internet｜存储重定向（3）实操

你好呀，今天聊一聊怎么样实施存储重定向叭

[前情提要](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247484971&idx=1&sn=070de28960c1b1c1ab0ab58ff4f833d4&scene=21#wechat_redirect)

昨天聊到了，存储重定向是要通过一个APP来实现，所以第1步就是下载，，，，，

https://www.coolapk.com/apk/moe.shizuku.redirectstorage

下载完了之后点开，会提示要给root权限和刷入模块，模块这里指的是magisk，关于如何root和刷入magisk详情参见[之前聊的](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247483687&idx=1&sn=729f4830cc5e41e9c1227bf4d76ab961&scene=21#wechat_redirect)，root完并且把magisk模块给刷上了，重启完就会看到这个

ps→增强模式就需要刷模块，如果普通模式直接给root权限就可以

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoPh2vNpoX0gSZ04R9VenN7ApUichRESJGOQGZvtnXQPIGqNDF0ZhIPzicVtrzQqDbuPMMGxicSuAtHyQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
点击应用管理

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoPh2vNpoX0gSZ04R9VenN7AKjkgEx6o2hYh9r6RUGUJibOuhVhOicaEsO35ZmFibdtKOiamkeg8Vkt1MA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
找到想要存储空间隔离的应用，点进去

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoPh2vNpoX0gSZ04R9VenN7AKrmRS6Gny6eTJgTp5Hc9hGuErTATebyberry3niaPwiaTPuUP6kcM9zg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
点击启动，就成功对他起用了存储空间隔离，如果这时候不弄其他选项的话，这个应用是没有办法访问到你手机上的文件的，并且他创建的文件我们也看不到，所以遇到那种没什么重要文件但垃圾一堆的应用就可以只开这一个按钮，就让他自生自灭去😂，反正再怎么创建文件夹也不会波及到正常的目录

------

如果遇到比如说QQ这一类需要读取一些目录的文件，比如说聊天时候发照片，之类的应用，就需要动底下的一些设置，首先先看基础设置的第2个，也就是可访问的文件夹

拿QQ举个栗子

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoPh2vNpoX0gSZ04R9VenN7AlDHxr6HgAVmRiaSA0l0fL9eiale72ctbDiaiaZsbxQiczdSSyeouiawY3ElA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
共享文件夹→是他可以访问也可以读写的，也就是说，如果在这里边把三个都勾选，那么在QQ里就可以给别人发这三个目录里的照片（如果不勾选的话，QQ会读取不到这些照片），并且QQ是可以在这三个文件夹里创建文件的

底下的自定义就可以设置是否让QQ读写到除了上面那三个的其他文件夹，ps：如果勾选了QQ本来放东西的文件夹Tencent，就会跟没用存储空间一样呢，，，，，

底下的其他应用的文件夹指的是可以让QQ读取到被隔离存储空间的应用创建的文件（也可以读取到没有被隔离的，只不过既然要存储空间隔离，就来个彻底（也就是整个手机只剩下四五个文件夹），完全分类好了之后就不需要用到这一个功能辣）

------

这是第1步，如果整完了第1步，被隔离的应用就不会再创建我们可以看得见的文件了，这时候把存储空间里这些应用的垃圾文件都删一删，会发现再怎么用手机的存储永远是删完之后的样子，很整洁了呢，但是如果这些被隔离的应用也有重要的文件（比如说QQ下载的文件，给QQ开启存储隔离之后下载的就找不到了），就需要用到第2步的文件导出

明天聊聊叭

