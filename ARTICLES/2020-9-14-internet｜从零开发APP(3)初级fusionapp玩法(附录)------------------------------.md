---
layout:     post
title:      internet｜从零开发APP(3)初级fusionapp玩法(附录)
subtitle:   
date:       2020-9-14
author:     廉一鸣
header-img: 
catalog: true
tags:
    - 从零开发APP

---

## internet｜从零开发APP(3)初级fusionapp玩法(附录)

你好鸭，昨天我们聊了用fusionAPP，把一个网页封装成一个应用 

今天再聊一聊其他可以调的参数叭

------

1. 组件

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoOjyUkY6ib6cEuOq9q52kibTAibXf61BRm6YsMM1VZoBEFKDMcCIPAu8ticL7pWEIth1UqHcqdex4XP9g/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
菜单项目也就是点开右上角会弹出来的东东

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoOjyUkY6ib6cEuOq9q52kibTAxBlXja3jQ7rHicpGDs9VFoAj9jFxnpgGLwpbziaKddXgDVQhOHrRx4aQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)点击加号后

![img](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoOjyUkY6ib6cEuOq9q52kibTAFUYz376w0C0IXGT6Ju8fOMUQ2N0qGEtDdtYLPIV9hbkI3HWb8uiahdw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
项目名称就是显示的文字，点击事件也就是要填入lua的代码，虽然说作者内置了很多，但是还是很不友好，，，，进阶的时候聊

搜索模式同样之后聊

顶栏图标

比如说这些

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)
![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)
点击之后发现，还是要添加点击事件，跟上面一样，需要学一点[lua](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247484791&idx=3&sn=60b4a45d56f88dbee6e04301289a72a9&scene=21#wechat_redirect)知识，所以这也是之后要聊的，右边的三个点可以选择作者在应用里内置的一些[矢量图](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247485062&idx=2&sn=503c195d337c92c98246dbd513eec90b&scene=21#wechat_redirect)

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)
侧滑栏，侧滑栏顶部图片如图

列表项目还有悬浮球，都可以参照刚刚的顶栏图标的设置，都是先定义文字，图标

再设置点击事件

点击事件理论上懂得越多，能够实现目的的方法就越多，等到时候聊进阶的时候详细聊一聊叭

作者在点击事件里内置了这几个选项

进入子页面

加载Js(之前聊过，是Javascript)

加载网页

停止加载

刷新网页

网页前进

网页后退(也就是相当于按了返回键)

返回网页顶部

阅读模式(也就是只看网页文字)

显示对话框

显示泡沫对话框

弹出消息

退出程序

退出页面

复制文本

分享文本

分享链接

发送邮件

联系QQ

加QQ群

页内查找

点击元素

下载文件

执行 Shell

------

明天聊属性!

