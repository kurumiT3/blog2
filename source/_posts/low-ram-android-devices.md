---
title: 低运存安卓手机生存指南
date: 2020-08-27 14:56:44
tags: 
         - 教程
         - Android
thumbnail: https://rmt.dogedoge.com/fetch/kurumit3/storage/Exams-bro.png?w=1280&h=600&fmt=webp
---

📖本文在少数派上同步发布，可选择在少数派[阅读此文](https://sspai.com/post/62351)

# 序言

<img src="https://rmt.dogedoge.com/fetch/kurumit3/storage/ccc3380d16d7e75971aaa3cdac82dad7.jpg?w=1280"  />

虽然都2020年了，但我相信一定有许多用户和我一样总觉得自己的运行内存总是不够，被系统疯狂杀后台，甚至连复制文件都会卡死。

—————————一条可爱的分割线—————————

# 正文

*P.S.以下介绍的大部分内容需要root或adb*

## 一 . 简化系统服务

无论是国内定制UI的各种花里胡哨的功能，还是类原生的google全家桶都会在后台允许拖慢速度，增加耗电

### 1.冻结

可冻结你认为无用的功能（不知道是啥的建议先查一下，防止翻车）推荐使用 [小黑屋](http://www.coolapk.com/apk/web1n.stopapp) 完全不需要付费可无限冻结

<img src="https://rmt.dogedoge.com/fetch/kurumit3/storage/cb537b6b865441085da300b91798ddb6.jpg?w=1280" style="zoom:33%;" />

### 2.直接卸载

（该方法有一定风险请务必不需要，且删除后无影响才卸载）
大多数系统app无法通过第三方应用卸载，所以需要手动删除。
请确保有root权限 system已解锁。这里是用的是[ MT管理器](http://www.coolapk.com/apk/bin.mt.plus) 系统app通常在以下几个文件夹中，可逐一查看（在根目录中）：
1）.system/priv-app
2）.system/app
3）.system/product/priv-app
4）.system/product/priv-app

<img src="https://rmt.dogedoge.com/fetch/kurumit3/storage/27a4bc71d3d83b0ff90e714c5c92720c.jpg?w=1280" style="zoom:33%;" />

### 3.谷歌服务

1） 使用magisk模块（谷歌打盹doze）
2）可使用microg代替
3）直接冻结或删除

## 二.利用第三方杀后台

1.[绿色守护](http://www.coolapk.com/apk/com.oasisfeng.greenify) （杀后台能力较弱，不推荐）

2.[黑阈]( http://www.coolapk.com/apk/me.piebridge.brevent )（需要捐赠，杀后台能力一般，但有一定效果）

3.[Thanox](http://www.coolapk.com/apk/github.tornaco.android.thanos) （需要xposed框架，功能强大，可设置自启动，后台运行，移除应用卡片后杀后台等，非常完善）

<img src="https://rmt.dogedoge.com/fetch/kurumit3/storage/e1773915ae085c3bd5193ac9f887a308.jpg?w=1280" style="zoom: 33%;" />

4.黑阈补丁版（杀后台非常强，但不支持Android10且杀的太快了）可通过 [镧系统工具箱2](http://www.coolapk.com/apk/xzr.La.systemtoolbox )打补丁



## 三.SWAP&ZRAM

### 1.swap

其实swap就是把存储空间当作运存用，效果较明显但占用空间。运存小的手机本来存储空间也不够用
用过 [scene工具箱](http://www.coolapk.com/apk/com.omarea.vtools)和 [镧系统工具箱](http://www.coolapk.com/apk/xzr.La.systemtoolbox) 可实现，效果较明显，但有副作用

### ![](https://rmt.dogedoge.com/fetch/kurumit3/storage/74af8d5df05f89160c77cc0511ce9713.jpg?w=1280)2.zram

主要通过压缩运存，来提升体验
同样可通过以上两个应用启用，另外也可以使用@yc9559 的 [QTI模块](https://github.com/yc9559/qti-mem-opt/)
四.内核相关
还有一个办法(部分符合条件的手机可能不支持)
如果你有root权限且安装了 busybox安装 [内核调校](http://www.coolapk.com/apk/com.grarak.kerneladiutor) ，在“低内存管理”把“空程序”拉的很高，建议重启一下手机之后看一下剩余运存，把滑块拖到那个值上，记得勾选开机自动设置和允许内核调校开机自启动。
“内容提供程序”也可以适当拉高
后台程序适当降低可以达到不掉后台的效果
原理是安卓系统有一个东西叫做低内存管理，用魔法打败魔法😎

## 五.应用简化

各类的app现在功能都越来越多，所占用的内存也越来越多。你可以选择官方简化版或第三方，也可以使用play版或不那么臃肿的旧版本😏
例如 
微信的7.0.9（最后一个可以秒启动的版本）
网易云音乐的4.3.1
bilibili的play版
QQ的办公版tim或[play版](https://kurumit3.lanzoui.com/ic47Ufrcx6d)配合简洁模式
微博第三方 [Share](http://www.coolapk.com/apk/com.hengye.share)
贴吧第三方贴吧lite
知乎精简版知乎lite
还可以将网易云和QQ音乐等合并使用 [倒带](https://rewind.kusstar.xyz/#/) 或[发条](http://www.coolapk.com/apk/com.guowan.clockwork )
部分应用你甚至可以使用网页版😎

可以利用[VIA插件](http://via-app.cn/#/tabBar/home)去除广告和限制从而使网页版可用

<img src="https://rmt.dogedoge.com/fetch/kurumit3/storage/bdb9cf1bc60186cdf819ac5bdc995a94.jpg?w=1280" style="zoom:33%;" />

## 六.关于系统

国内定制UI有时会较为臃肿，有许多不必要的功能，有时为了更流畅的动画也会让低运存手机负重不堪所以你可以选择自行删除这些不必要的服务或选择刷类原生。

*以上内容皆为个人见解，如有不足或建议，欢迎讨论*

------

***END***