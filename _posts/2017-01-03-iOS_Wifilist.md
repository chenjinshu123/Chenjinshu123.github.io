---
layout: post
title: 卖船神教，史上最佳游戏还是最大骗局
date: 2018-06-21
tag: 游戏
---

　一款好游戏，3A游戏，要投入多少钱开发？
业界老司机七爷首先想到的是GTA系列。这个系列的最新作，GTA5，开发费用达到了2.68亿美金！不过有另一款游戏，虽然还没有完成但所有人——包括它的粉丝和它的喷子——都认为如果它能做完，开发费用绝不会低于GTA5。这是怎么样的神作？
<img src="/images/posts/Xcode8/image1.png" height="200" width="600"> 






```
kNEHotspotHelperCommandTypeFilterScanList： 表示扫描到 Wifi 列表信息。

NEHotspotNetwork 里有如下信息：

>* SSID：Wifi 名称 
>* BSSID：站点的 MAC 地址
>* signalStrength： Wifi信号强度，该值在0.0-1.0之间     
>* secure：网络是否安全 (不需要密码的 Wifi，该值为 false)
>* autoJoined： 设备是否自动连接该 Wifi，目前测试自动连接以前连过的 Wifi 的也为 false 。
>* justJoined：网络是否刚刚加入
>* chosenHelper：HotspotHelper是否为网络的所选助手

[官方文档连接](https://developer.apple.com/reference/networkextension/nehotspotnetwork)


### 6、获取Wifi列表回调

当你把上面的代码写完，并成功运行项目后，发现并没有Wifi列表的回调。因为你还没刷新Wifi列表，你需要：

* 打开手机系统设置 -> WLAN -> 系统 Wifi 列表加载出来时，上面代码部分才会回调，才能获取到 Wifi 列表。

<img src="/images/posts/Wifilist/WLAN.png" height="360" width="200">  

这个时候你就能看到控制台源源不断的Log。

### 注意事项

* 1、获取Wifi列表功能由于是需要申请后台权限，所以能后台激活App(应用程序)，而且激活后App的进程能存活几个小时。
* 2、整个获取Wifi列表不需要App用户授权，也就是在App用户无感知下获取设备的Wifi列表信息，使用时请正当使用。
* 3、Wifi列表获取 NetworkExtension 是 iOS 9以后才出的，目前 iOS 9 已经覆盖很广了。


下面付一张来自 [TalkingData 对iOS操作系统的统计报表](https://www.talkingdata.com/index/#/device/os/zh_CN)，时间：2017-01-03

<img src="/images/posts/Wifilist/systemVersion.png" height="280" width="600">  

### Q&A

在操作过程或者文章有问题的话欢迎在 [原文](http://baixin.io/2017/01/iOS_Wifilist/) 里提问或指正。

>* 使用 Demo 我就不提供了，你如果没有申请 NetworkExtension 权限，提供了 Demo 你也无法使用。

<br>

参考资源：[NEHotspotHelper NetworkExtension API iOS9.0](http://stackoverflow.com/questions/31704292/nehotspothelper-networkextension-api-ios9-0)

<br>
转载请注明：[潘柏信的博客](http://baixin) » [Wifi 定位原理及 iOS Wifi 列表获取](http://baixin.io/2017/01/iOS_Wifilist/)  


