---
layout:     post
title:      internet｜app｜远程控制（1）
subtitle:   用手机玩电脑
date:       2020-9-1
author:     AGZX
header-img: 
catalog: true
tags:
    - app
    - 远程控制

---

## internet｜app｜远程控制（1）

你好吖，搭建网站聊的差不多了，这几天大家聊一聊远程电脑叭，经过这几天的文章，我们就可以：

1. 远程开机自己的电脑
2. 并且可以用手机方便地控制

随时随地只要手机能连上网就可以

------

今天先来聊一个很重要的APP→teamviewer

用它主要就是用手机来远程控制电脑（Linux MACos windos都可以，都有对应的版本）

------

首先先下载teamviewer（电脑和手机上都下载）

https://www.teamviewer.cn/cn/

之后在电脑上打开teamviewer的setup.exe（也就是安装文件），之后选择用免费版，选择商业用途了也可以删了重新安装（商业用途要付费）

安装好了之后会发现

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMZFtSakPK905xhkKsc1zFm76ibicSakXHyDAEoMibqocFTwQHKfNicGwcLIuwvzkSUSKZdPr9lpe81yA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
这时候在手机上打开客户端（先注册登陆），输入电脑上允许远程控制的“您的ID”，并且再把密码输进去，会发现

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoMZFtSakPK905xhkKsc1zFm0ib5s7oofZzwD99CriavaicucDsKXEKfXWibQoz26KSAoB5059icrOHI2ZQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
盗的图，，，，

手机就能看到电脑的屏幕了，这时候动一动手机屏幕鼠标应该也会跟着动（不过杀毒软件这时候应该就会报警了，允许程序的操作就可以），手机点一下屏幕，光标也会跟着点一下，这样就成功的通过手机来控制电脑了

（并且不需要连接同一个WiFi，只是手机版貌似需要注册，注册就行）

如果我们能让电脑可以远程开机，并且能让team viewer开机自启动，那么就可以即使不在电脑旁边也能唤醒他，并且远程控制了

这就是之后咱要聊的东东

