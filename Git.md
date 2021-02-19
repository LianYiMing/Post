# Git使用全解

## 版本管理为何而生

> 搞过自己的项目嘛？

用软体搞曲子，hbuilder写个网站，AI和PS画个吊图

还是CAD搞个屌爆的设计，3D打印牛掰的建模

或者用word总结的教学经验，写的书

> 如果你习惯多端协作，版本控制绝对是个问题

任何时候任何设备都无法组织你的热情

早上吃饭用手机突发奇想改两下

地铁用mac笔记本详细扩展早上的奇想

班上偷偷用单位的Windows接着搞搞

晚上回家抓起Linux继续起飞

但。。。。

老子怎么同步文件

用U盘挨个拷咩？

> ”您老也不嫌麻烦“

**你应该了解下git**

>  你跟一堆人协作过咩？

当一堆人同时搞一个项目

宋兵甲刚写完项目介绍，电脑里项目文件却还是n天前的

炮灰乙打完工程的最后一个右括号，保存退出发现文件夹里项目的介绍却还是空的

流氓丙写完PPT，望着同样控不拉叽的文件夹拿起来电话

> "项目搞完了咩？微信发我"

然鹅超过100mb

![0](https://i.loli.net/2021/02/10/yY86RU9GVNdLHIm.png)

> "草！"
>
> “张小龙____”

还是只能拿着u盘傻不拉叽在寒风挨个去找。。。

如果几万人的大公司呢？

> ''博纳瑟也得送u盘跑死'

**牛逼的git闪亮bling登场**

<hr>

我们会发现不管是个人项目or团队协作

核心问题就是如何在不同设备处理最新的更改，也就是——

> 版本管理

项目开发不是小case——

大多数情况下需要整个团队甚至一个公司的人work together才能完成一个项目

只要能**提升效率**的东东一定就会有人搞

and我们刚刚聊到了

> 版本管理——在共同开发中很重要

于是也就有了现在的一大堆专门的工程版本管理器

遵循10分有逻辑性的规则来管理，

万人团队共同协作也不会导致版本错乱

而目前人数最多也是最适合个人项目用的

`Git`

关于团队开发才需要用到的功能，我们用不上，但其他的功能

```
it just works!
```

## git介绍

要用它就看看究竟是怎么个管理法

所有的版本管理都必须要遵循一条原则——

> 需要有一条主分支来来存放当前的最新进度
>
> 时间

这样就可以无论任何地点，通过时间就能将所有的更改有效的组织在一起

形成主分支

之后只要和主分支进行同步，就能够在最新的版本上进行工作，不至于有文件修改的冲突

其实用U盘在不同端互相拷文件，U盘就是”主分支“

为了方便——

主分支需要在继续工作的任何地方都能能访问的到

> 互联网

于是

不管是中心式管理版本的系统CVS,Subversion

还是分布式管理版本的Git

都有一个主分支且都放在服务器上

（所以其实不同的版本管理器都能个人用，只是应对细分情况有不同的处理方法，关于个人的版本控制可能无关紧要）

ps：服务器可以自己搭建也可以直接用现成的免费版本管理服务

> 由于这些版本管理方法只是一套思想，
>
> 所以即使不联网，在本地也建立本地仓库用
>
> 只是联网有利于多设备协作

git和其它主流版本管理器其实就是在”分布式上“

主流的代码管理器都是以中央分枝为主，

在各端修改好更新后提交给中央分枝

通过后再改变服务器里中央分枝项目，

再使用的时候只用在其它端同步一下，就能让版本与服务器一致

git也是这样

> 只是其他的项目管理器只认服务器

只要你的的提交不通过

本地的代码就对主分支的项目没有屁作用

只能是本地的一些普通文件

> 以我为主

![image-20210209111357218](https://i.loli.net/2021/02/10/ctJnO15y6xVLU7s.png)

而git则是像一个大树

在主分支工作的时候跟中心版本控制没有什么不同

而你还有另一个选择

> 分支

你可以在主分支外分出来一条不一样的分支

之后你的所有提交都会提交到服务器你分出来的分支而不是主分支上

> 还可以多条分支与主分支合并

如果没有文件修改的冲突（比如一个文件在其它分支和主分支上都被修改过）

就能完美合并

> 有屁用？

真的有很多屁用

在于多人开发项目的协同工作

各部门开发各部门的，每个部门一个分支，

首先在自己的分支上把本部门搞出来的最新代码和已经在其余部门的分支中验证无误的其它代码一起运行测试

之后与主分支进行合并，这样不管是哪个部门都能够用最新且正确的代码

来给自己新开发出来不稳定的代码进行测试

保证效率，也保证主分支的无误

> 牛逼格拉斯

![src=http___img.it610.com_image_info2_0ea4d608d94a434e84e69bf10ec0cc71.jpg&refer=http___img.it610](https://i.loli.net/2021/02/10/b653XTBkMy4OKDF.jpg)

各分支互不干扰，但仍以主分支为主

> 兼收并蓄

比中心版本管理貌似还要牛掰

世界上排名第一和第二的开源平台:

```
github,gitlab
```

全部是采用git作为版本管理器

最主要还是由于git对于开源社区的共同无偿协作的效率提升很有意义

（开源社区的共同协作，本质上跟公司的各部门协作没有什么区别，所以git就发挥了它的作用）

> Git就是当初在开发Linux的时候被开发出来管理代码版本的

当然这是git对于多人开发的巨大作用

> 个人使用git最大的作用——
>
> 把它当成了一个云同步的服务器

不过实际开发还是很有用的呢

## 实操

### 软件方法

分为`本地`和`服务器`的配置

服务器不同，本地的配置也不同，所以先选择服务器

github功能最多，国内的gitee码云最快

反正我用`github`

去官网创建账号，

![image-20210209121905066](https://i.loli.net/2021/02/10/4DIfL2KUw8xQAW1.png)

点击new创建一个新仓库

![image-20210209121954529](https://i.loli.net/2021/02/10/5GKj3bMB9X2SsWq.png)

只用设置仓库名就可以

![image-20210209122219597](https://i.loli.net/2021/02/10/2RwVFYBO6TXsxrH.png)

由于没有任何文件，所以提示你要在本地打开进行提交

> 分为便捷的应用无脑提交和屌炸的命令行提交

应用提交：（仅支持windwos和mac）

下载github的windwos+mac桌面应用

https://desktop.github.com/

![image-20210209122557778](https://i.loli.net/2021/02/10/3UwdXPCSHeNkyVf.png)

左边克隆仓库到本地

```
"Clone a repository from the Internet"
```

弹出来的窗口选择仓库和路径

![image-20210209123909686](https://i.loli.net/2021/02/10/psz73yDm19rFYjX.png)

克隆下来后

试着添加个文件

![image-20210209124120680](https://i.loli.net/2021/02/10/oMEmVhJUxQn7Z8C.png)

之后

```
左下角commit
```

```
右上角publish
```

```
右中侧Creat pull request是教你如何合并分支
点击后由于只有一个分支，所以怎么搞都会卡在这
不用管他
```

![image-20210209132923970](https://i.loli.net/2021/02/10/nyEgqPxw74ZCe8s.png)

之后就发布主分支master的第一个commit到github的服务器上

之后每一次修改后来应用提交一下就会自动同步到github云端

如果其它设备修改后提交到同一个分支，本地检测到，右上角就会变成

![image-20210209133249158](https://i.loli.net/2021/02/10/jzOiBM65vn29hlI.png)

点击就会将云端和本地不同的文件同步到本地

如果在第2个windows或者MAC上配置好github就可以实现多端的文件修改以及版本同步

> 这样就成功在不同设备和不同端搭建起来了个自动同步系统

并且在每个端都有clone到本地的文件，云端服务器还有一份，永远不会担心数据丢失，还能因为版本管理而变得高效

对于个人管理自己的项目就已经几乎完美了

<hr>

### 命令行方法

**以下是可以装逼的进阶内容**

> 选择阅读

##### 我们同git仓库中的文件状态来入手

> 文件状态

Git库中的项目文件有四种状态：

`未跟踪状态untracked`、

跟踪状态tracked：（分为三个）

1.`未修改状态unmodified`、

2.`已修改状态modified`、

3.`暂存状态staged`

`已跟踪`的文件是指已经被提交到git仓库的那些文件，

而`未跟踪`的文件是指还没被提交到Git仓库中的那些非Git忽略的文件

（Git可以通过在项目根目录下产生一个.gitignore文件，在里面指定要忽略的文件类型，这样Git就不会去监视这些文件的变化）

>  git通过文件名来进行跟踪

如果刚提交完一次git更新，那么所有文件都会是`未修改状态`

如果修改了文件(包括删除)，git还会认得这个文件，文件的状态就是`已修改状态`

如果你在文件夹里放了新的文件，git会不认得，也就是`未跟踪状态`,没有之前的文件版本可以比对

在本地通过add,给`跟踪状态`下的文件做个快照，记录下来`跟踪状态`下文件的修改

然后把`已修改状态`的文件（包括新增的文件）的**修改内容**放在暂存区，文件就成了`暂存状态`

之后通过commit给这次提交描述一下

本地的仓库就成功完成了git更新版本

本地项目的所有文件就会变成`未修改状态`

然后通过push提交修改到云端，将本地仓库新的commit提交到云端

（提交的改的内容是缓存区的内容，缓存区是文件修改的内容而不是文件本身，所以上传会很快，也为git的回滚奠定基础），

云端仓库上传完成后就与本地完全一样了





![image-20210209140356031](https://i.loli.net/2021/02/10/IVLYzONW3jSQkbZ.png)

发现提交git更新总共有如下步骤

1.通过add检测是否修改

2.如修改，把如何修改的内容（包括新增和谁删除了）放到暂存区

3.提交到本地仓库

4本地提交到云端

`新增加的文件`和`已修改的文件`的修改内容在add这一步都会会放入暂存区

之后完成提交更新后所有文件都会变成`跟踪状态`的`未修改状态`

这一过程可以通过软件来搞，也可以通过命令行来执行

> 执行的命令种类就叫做git

电脑端的桌面应用，本质上就是一个git命令的可视化执行命令软件

在底层也是运行了git 命令

所以只要能够找到命令行，并且安装git环境

就可以实现在任何地方使用git管理

> 甚至是手机
>
> 通过git可以将手机与电脑的项目完美同步
>
> 再搭配一些手机端的IDE就可以实现无电脑化的优雅写代码/搞工程

由于git命令在不同设备都一样

**电脑码字手机截屏很方便**。。。。。

就用安卓手机举个栗子

>  再次声明git命令是通用的呢
>
> Linux和Mac和Windows都通用

Android最好用的命令行是著名的termux

https://www.coolapk.com/apk/com.termux![图片](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoNm5dsN1XpKvuBGCjZSuIqQibU2ia3WXCKth0XpXvynphXibLSs5DJwv7Ten1qK67OsibDbYSdicexuiagw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
支持在Android安装一堆牛掰环境

强大如同Linux的终端

之后会详细聊

<hr>

打开termux

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoNm5dsN1XpKvuBGCjZSuIqQicfMhGLkKicn7gCmrZ0yE5ic1xdG1w5UwTpgnz4jOAeUPtay477ibhnzMA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

通过pkg包管理器可以直接安装git（可以把pkg理解成开发环境的应用商店）

Linux和Mac自带pkg环境,，Windows可以直接通过exe程序来安装git

详见附录

执行git安装命令

```
pkg install git
```

会弹出来如下代码

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoNm5dsN1XpKvuBGCjZSuIqQQfDn5oiaH4NCz2JfhiavWzMqwmbEwicapTibzXV9d5QpqffsvU63H9MA8A/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
之后会有do you want to continue?

输入y接着进行git安装
![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoNm5dsN1XpKvuBGCjZSuIqQpn2EOHdJhCN8cgydYicq9t6ibPxbkY9xmDurbRqhKX4bOf2v08DWGeZQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
一切正常，回出现上图所示代码提示，最后两行是setting up

也就是安装成功

输入git --version

运行一个最简单的git代码→查看版本

如果底下弹出了git版本就说明安装成功了

这样termux终端就成功安装上了git

git为了确保安全，通过rsa加密进行ssh数据传输（也就是https加密的方法）

总之需要我们进行验证

首先让termux和Linux+mac终端装上支持ssh传输的环境

执行

```
pkg install openssh
```

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoNm5dsN1XpKvuBGCjZSuIqQq3tELl9MvdHnnIMeVLULAuItNslYWtbB1QweDMVxSXZTKSGLEfibTrw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

时间会很长，慢慢等

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoNm5dsN1XpKvuBGCjZSuIqQ93XNOkMOeYEa5r3J83TzVgaJPLh56m9kGf5ltdWwJSAaAUhhbe7LFQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

安装完ssh之后(也就是进度条走完)

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoNm5dsN1XpKvuBGCjZSuIqQ93XNOkMOeYEa5r3J83TzVgaJPLh56m9kGf5ltdWwJSAaAUhhbe7LFQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

会弹出来一堆东东

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoNm5dsN1XpKvuBGCjZSuIqQofgqVbA1zkzib8BfzKrXWLRAticcOFeRZoXzeY9qpTicnumfPKKTVuIpA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

如果弹出来跟上图一样就可以使用ssh了

这时候执行

```
ssh-keygen -t rsa -C "git@github.com" 
```

如果使用github的git，就要在第一步执行

如果是其他就改@后的名称，比如码云就是（应该是git服务器的域名）

```
ssh-keygen -t rsa -C "git@gitee.com" 
```

ssh密钥最后会显示

如果搞错git服务就重新执行

```
ssh-keygen -t rsa -C "git@改过来的你想用的服务"
```

之后按三次回车

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoPm71Kyw5tKey12KrOwtvINibqhoK1yiaYbTVRVNcIOKaS30eegJsJamS8UnXc23bpnBN8XcRJCfJicA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
如果遇到是上图，就是失败了，如果是下图就是成功

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoPm71Kyw5tKey12KrOwtvINP9EyeeHODDTQTM5dX7lr2Jb5yyy5BkK04ZEyDiaPl2fMOZvVA4kMY0Q/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
ps：发现输三个空格会失败，打一个字母再回车就不会

之后执行代码来查看ssh密钥

```
cd ~/.ssh
```

这一步是安卓端到ssh公钥的目录，

公钥和私钥都在termux的data分区里，

termux的默认目录也就是它的data分区

之后执行

```
cat id_rsa.pub
```

查看`public key`——公钥(具体的rsa加密之后详细聊)

![img](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)

把后面这一段乱码复制下来，包括前面和后面的

我们现在有了ssh的公钥，为了能让github认出是我们

要去github粘贴公钥

https://github.com/settings/profile

也就是找到设置

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoPm71Kyw5tKey12KrOwtvINawKek6BrY1b3Qn6UpVNP49Ep3tPBr9wZmNC49MRTGo5DaO05tAvpCA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
之后找到

```
ssh and Gpg
```

直接访问下面的链接也可以

https://github.com/settings/keys

右上角添加刚刚复制的公钥，也就是向github说有这个钥匙的人是值得信任的，就可以通过拥有该公钥的本地进行push代码更新

(因为github添加了公钥，

后只要有公钥都可以进行push分支，

所以你的公钥泄露就可能会被恶意疯狂窜改仓库，所以要打码)

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoPm71Kyw5tKey12KrOwtvINFylx8wS1t8fADjgxZ4DbbsBXquDUhmqeelJCAxVpCa2KicnDPTlZibvA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
之后会这样

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoPm71Kyw5tKey12KrOwtvINJbK92czsVW2QuH2GEiahXYA5XE09RQtp70P89yvUribz84g4HMUedx1A/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
也就是成功了

回到termux或者Linux+Mac的终端

执行git命令赖克隆一个仓库到本地

```
git clone git@github.com:用户或组织名/仓库名.git
```

比如一个仓库链接是这样

https://github.com/LianYiMing/SiteBuilding

那就要执行

```
git clone git@github.com:LianYiMing/SiteBuilding.git
```

其它git服务同理

注意，clone是不需要密钥就能搞的

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoPm71Kyw5tKey12KrOwtvINiaevnfOzIHUibvibegSEnDcgqeYhd3nydFC48l2lU6Ho0hicb3zxnTAy5g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
如图

之后会弹出下图
![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoPm71Kyw5tKey12KrOwtvINFABD96JSaZvkMK4zv64YNN4ibTFHTsuKZqXtdx3nmp4dGDzGrmIsdYA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
也就是会有克隆的进度

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoPm71Kyw5tKey12KrOwtvINI9s94NTvylYRwmcibkicto1TeCv8ZMjeicERiaBriczKF4yaouEOnbfFesg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
然后就克隆成功了，回到termux的data分区就能看到克隆的仓库了

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoPm71Kyw5tKey12KrOwtvINGcES9iblWFy4qoUxQiad4UlPUiavicH41hFCPlib9nG9Vntulj0BIoGlFnw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
但是data分区属于非android一般用户的权限分区

不root看不到，所以就需要用[CD命令](https://mp.weixin.qq.com/s?__biz=MzI4Nzc2MzA3OQ==&mid=2247485756&idx=2&sn=457f57a0a44eb3001997f1a528a8f986&scene=21#wechat_redirect)来放到其他地方（当然Linux和MACos也需要cd一下）

 Termux上的CD命令LinuxMAC都通用

```
cd 目录绝对路径//相对于root根目录来说的路径,也就是右键-属性看到的路径
```

对于Android：

‘’这里的root目录我们平常访问不了

只能访问root目录里的一个子文件夹→内部存储

所以CD命令要cd到内部存储的路径‘

比如

```
cd storage/emulated/0/Downloa/Github 
//不同机子不同安卓版本内部存储路径不一样
```

<hr>

```
cd ~
```

跳到自己的home目录(也就是命令行所在的目录)

Ps：termux的home目录也就是他的data分区

```
cd ../..
```

跳到目前目录的上上两层

> 我们只需要用第1个CD就可以

------

首先我们先要确定克隆下来的文件存放的文件夹的目录

Android端——原来聊过的xplore可以查看

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoO630NQrZ6lWpmfrpAcjNfLILkS0jsrRDs0Q85aGl2bwleaB3cIlc9NJzFSia52MoqNlCRicg5OF7vA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
如图最上面就是文件路径

长按之后点击文件详情就可以一键复制

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoO630NQrZ6lWpmfrpAcjNfLIQdvFYqZiaibe2C1KJ9y4vu9NNiavdNxJnAm2uZKvOLMdOytdVn6uibbhA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

> 用MAC和Linux的人我不信搞不清楚路径

回到termux或者终端

执行下cd（重新启动termux或者终端后路径会重置）

```
cd /storage/emulated/0/Download/Github
```



这时候执行的clone操作就会克隆到这个目录里

执行clone

```
 git clone git@github.com:LianYiMing/SiteBuilding.git
```

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoO630NQrZ6lWpmfrpAcjNfLkVAW0YKvDZrYIibV5nBTZN9teoAKDODVSmswuayM6ic1FGmjO7hicAhug/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
这样就成功把git仓库克隆到指定路径了

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoO630NQrZ6lWpmfrpAcjNfLraFCqY7swtGHEibymckzibbosdI7zMNlibQcVOme5uibOpG6Hb7fTduM5g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

#### 如何提交git?

首先需要执行代码来验证身份

```
git config --global user.email "AGZX_lym@163.com"
```

上面双引号里填入你的github注册邮箱

```
git config --global user.name "LianYiMing"
```

双引号填入github用户名

![图片](https://mmbiz.qpic.cn/mmbiz_jpg/tMsLbdfwxoO630NQrZ6lWpmfrpAcjNfLH8nUQnM1m8j2uj471eSiaoRXgtLm9nkFxnIjC64oOaiancDxswvakvlQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

之后修改一下刚刚仓库里的文件，以确保可以提交，没有修改过的话提交会不成功

回到termux/终端里，执行划线句子(建议分次)

```
cd 仓库路径
```

```
git add .
```

把包括新文件的所有项目文件提交到缓存区，并且检测跟踪状态下的文件修改并`记录修改内容`

add是一个点，代表cd路径内的所有文件

点还可以换成单个文件名（感觉不常用）

> 话说rm-rf也是打错点就GG

之后通过commit做个便利贴

```
git commit -m ‘内容描述’
//写啥都行，反正不能为空
```

> commit -m便利贴的作用
>
> commit更牛逼
>
> git是通过commit来辨别每一次更新的
>
> 每一次提交commit后，都会给这次commit生成一个唯一的ID
>
> 保存在log中
>
> 为回滚奠定基础

这样就完成了一次本地仓库的git版本更新

```
git push
```

上传本地仓库比云端多出来的commit

运行完这些就提交成功了

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoMackP5CICx7TN3GIRN5NnAlEYG10NQcaj8RiaVTHQhniaU3AcVicyVHlacQISScoysHxcD05l0KggDQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
这时候回到github上就可以看到刚刚的提交了

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoMackP5CICx7TN3GIRN5NnAFXvkAkR1Mrevqgb8Hu8yovXCdPCxhWF2lyFxGJibwbbznAQcMHKTuDw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

还有一些比较重要的操作

```
git pull
```

````
git fetch origin
````

```
git merge origin /master 
```

在多台设备上同时作业就会导致本地的仓库最新版本不一样，

就需要用到git pull和fetch

向git服务器请求文件，如果有本地没有的或者更新时间比本地新的就下载下来

如果没有下载就直接提交，就会导致版本混乱

报错

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoMackP5CICx7TN3GIRN5NnAenYHgwhZCQ10t0ZsLTlicvgojAw2R2ONfqkDDrspYkAbmFT8krx5fXA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
git  pull在实际用起来貌似与下面两个一样

但是也有很大的区别

使用中git pull感觉就够用了

可以参考下大佬的：

https://blog.csdn.net/weixin_41975655/article/details/82887273

```
git diff  
```

 显示目录里的原文件和最新提交/缓存区的区别

会输出类似这样

```

a/README.md b/README.md

index e69de29..cb5dc9f 100644

--- a/README.md

+++ b/README.md

@@ -0,0 +1 @@

+# 廉一鸣
```

如果没有用 git add命令向暂存区添加任何东西，只会显示工作树与最新提交状态之间的差别。

“+”号标出的是新添加的文件

被删除的文件则用“-”号标出

```
git add README.md
```

> git add 文件名 //只提交一个文件的修改到缓存区

git add如果后面加一个点，就是把所有文件的修改内容放到缓存区

反之可以只提交一个文件的修改内容到缓存区

git可以记录下来每一次缓存区的内容

> 因为缓存区的就是每一次文件是如何修改的

一方面有利于快速把最新更新上传到服务器，另一方面还有更大的优越性——

> 回滚

git每一次的commit缓存区的内容都被记录了记录下来

也就记录下来了每一次提交的变化

> **那么就可以使项目文件回到任何一个时间点的版本**

时间点如何辨识？

每一个commit提交都会生成一个ID代码来进行辨识

所以我们只要通过执行命令

通过commitID就能让文件回到不同时间的不同版本

```
git log <filename>或者. //查看一个文件或者所有文件的每一次提交
```

这一操作会输出commit ID

```
git checkout  <commitID>  <filename>或者.
```

也就是开始回滚操作——让文件回到commitID所对应的那一次仓库提交时文件的版本

filename换成.就可以让整个仓库回到原来的情况1

> 去git服务商的官网也可以进行手动回滚操作

**查看与最新一次提交的区别**(也是github客户端每次打开窗口前所执行的)

```
git diff HEAD
```

就会输出时间最近的一次提交和当前目录文件的区别

如果刚同步完就不会有执行结果

![图片](https://mmbiz.qpic.cn/mmbiz_png/tMsLbdfwxoMackP5CICx7TN3GIRN5NnAGQvw3ymLpKBEAGNURvg1qAKRThh0YhIrMJ3sp5GY6ibkucoMjiaLektQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
@@底下是文件的修改内容

加了一行回车所以就会显示

\+ 

<hr>

有了上面的这些命令操作git就能达到跟客户端软件一样的效果了，

当然还有更多git命令

使用情况如果更加复杂，直接百度应该就能找到

感觉不错的

```
https://blog.csdn.net/asoar/article/details/84111841
//git回滚的更多操作
```

```
http://blog.sina.com.cn/s/blog_e83e4f210102vnn1.html
//一堆git命令
```

<hr>

### 附录

#### Windows安装git

首先跟装Java一样从官网下Git安装器

官网地址：https://git-scm.com/downloads

之后一路next到底，用程序的默认设置就可以

狂点next后就会安装成功这时候后打开cmd命令行

![image-20210210040108357](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210210040108357.png)

 Git不是通过cmd运作的，而是通过他自己的一个命令行——git bash

> 当然安装完git后cmd也可以用了

![image-20210210041315238](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210210041315238.png)

安装完后勾选可以直接运行git bash

```
lunch gitbash
```

会弹出来bash窗口

就可以使用git命令了

#### 本地仓库

> 其实版本管理费只是一套思想，并不是一个产品的名称

比如说git并不需要服务器的同步，本地就是一个完整的git仓库，

服务器的作用只是在于便于多端协同工作罢了

> 所以本地的Git环境只有一种而git服务器有很多种,提交云端后本地文件的状态不会改变

然后问题来了，本地是如何记录下来每一次的修改了呢？

在本地克隆下来的文件夹里，会有个叫做git的目录放着git这一版本管理系统的核心文件

每一次commit的缓存区都会被记录下来

因为缓存区记录修改而不是所有文件，就节省了很多体积呢

如果不想用服务器git同步管理版本那么就需要安装git环境后执行

```
git init
```

也就是在命令行所在路径中生成一个git仓库，在这个仓库里就支持一切git命令了

#### 云同步

我们把git作为个人项目的管理，主要还是因为github采用的git

github的服务是免费的，并且仓库无限大小，

如果项目真的不错，还有可能被很多人收藏，共同协作

所以就采用git管理个人项目

由于git有现成的免费的无限的云同步

> 不用白不用

但其实其他版本系统对于个人开发也没什么区别

<hr>

#### Git的前世今生大概就是这样了呢

>  **善用工具真的阔以提升效率**

明天见！

<hr>
### 