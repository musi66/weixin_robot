通过自己编译rom实现的微信机器人,rom自带v2ray透明代理, 没有任何三方框架, 安全系数极高, 稳定性好, 不会被封号

# 支持的功能
1. 发送消息(文字,语音,红包,图片, 视频,小程序, 图文连接...)
2. 消息拦截
3. 发送朋友圈
4. 视频号相关功能
5. 修改个人资料
6. 群管理相关
7. 加好友相关


# 目前市面上搭建微信机器人
首先微信机器人分很多种。
一、 从实现原理来分
1、以 hook 微信的方式来实现。
又可以细化为两种。即有 hook PC 端 (Window 系统）的微信，也有 hook 手机端（ Android 系统）的微信。
1.1 hook PC 端的代表作：wetool。功能超级强大，虽不支持二次开发，但已有的功能足够个人使用，可惜官方作品已被腾讯告死，好在市面上还流落着不少破解版，有需要的自行搜索。另外还有一个需要进行二次开发，才能使用的非主流框架可爱猫，需要的自行研究；
1.2 hook 移动端的代表作：太极。功能也很强大，不支持二次开发。使用起来相对比较复杂，一般人玩不起来。 （也是我目前在用的微信机器人）
无论是 PC 端还是手机端，用 hook 方式实现的最大缺点就是要和某一个版本的微信客户端进行绑定，如果框架本身不对最新版本的微信适配，那使用的时候就无法升级到最新版本的微信。
2、通过模拟微信通信协议的方式来实现。
又可以细化为两种方式。
2.1 通过模拟 web 协议的方式 ，代表作：ItChat。曾经红极一时，号称三十行即可自定义个人号机器人。可惜的是，微信官方已不准许新的微信号再使用 web 登录，这就直接从源头扼杀了 web 协议的微信机器人，虽说老的微信号还是能凑合着用，不过部分功能也受限。
2.2 通过是非 web 协议，如 Pad 协议、Mac 协议，代表作：wechaty。当然它自身也支持 web 协议，而且 web 协议的机器人是免费的。这哥们打着开源的幌子，主要代码并没有开源，只是提供了一套 SDK 而已，除了 web 以外的通讯协议均付费（大概 200 一个月吧），才提供调用的 token。
以协议的方式来实现不需要和微信客户端绑定，但他们基本上都只提供 API，并不是可以直接拿来用的成品，需要进行二次开发才能使用。二次开发对普通用户来说是个巨大的门槛，但对懂编程的人来说是个巨大的优点，要实现什么功能由开发者来定。如最近很火的 ChatGPT 大都是通过 wechaty 二次开发接入。
二、 从终端来分
1、 wetool、可爱猫需要运行在Window电脑上，并且要和某一个版本的微信绑定；ItChat、wechaty也需要部署运行在电脑或服务器上。所以，这些都属于 PC 端的微信机器人。
2、 太极可以直接安装到Android手机上运行，所以属于Android端的微信机器人。
三、 从功能上来说
理论上手机端微信机器人的功能是多余 PC 端的。因为手机端微信的功能本身就多余或者说领先 PC 端，例如红包相关的功能，PC 端的微信就无法处理吧。所以抢红包的功能就只能由手机端的微信机器人来做。
不过，PC 端的微信机器人在使用上比手机端方便，尤其是群管理相关的功能，在 PC 上一目了然，一眼看过去就知道如何使用。而手机端就很鸡肋，入口深，配置难！另外就是PC端的微信机器人大都支持二次开发，扩展性很强。
所以，还是要根据自己的业务需求选择适合自己的微信机器人。
四、 风险
使用任何一款微信机器人都会风险。
1、被腾讯官方封号的风险。 但只要不是用的特别过分一般都不会被封号，如果你每天都群发几百次，加几百人，即使你不用微信机器人也会被封。一般情况下被封不是因为你使用了微信机器人，而是你触发了请求频率，以我为例，PC 端和 Android 端的都用过 2 年多的时间，从未被封过。
2、信息泄露的风险， 这个无解。毕竟是在别人框架 / 通讯的基础上运行，谁也保证不了是否有暗门，除非你自己撸一套框架。



