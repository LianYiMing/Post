---
layout:     post
title:    internet｜从零开发APP(1)初识fusionapp  
subtitle:   
date:       2020-9-11
author:     AGZX
header-img: 
catalog: true
tags:
    - 从零开发APP

---

## internet｜从零开发APP(1)初识fusionapp

你好鸭，从今天开始，咱们来聊一聊怎么样从0开发一款APP叭

------

今天先来聊一个貌似跟这个没什么关系的应用→fusionapp

(⊙o⊙)啥？

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoP6vucSMiah4lzaRHqyM8MWnA7ns5Sag5hOYib860c1pjoWHB6wmYA7oTLMvU47LRicMy5bpaseYicdow/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



其实介是个网页转应用的APP，在里面输入网址，它会自动打包成APP来安装，打开这个应用就会看到输入的网页了，但它兼容[lua](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247484791&idx=3&sn=60b4a45d56f88dbee6e04301289a72a9&scene=21#wechat_redirect)的语法，所以就可以在这上边用Lua写应用，最后再用他的打包功能来安装

今天就来先熟悉一下fusion叭，，，，，

------

first，下载

https://www.coolapk.com/apk/cn.coldsong.fusionapp

second基本功能:

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoP6vucSMiah4lzaRHqyM8MWnUY4esUz5BlCYK6a8QXz1ia4oG68Rpibr6qfHoUKOX2faib3dRJ0n69hew/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
应用里内置了很有用的矢量图，这一点在之后用处非常大(不然找矢量图很浪费时间)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoP6vucSMiah4lzaRHqyM8MWnu0KWoT3I4KWbXX6t2SkaBe51xXzSLlp5lj9cVZcWzq6dnqklkD8CKg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
图标制作也就是可以用它的图标制作工具来给你的应用制作图标

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoP6vucSMiah4lzaRHqyM8MWnt3mdzF68yvJDblOmdORUXYWsZXNhOpeO20gyRU4Qib255EJczbE46Mg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
配色之墙，提供了很多很漂亮的配色，开发应用的时候非常实用，直接复制粘贴(复制粘贴实际上就是复制下来颜色对应的代码，至于为什么是代码，那就是之后要聊的了呢)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoP6vucSMiah4lzaRHqyM8MWn7iajepXyqFj6faSC8JtHCHZXCU95drU1FDgf1Ticx6uNUAfciaMx75C8g/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
剩下的都顾名思义，明天继续聊一聊怎么样把网页转成应用叭