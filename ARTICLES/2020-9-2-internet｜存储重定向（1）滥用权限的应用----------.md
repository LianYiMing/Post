---
layout:     post
title:      internet｜存储重定向（1）滥用权限的应用
subtitle:   垃圾APP的噩梦
date:       2020-9-2
author:     AGZX
header-img: 
catalog: true
tags:
    - i储重定向


---

## internet｜存储重定向（1）滥用权限的应用

原你好吖，今天聊一聊存储重定向吧

众所周知，Android 应用的数据主要储存在两个地方，应用私有文件夹和内置存储空间：前者在一般情况下不需要用户去干涉（也就是在之前聊到的data分区），后者则是你一打开文件管理器就所在的目录，任何拥有存储权限的应用都可以在此随意读写文件。

手机里的存储目录。只要给了一个应用读取设备的文件的权限，国产的垃圾应用基本都会滥用存储空间，存储一些日志之类的，对用户没有任何帮助的东西（美其名曰是加快速度的缓存，但是理论上这些缓存之类的东西应该存在手机专门划给缓存的分区，而不应该放在用户使用的存储空间）

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMiao1iaP56V1aNxN54Xt2IvqpY7Xjwl6ShYIpgeEFL92IWR3QQNibNxnstIMiaJcVKd6NsqprRsMjA5A/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
以至于在手机上找个文件都很恶心

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMiao1iaP56V1aNxN54Xt2IvqticTD536NFRTV4ibFYBvlZvoqb9rNJvXQLSktUldPZFjUcXicSQn2jfiaQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
理论上说在应用里我们保存的一些东东应该被放在

Movies （影片）

Music （音乐）

Documents （文档）

Download (下载的文件）

DCIM 或者Picture（图片）

手机备份的时候，直接把这几个文件夹复制到电脑就OK了

But

基本上所有的国产应用都会在新建一个专门放在这个应用里保存的东西的一个文件夹，并且再放上很多无关紧要的东西，在一些应用中保存下来的音乐、图片或下载的文档，很有可能会被应用擅作主张藏在相当深的路径里。这就让平时微信和QQ找文件发文件，或者备份的时候非常麻烦。同时完全的读写权限也让部分隐私敏感的用户担心个人隐私问题，个人文件和敏感信息处于「任君采撷」的状态。

**存储重定向就能完美解决这个问题**

------

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMiao1iaP56V1aNxN54Xt2IvqvWkUy0sLJ5FMF3PrcezAa0zqHAxdqibvbAlrPRl7pWftlYKT9Bmg9sg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



