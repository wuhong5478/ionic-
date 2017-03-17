# ionic集成极光推送最新教程教程
最近在做一个hybrid需要用到推送功能，网上的教程都太久远了，记录下最新版的ionic 极光推送的集成方法
1.  先去极光推送官网注册极光推送账户，并创建应用，这里最重要的一点就是**你创建的应用包名必须和ionic项目的应用包名一致**。
2.  通过 Cordova Plugins 安装，要求 Cordova CLI 5.0+，在你项目目录下运行以下代码。<br/>
        ```
        cordova plugin add jpush-phonegap-plugin --variable APP_KEY=your_jpush_appkey
        ```
        这里的your_jpush_appkey就是之前你在极光推送创建应用后分配的一个appkey，填上运行命令，安装成功。之前网上的其他教程都太久远了，需要改这改那，会被误导，
        现在最新版的插件直接运行这句命令后就ok了。
3.  前往插件github地址（https://github.com/jpush/jpush-phonegap-plugin/blob/master/README.md）查看相关ap使用。我这里为了测试只使用了最基础的一个初始化api，
  在你的ionic项目的app.js 启动推送 ```window.plugins.jPushPlugin.init()```.
4.  最后，想推送消息的时候在极光推送控制台发送消息就行了，app稍后就会收到提示。  
