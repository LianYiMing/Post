---
layout:     post
title:      internet｜免root玩机｜virtual xposed
subtitle:   免root玩机
date:       2020-8-3
author:     AGZX
header-img: 
catalog: true
tags:
    - 免root玩机


---

## internet｜免root玩机｜virtual xposed

今天继续聊免root玩机
![img](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoNr19BkJJ802uHqUwMTCa8sHP2wo5cZWH6lBLJTQBZnlT8FkhbmoBnLhxNP7Jc2KhZHPWvu6XlsAQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)





![img](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoNr19BkJJ802uHqUwMTCa8syC58LVemoq3TEyfkBuSdBrSH5zPKdHuHOtKDK9RuSnoMHMg62ic35jg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



![img](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoM12GmQGZYFy7azn1RM2IznldnbaicFIpNnKejI3fo2HevqRhvWHQ8k8TXI8CgyfSN0qVGbqWJj3Wg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



![img](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoPvhibcLnC5hTcXqKITTp19OH29NLiam9n4fQKickXsBhK690REU4AB7V3lQCIYMvKB7L1fbALqaCoAw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

***森么东东***

![img](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoM12GmQGZYFy7azn1RM2IznibrWgBLOicIoeicsg3LGoSS6wTeO5SJomic3dofibictDVGkkudHjOHZekDA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

就是类似于一个虚拟机的应用，～virtual xposed. 跟太极差不多，是虚拟出来一个系统，但是以应用的方式来运行所以说很占运存，但是怎么修改也不会修改到真系统，所以也不会变砖，也不用刷机子

Ps：也是只能安装XP模块





![img](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoNr19BkJJ802uHqUwMTCa8sSp3hOnFoDHTkbD7VvvWxBZDUCaJJicnFloaNozOn9ghH7gaMN47c1PA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



![img](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoM12GmQGZYFy7azn1RM2Iznj8Q2gQs4btqOD1edLs4NiaCEfe3CkKjKAKKcDsnGESOuQfhkHY4r5Hw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



![img](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoPvhibcLnC5hTcXqKITTp19OAGQ6v3CMNd82aSzq3ib9HJibexbJUfTD5lLKgnnJicYrmOlSF7BtnrbBg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

***咋用\***

![img](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoM12GmQGZYFy7azn1RM2IznibrWgBLOicIoeicsg3LGoSS6wTeO5SJomic3dofibictDVGkkudHjOHZekDA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



还是先下载：

https://github-production-release-asset-2e65be.s3.amazonaws.com/112717963/52dcd580-6853-11ea-99f6-53ebdc91feb4?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20200803%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20200803T052026Z&X-Amz-Expires=300&X-Amz-Signature=5da703e86f52d1db553411b6524b261032cabb3fcba189684cb12ec17684915e&X-Amz-SignedHeaders=host&actor_id=68997871&repo_id=112717963&response-content-disposition=attachment%3B%20filename%3DVirtualXposed_0.18.2.apk&response-content-type=application%2Fvnd.android.package-archive

ps：要网络环境……

then 

在这里面安装要需要使用的APP，以及其相对应的 Xposed 模块即可。你可以通过 APK 文件安装应用，但如果你原系统中已经安装了某款软件，，那么这时你可以直接克隆 (复制) 一份到 VirtualXposed 的虚拟空间来，而不必重复下载安装。

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)



你可以通过 APK 来安装 Xposed 模块，也可以通过 VirtualXposed 内置的 XposedInstaller 来安装和管理模块，这个跟通常的 XposedInstaller 使用方式是一样的

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)



![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)



![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)

***下次接着聊！![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)
\***

*

