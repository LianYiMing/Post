---
layout:     post
title:      internet｜app｜open2share
subtitle:   SendAnywhere
date:       2020-8-22
author:     AGZX
header-img: 
catalog: true
tags:
    - internet
    - app
---

## internet｜app｜open2share

你好鸭，今天接着聊个app

众所周知，如果在某个应用内分享的话，是需要开发者跟这个应用进行协调，把分享的[API](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247484751&idx=2&sn=57b508091df008626e97701e20823d15&scene=21#wechat_redirect)给这个应用才可以，

But如果直接调用用系统分享的[API](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247484751&idx=2&sn=57b508091df008626e97701e20823d15&scene=21#wechat_redirect)的话，是每个应用都可以调用的，就不用再单独协商，所以这也就造成了很多应用内的分享范围太少，而系统分享界面，却有非常多的分享按钮，比如↓

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMogianu3uE56uepRpyB0EMZF9F85fh32bbJWVxDcmEwGvxMWCuVg5uGh6u0vIFkwJNPU3NxkLBUKg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMogianu3uE56uepRpyB0EMZEZ8k9b45Zulc3yic3iaZfXZm7N5icC5icCib3YaSdAR5ePGwbHABxuKAkRA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
上图是QQ浏览器里的，下图是系统的分享界面，差了好像不止一个数量级，，，，，，（尤其是QQ和微信，文件想要分享到其他APP内很麻烦，官方留的接口太少）

所以，有时候想要分享到某个应用时，官方不给接口（也就是API），就可以来调用系统的分享接口来达到目的，今天聊的介个APP就是起到了这个作用

官方介绍↓

这是一款可以将打开交件（open， ACTION_vew）转换为分享文件（share

 ACTIONe）的小工具

本软件已开源 : https: //github.com/linesoft2/open2share用于解决某些App因为一己之私而不提供分享文件功能导致的各种不便（如某讯的两大

社交App）。

使用方法:在打开文件时选择“转换为分享文件，然后再进行分享操作即可。

------

**使用**

First，下载

http://dl-cdn.coolapkmarket.com/down/apk_upload/2020/0713/app-release-254363-o_1ed1ul6p5ec11h81c891hf71usdr-uid-849989.apk?_upt=b20d28d21598073258

Then，不用打开它，比如说在微信打开文件的时候


![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMogianu3uE56uepRpyB0EMZHDgyp5JLyJQPj6ILxNXMoB3ofKbrRDBibENwke6gLRgcTs7gfdMiaibsw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
找到这个

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMogianu3uE56uepRpyB0EMZcnweTOJTueU4ic7Rwj3NlP95xK8hJHU6WibMtqx2bNibPNyyusW6oh4mA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
就可以分享到系统分享界面的选项了




