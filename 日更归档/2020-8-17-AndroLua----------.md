---
layout:     post
title:      AndroLua
subtitle:   写出你的App！
date:       2020-8-17
author:     AGZX
header-img: 
catalog: true
tags:
    - n.
---



## AndroLua

故名瞅瞅，前半部分是Android，后半部分是Lua，前半部分的安卓应该您知道，后半部分的Lua→

Lua 是一种轻量小巧的脚本语言，用标准C语言编写并以源代码形式开放， 其设计目的是为了嵌入应用程序中，从而为应用程序提供灵活的扩展和定制功能。

Lua 是巴西里约热内卢天主教大学（Pontifical Catholic University of Rio de Janeiro）里的一个研究小组，由Roberto Ierusalimschy、Waldemar Celes 和 Luiz Henrique de Figueiredo所组成并于1993年开发。

感谢@Penguin_A

so，在安卓系统上的脚本语言，就可以理解为↓

AndroLua+阔以在安卓平台上的用 Lua 开发安卓程序，不仅支持调用Java[API](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247484751&idx=2&sn=57b508091df008626e97701e20823d15&scene=21#wechat_redirect)（也就是可以在咱手机上用Java写应用）

而且支持编写安卓界面程序，还可以将自己写的 Lua 程序打包成apk安装文件安装。

Lua 语言的简单使没有任何编程经验的用户也能在短时间内开发出安卓程序，因此，在学习AndroLua+之前我们需要先学习 Lua 语言（不过之后聊软件开发的时候其实只用掌握一丢丢就行）

看了很多酷安大佬的程序，很大一部分都是用Androlua开发的，包括之后咱聊到的把个人网站做成一个APP，也就需要用这种语言

AndroLua+

介是Github上一个[开源](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247483869&idx=2&sn=942ca99c2926af50fd37ce5049c954fd&scene=21#wechat_redirect)项目，该版本只支持运行简单的lua代码。国内网友nirenr等，将它在原来的基础上进行改进，不仅支持创建安卓窗口程序，而且将它的运行速度翻了几翻，并集成了常用模块import,http,bson,xml,socket,zlib等等，使调用更加方便。

并且呢，，，最新的Androlua有支持高亮和关键字提示的文本编辑器（可以区分出不同元素的颜色，有点类似之后聊的IDEA Intellij），更值得高兴的是Androlua还支持将lua程序打包成apk。Androlua自带有帮助文档，可以使使用者快速上手。Androlua软件已更名为Androlua+，最新软件的版本为3.4.2，并衍生出许多版本，Androlua+可以在各大应用市场下载的说

