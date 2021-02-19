---
layout:     post
title:      Androlua*布局属性*『类型』
subtitle:   
date:       2020-9-18
author:     廉一鸣
header-img: 
catalog: true
tags:
    - n.

---

## Androlua*布局属性*『类型』

我们第一刚聊到了一个线性布局的代码，大概是这样的



layout={

 LinearLayout,

 layout_width="fill",

 layout_height="fill",

 orientation="vertical",

 backgroundColor="#FF464C6F",

}



activity.setContentView(loadlayout(layout))

大括号外的都说的差不多了，但是括号里貌似一点都没说，所以今天就来聊聊括号里的第一行

**LinearLayout,**

既然是要写布局，上次又聊到了布局有很多种类型，所以第1行就要声明，这是一种什么布局

--线性布局（LinearLayout）：按照垂直或者水平方向布局的组件。

--帧布局（FrameLayout）：组件从屏幕左上方布局组件。

--表格布局（TableLayout）：按照行列方式布局组件。

--相对布局（RelativeLayout）：相对其它组件的布局方式。

--绝对布局（AbsoluteLayout）：按照绝对坐标来布局组件。(也就是要用到像素)



比如说这就是一个线性布局

layout={

 LinearLayout,

 layout_width="fill",

 layout_height="fill",

 orientation="vertical",

 backgroundColor="#FF464C6F",

}

activity.setContentView(loadlayout(layout))

不同的布局排列不一样，其他属性(也就是LinearLayout,下面的几行)也不一样，所以要先在这声明一下

具体声明的值直接就是布局的名称，也就是上面说的5个布局，直接打入上方布局括号里的英文，然后英文逗号结尾，就声明成了

声明之后，在底下就可以直接用属性了，其他属性之后继续聊叭