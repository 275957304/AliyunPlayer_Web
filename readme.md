## Aliplayer web播放器场景化和自动定义组件Demo

每个例子都是独立的，方便单独使用，现在使用webpack配置文件都是基于2.0版本的，如果使用最新的4.0版本，需要自己重写webpack的配置，如果不想手工安装webpack2.0， 可以直接[下载依赖项](https://player.alicdn.com/aliplayer/node_modules.zip)，直接存放于使用例子的文件夹下面。

### 点播demo

包含播放、播放列表、评论、点赞、客户端长连接mqtt等功能，支持在android微信全屏H5同层播放，解决android微信弹出全屏播放的问题。

[说明文档和代码](https://github.com/aliyunvideo/AliyunPlayer_Web/tree/master/h5VodDemo)

![移动版](https://player.alicdn.com/aliplayer/img/h5demosmall.png) 

### 直播demo

包含全屏播放、评论、点赞、客户端长连接mqtt等功能，支持在android微信全屏同层播放，解决android微信弹出全屏播放的问题。

[说明文档和代码](https://github.com/aliyunvideo/AliyunPlayer_Web/tree/master/h5LiveDemo)

![移动版](https://player.alicdn.com/aliplayer/img/h5livedemo.png) 

### 多平台点播直播Demo

包含播放、播放列表、评论、客户端长连接mqtt等功能，支持在android微信全屏H5同层播放，解决android微信弹出全屏播放的问题， 

根据设备类型自定选择移动版或桌面版播放。

[说明文档和代码](https://github.com/aliyunvideo/AliyunPlayer_Web/tree/master/multiPlatformLiveDemo)

#### 桌面版

![桌面版](https://player.alicdn.com/aliplayer/img/pclive1.png) ![桌面版](https://player.alicdn.com/aliplayer/img/pclive2.png)

#### 移动版

![移动版](https://player.alicdn.com/aliplayer/img/reacth5live.png) 

### 自定义组件demo

此Demo关于H5播放器的自定义组件，可以作为自定义组件如何实现的参考，在这里也可以找到一些常用的自定义组件。

[说明文档和代码](https://github.com/aliyunvideo/AliyunPlayer_Web/tree/master/customComponents)

![移动版](https://player.alicdn.com/aliplayer/img/customcomponents.png) 



```

如果不希望退出后直接关闭页面，可以在代码中对上面的代码添加注释。

#### [Aliplayer官方文档](https://help.aliyun.com/document_detail/51991.html?spm=5176.doc62941.6.704.Lcuzlc)

#### [体验demo](https://player.alicdn.com/aliplayer/)

#### [参考文章](https://help.aliyun.com/document_detail/62953.html?spm=5176.doc51991.2.21.c1yAdY)

#### [实现介绍文章](http://www.jianshu.com/p/4ac1aa9fd087)

![移动版](https://player.alicdn.com/aliplayer/img/h5demosmall.png)  


### 安装依赖项

本Demo使用了ES6、webpack、gulp等技术。

 - [Node.js](https://nodejs.org/en/)
 - [Webpack](http://webpack.github.io) 
 - [gulp](https://gulpjs.com)

```sh
$ cd h5demo
$ npm install

```

### 编译

#### 开发环境

启动webpack dev server微服务，支持监听文件变化，实现时时打包，支持热模块替换。

```sh
$ cd h5demo
$ npm run dev
```

#### 产品环境

```sh
$ cd h5demo
$ npm run prod
```

#### Q&A 

[X5浏览器同层播放介绍](https://x5.tencent.com/tbs/guide/video.html)

Q：如何测试效果，确定进入了同层播放器？

A：安装新的tbs版本后，如果要测试效果，请杀掉微信进程，把系统时间往后调一天以上，再进入网页进行视频播放，如果微信的顶bar消失，进入了一个沉浸式的播放器，则是进了同层播放器。

Q：如何查看当前的的tbs版本？

A：在微信聊天窗口输入//gettbs 并发送，查看弹出的Toast上显示的tbsCoreVersion 是否等于36849 ，若是则tbs版本正确。注：这是之后进行测试的基础，这个版本一定要正确

Q：接入了同层播放器，在老版本的tbs是否会出问题？

A：对老版本不会产生影响。

Q：同层播放器在iOS上会生效吗？

A：目前的同层播放器只在Android（包括微信）上生效，暂时不支持iOS

Q：同层播放器顶部”<”和“…”按钮可以去掉吗？

A：不能

Q: 在微信TBS里如何区是否支持同层播放器

A: a)在微信等TBS里通过UA判断X5内核版本来区分,当版版本号>036849表示支持

UA示例:

Mozilla/5.0 (Linux; Android 4.4.4; OPPO R7 Build/KTU84P) AppleWebKit/537.36(KHTML, like Gecko) Version/4.0 Chrome/37.0.0.0 Mobile MQQBrowser/6.8 TBS/036849 Safari/537.36 MicroMessenger/6.3.27.861 NetType/WIFI Language/zh_CN

b)在QQ浏览器Android版本中,当浏览器版本>=7.1时开始支持

UA示例：

UserAgent: Mozilla/5.0 (Linux. U. Android 4.4.4. zhcn. OPPO R7 Build/KTU84P) AppleWebKit/537.36 (KHTML, like Gecko)Version/4.0 Chrome/37.0.0.0 MQQBrowser/7.1 Mobile Safari/537.36


