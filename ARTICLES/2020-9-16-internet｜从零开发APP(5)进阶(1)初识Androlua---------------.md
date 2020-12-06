---
layout:     post
title:      internet｜从零开发APP(5)进阶(1)初识Androlua
subtitle:   
date:       2020-9-16
author:     廉一鸣
header-img: 
catalog: true
tags:
    - 从零开发APP

---

## internet｜从零开发APP(5)进阶(1)初识Androlua

你好呀，前几天聊到了，用fusionAPP来简单把一个网页组装成一个应用

But

这貌似跟自己开发APP一点关系都没有，，，，

所以进阶篇就来聊一聊用[androlua](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247484791&idx=3&sn=60b4a45d56f88dbee6e04301289a72a9&scene=21#wechat_redirect)+fusionapp来真正开发应用吧

------

我们前几天在聊组装网页应用的时候，好像忽略了首页下方的几个选项

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMqoHzhpxqrjZmHnzehkSVpNzgDW8yviaj5xdVyqFNV54J3P3ZG86wkVWoZ5sCTnHNFBxw1wqJQaAg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
首先先看网页控制

点一下会发现是这个

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMqoHzhpxqrjZmHnzehkSVpMZhrXZyPEvw8OZ5eOvFbEHFmMvYDTwohYkiaTtAfkuOnyrfwpnic1WJw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
也就是可以理解为在对应[网站添加对应的脚本](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247484306&idx=1&sn=5a76bc655dbf817d6c04146eaa26c0ed&scene=21#wechat_redirect)

删除元素

跟原来咱聊到的去广告原理一样，都是执行一个js脚本来去公告

也可以选择当浏览到一个网页的时候执行[Javascript](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247484288&idx=2&sn=56321e910ebb95ae84b6ec3151bf8726&scene=21#wechat_redirect)

来达到各种各样骚操作(比如说换字体和去广告或者破解视频VIP等等)(具体要找好用的js脚本，还是可以去[油猴](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247484248&idx=2&sn=18e4e9a3bf8cf88f279d736269945b88&scene=21#wechat_redirect)上去找)

and可以添加多个网页

------

然后就是子页面

聊初级玩法的时候可能有疑惑，万一要浏览多个网页呢，一个应用只能看一个网页，是不是太low了，所以就有了子页面功能

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)
点加号后后会跳出来跟创建工程时一样的界面，创建之后会发现能调的参数也完全一样(除了不可以子页面里创建子页面)，所以就可以和之前聊到的一样，在工程里嵌套子页面，再通过顶栏和侧边栏的点击事件，就可以用一个应用浏览所有常用的网站

------

自定义事件

也就是要用androlua语法，写出自定义事件发生时会执行的程序，比如说第1次使用应用弹出隐私协议

全局js，也就是不再单独针对网页，然后在这个应用里打开的网页，都会被执行一遍介个js

------

拜拜