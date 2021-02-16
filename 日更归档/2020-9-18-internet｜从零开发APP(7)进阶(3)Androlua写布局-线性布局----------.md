---
layout:     post
title:      internet｜从零开发APP(7)进阶(3)Androlua写布局-线性布局
subtitle:   
date:       2020-9-18
author:     廉一鸣
header-img: 
catalog: true
tags:
    - 从零开发APP

---

## internet｜从零开发APP(7)进阶(3)Androlua写布局-线性布局

你好呀，今天接着昨天的聊一聊，通过线性布局来写APP的界面布局叭

今天要用到的布局是线性布局，[前情提要](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247485122&idx=2&sn=a3de67c8c2ae0f9d9c94b589fb866bcd&scene=21#wechat_redirect)

------

首先还是在fusionAPP里创建一个空白的工程

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoP0sA0baM80vpwA1Ie5SwbnaX31YfkziaibpbgriajbsKa1GSCLlPRjq4OmVIF63h8Y8HydbY8gpcUbA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
然后点进去工程页面，找到自定义事件

点进去程序启动

在代码行里输入

layout={

 LinearLayout,

 layout_width="fill",

 layout_height="fill",

 orientation="vertical",

 backgroundColor="#FF464C6F",

}

activity.setContentView(loadlayout(layout))

点击运行

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)
会发现整个屏幕都是紫色

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)
下面来具体解释一下

整个代码部分会发现有两部分组成

一个是

layout={

 ，，，，，

}

然后还有底下的这个

activity.setContentView(loadlayout(layout))

首先是上面的

开始的layout=，就相当于是给{ }里的内容取了个名字，所以这个名字也可以自定义，比如

lua={



 ，，，，，



}

中间的逗号就是布局的具体内容

 LinearLayout,



 layout_width="fill",



 layout_height="fill",



 orientation="vertical",



 backgroundColor="#FF464C6F",

开始的linearlayout，是声明这个布局是线性布局

然后剩下的就是线性布局的一些属性(比如说布局的长度宽度和背景)，会在每天的第二更一个一个聊

然后就是activity.setContentView(loadlayout(layout))

会发现在load layout后有个(layout)，这就是刚刚我们给那一段布局起的名字

具体来说就是输入这段代码后，系统才会判定，叫这个名字的布局会被显示

如果取掉这一段代码，运行之后就会发现是完全空白。

------

