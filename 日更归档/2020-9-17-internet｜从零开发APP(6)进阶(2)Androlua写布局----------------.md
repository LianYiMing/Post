---
layout:     post
title:      internet｜从零开发APP(6)进阶(2)Androlua写布局
subtitle:   
date:       2020-9-17
author:     廉一鸣
header-img: 
catalog: true
tags:
    - 从零开发APP

---

## internet｜从零开发APP(6)进阶(2)Androlua写布局

你好呀，今天接着聊一聊，用fusionAPP来开发出一个应用来

在原来聊到的创建工程中，如果选择了空白模板的话，会发现安装后整个就是一空白，这些空白就是留给我们写布局的地方

------

首先先创建一个空白的页面

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMxK1u1JlvShWYYWicWgib2gaS0oeLp9BPa77vEYUHKO5aLglrNSGV2m2EyD33KY4N9R7efIhRaOMXQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
在自定义事件里边找到程序启动，当然除了最后收到新标题，剩下三个都可以

点进去后发现会有地方让我们输入代码
![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMxK1u1JlvShWYYWicWgib2gaU0RdMZolqCiaW5KhA05J5U5iaNYkliaPQz3AaZv0xqXlH3IGbf11na36A/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMxK1u1JlvShWYYWicWgib2gadj1wUqzxdywofmvRx7cU78BenpEEh4p1jR8FQyZnxicOYiaHXacrKicWw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
这时候就要用到几个基本的布局语法了:(by寒歌 有可能会看不懂，不过无所谓之后慢慢解释，平常开发主要就是用到线性布局就够了)

--Android中常用的5大布局方式有以下几种：

--线性布局（LinearLayout）：按照垂直或者水平方向布局的组件。

--帧布局（FrameLayout）：组件从屏幕左上方布局组件。

--表格布局（TableLayout）：按照行列方式布局组件。

--相对布局（RelativeLayout）：相对其它组件的布局方式。

--绝对布局（AbsoluteLayout）：按照绝对坐标来布局组件。

------

比如说这是一个线性布局

LinearLayout,

   background="#66463085";

   layout_width="fill",

   layout_height="fill",

   Gravity="center",

   id="DialogExternal",

------

明天聊聊实操叭