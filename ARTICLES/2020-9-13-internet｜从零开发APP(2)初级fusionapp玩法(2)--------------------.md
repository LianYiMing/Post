---
layout:     post
title:      internet｜从零开发APP(2)初级fusionapp玩法(2)
subtitle:   
date:       2020-9-13
author:     廉一鸣
header-img: 
catalog: true
tags:
    - 从零开发APP

---

## internet｜从零开发APP(2)初级fusionapp玩法(2)

今天[继续聊](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247485073&idx=1&sn=f30729e1078dff14b69b4e5e6ae3e7d2&scene=21#wechat_redirect)叭

昨天聊到了fusionAPP制作应用时的基本配置，今天就来实操整一个吧

------

首先还是打开昨天创建的那个工程

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMflicbhmUE5G0Aw97YlECwq6NW3Rmm4Qp3yKibAWrjmiatWQNka2siaZ6GL9d65Kr65cS3wSYkXqxDew/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
在底下找到浏览器配置→启动网页，填入想要转成应用的网址→右上角运行一下，看看是不是打开了这个网页

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMflicbhmUE5G0Aw97YlECwqXj8e0Sfm2cNFCcluoyt2UbiaiaEoePQia6VGk0DnE0RoTAXHe2cGWxUfg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
如果能正常显示的话，就点右上角的三个点→打包安装

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMflicbhmUE5G0Aw97YlECwqErYo3IB7ffCdh7aicQrc37Of7byQ5lEsmtoO7z9Of61qJLR71VV5zEQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
点击安装应用，把应用安装，之后在桌面点开这个图标，就会发现是这个网页了

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMflicbhmUE5G0Aw97YlECwq3P8ZJ5o2KRcPD3gj8JPAuNLIdDCODTsnbkt7U8ia9YAeVWg9wjsM9Vg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

------

作者还留了很多美化的参数可以调↓

还是第1张图片

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMflicbhmUE5G0Aw97YlECwq6NW3Rmm4Qp3yKibAWrjmiatWQNka2siaZ6GL9d65Kr65cS3wSYkXqxDew/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
1.版本号

版本号可以不用调，因为同一版本是可以直接覆盖安装的，但是如果已经调过了之后，那么下一次安装的版本要么得跟他一样，要么就要比他高，这是安卓系统的一个机制，不让降级安装

2.横屏顾名思义，这个网址是横屏打开的

3.启动图也就是点开应用时会白屏两秒，应用启动图来之后就可以自定义，

此时显示的图片是啥

4.显示状态栏，如果取消勾选的话，进入应用后不会显示时间和电量内一栏

5.浏览器标识

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)
也就是UA，是专门让网页判断访问者是手机还是电脑的，因为手机跟电脑看到的页面是不一样的(比如说长宽比，有些功能还会有区别，比如说印象笔记网页版只有PC的)，有时候需要用到电脑的ua，那么ua标识就选择PC

6.外部应用和进度顾名思义

7.长按菜单如图

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)
可以对网页中的元素进行弹出菜单，进而实现屏蔽网页中的广告

8.网页沉静也就是顶栏随着网页颜色的变化而变化，如图

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMflicbhmUE5G0Aw97YlECwqI8VbEZ4N8p016I2md0RC4gw65NicF4RsmyDnpssvyfXRoah81WIP6Yg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
打开了之后刚刚深蓝色的顶栏，随着网页变成了白色自己也变成白色了