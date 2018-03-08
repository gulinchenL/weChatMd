# weChatMd

## 微信小程序

>小程序是一种不需要下载安装即可使用的应用，它实现了应用「触手可及」的梦想，用户扫一扫或者搜一下即可打开应用。也体现了「用完即走」的理念，用户不用关心是否安装太多应用的问题。应用将无处不在，随时可用，但又无需安装。--张小龙


简单说，它就是一个可以实现之前只能是原生态APP可以实现的效果和功能的WEB工程。比如,可以直接和手机硬件交互的功能，录音啊，拍视频啊，调用手机的重力感应啊，GPS。这些是WEB所不具备的能力。

微信小程序在16年9月份被发布的时候，引起高峰但是短暂的轰动。这是小人挑战巨人的工具，众人趋之若鹜，以为可以凭借微信庞大的用户基础冲击某行业的巨头。然而能够凭借小程序飞天的小公司太少,仍然需要依靠自己的核心资源一步一个脚印.小程序没有官方的APP商店,做的好的小程序不一定会被人周知,如果想动心思通过诱导分享/诱导关注的流氓操作攫取用户粘度,只会被封停下架，比如心里测试大全（左右脑，完全随机的分析）。小公司活路少，大公司也不好受。

>我们决定不做了。我们知道小程序是什么了。哈哈，但是不能说。--罗振宇

[多数企业退出小程序](http://www.qlmoney.com/content/20170117-242429.html)

为什么小程序的高峰非常短暂?那时候的小程序功能十分简陋,支持和关联项都不多,审核严苛，难以变现，同时不支持游戏。

还记得去年圣诞节的圣诞帽APP么？

但是随着18年初小游戏的崛起，微信小程序又开辟了第二个战场。[这个是后话](http://www.cocos.com/1314)。

## 小程序技术栈

微信框架  神似vue框架

wxhl  wx版HTML,用view标签代替div标签,任何地方都可以插入view标签,如果报错或不适用,那就寻找定制的其他标签,如radio,直接看框架/组件部分

wxss  wx版css,和css一模一样,推荐看 [菜鸟教程CSS](http://www.runoob.com/css3/css3-tutorial.html)

js    推荐看[菜鸟教程js](http://www.runoob.com/js/js-tutorial.html)

json  类似于webview的配置

## 推荐公众号:

知晓程序

## 开发

[先从最重要的开始...](https://mp.weixin.qq.com/debug/wxadoc/product/index.html?t=201837)

[再从最基本的开始...](https://mp.weixin.qq.com/)

## tips

小程序在一年内多次更新,修复老坑的时候也会挖出新坑,网上很多教程会失效,大家按需食用。中小型的项目还是推荐单人开发，多人交流的模式。技巧和新坑，建议在讨论组里发布，其他同事踩过了可以解答，按周汇总，形成我们自己的手册。下面的这些是以前开发时遇到回忆的 ~~可能过时~~。

1. [页面通信/传值](http://www.ifanr.com/minapp/830664)
* 一些常量，可以交由 app.js 管理；需要持久化的量可以放在本地保存。
* 涉及到下级页面或者模板元素的数据，可以通过传入参数的方式传入。
* 后级页面可以通过获取堆栈里的页面对象快速修改上级的数据。

2. 小程序的接口地址都采用https协议

3. 注册页面时,先注册三级页面,再注册四级页面,以此类推

4. 开发时统一采用ip6(375*667 dpr=2),这样1px=2rpx,直接对应设计图的尺寸

5. 所有涉及微信接口,都必须通过服务器获取,不能直接发送请求
