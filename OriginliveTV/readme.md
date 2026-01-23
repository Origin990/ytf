# 起源电视

Mr.zhen倾力打造的直播电视集成播控平台

一款基于云端技术融合式、支持播放流媒体的软件。

## 原项目：

1.0（感谢[lizongying](https://github.com/lizongying)提供源码）：[my-tv-0](https://github.com/lizongying/my-tv-0)

2.0（感谢[yaoxieyoulei](https://github.com/yaoxieyoulei)提供源码）：[mytv-android](https://github.com/yaoxieyoulei/mytv-android)

2.0图标的设计灵感来自这里[miyoushe](https://www.miyoushe.com/sr/article/64580342)

## 项目背景

* 发起此项目是为了弥补现代智能电视看不了直播电视的短板以及解决老年群体观看电视的种种障碍，这个项目在诞生之初，一直保持着无广告、免费、为爱发电的运营方式，探索世界的智能电视更应如此，秉着效率至上的信条，为你带来本该享受的极速观看体验。

* 本人是这个项目的负责人与管理者，在GitHub自主开发的电视集成播控平台，即取名为「起源电视」。

## 注意事项

文件中的所有直播源均来自网络。

本人仅负责将网络上的直播源进行整合，并不会对直播源中的直播内容进行安全管控。

## 使用（1.0）

* 遥控器中键/触屏单击打开视频列表
* 遥控器菜单键/触屏双击打开配置
* 遥控器左键/触屏长按打开节目单
* 遥控器返回键关闭视频列表/配置
* 在聚焦视频标题的时候，右键收藏/取消收藏
* 打开配置后，选择远程配置，扫描二维码可以配置视频源等。也可以直接远程配置地址 http://0.0.0.0:34567
* 如果视频源地址已配置，并且打开了“应用启动后更新视频源”后，应用启动后会自动更新视频源
* 默认遥控器下键/触屏下滑切换到下一个视频。换台反转打开后，逻辑相反

## 使用（2.0）

* 遥控器中键/触屏单击打开视频列表
* 遥控器中键长按/菜单键/触屏双击打开菜单
* 遥控器左键/右键切换路线（直播源文件为多路线或开启超能模式后可用）
* 遥控器返回键关闭视频列表/配置
* 遥控器中键双击唤起可优AI（暂未上线的功能，目前无法使用，敬请期待）
* 在聚焦视频标题的时候，右键打开当前频道的节目单，长按中键可收藏当前频道
* 打开更多设置后，选择推送，在页面扫描二维码可以配置视频源等。也可以直接远程配置地址 http://0.0.0.0:10481 （除非绝对必要，请勿私自修改直播源，按照默认设置即可。如果这侵犯了你的隐私，请告知我们，我们会在未来删除关于你的所有信息）
* 2.0默认开启自动更新直播源，且无法关闭。可在设置>直播源内设置直播源的缓存时间，如果视频源地址已配置，应用启动后会根据直播源缓存时间进行自动更新视频源（除非绝对必要，请勿修改此选项，按照默认设置即可。如果这侵犯了你的隐私，请告知我们，并在您的软件内的自定义直播源选项中删除所有的直播源）
* 默认遥控器下键/触屏下滑切换到下一个视频。换台反转功能打开后，逻辑相反，软件内也有相关说明。

注意：

* 不同机型可能受系统版本影响，操作方式可能不一致，请以实际情况为准
* 遇到问题可以先考虑重启/恢复默认/清除数据/重新安装等方式自助解决
* 视频源可以设置为本地文件，格式如：file:///mnt/sdcard/tmp/channels.m3u
  /channels.m3u（2.0暂未测试）
* 为了使用方便，只支持设置3位频道号
* 目前设置代理后，需要重启生效。代理属于全局代理，也就是视频请求及其他请求都会使用代理。

目前支持的配置格式：

* txt
    ```
    组名,#genre#
    标题,视频地址
    ```
* m3u
    ```
    #EXTM3U x-tvg-url=""
    #EXTINF:-1 tvg-id="" tvg-chno="" tvg-name="标准标题" tvg-logo="图标" group-title="组名",标题
    #EXTVLCOPT:http-user-agent=
    #EXTVLCOPT:http-referrer=
    视频地址
    ```
* json
    ```json
    [
      {
        "group": "组名",
        "name": "标准标题",
        "title": "标题",
        "logo": "图标",
        "number": "频道号",
        "uris": [
          "视频地址"
        ],
        "headers": {
          "user-agent": ""
        }
      }
    ]
    ```

推荐配合使用原项目的 [my-tv-server](https://github.com/lizongying/my-tv-server)

下载安装 [releases](https://github.com/Origin990/ytf/releases/tag/ytf)

我们提供安卓4.4兼容版本（2.0版本仅兼容Android5.0+系统版本）。

注意！以下内容仅作为实机演示，不代表本软件内置了初始直播源。

1.0：
![image](http://jp-proxy.gitwarp.top:3000/https://github.com/Origin990/ytf/blob/main/OriginliveTV/screenshots/MuMu-20251002-101712-513.png)
![image](http://jp-proxy.gitwarp.top:3000/https://github.com/Origin990/ytf/blob/main/OriginliveTV/screenshots/MuMu-20251002-101749-620.png)
![image](http://jp-proxy.gitwarp.top:3000/https://github.com/Origin990/ytf/blob/main/OriginliveTV/screenshots/MuMu-20251002-101810-532.png)

2.0：
![image](http://jp-proxy.gitwarp.top:3000/https://github.com/Origin990/ytf/blob/main/OriginliveTV/screenshots/2.0-1.png)
![image](http://jp-proxy.gitwarp.top:3000/https://github.com/Origin990/ytf/blob/main/OriginliveTV/screenshots/2.0-2.png)
![image](http://jp-proxy.gitwarp.top:3000/https://github.com/Origin990/ytf/blob/main/OriginliveTV/screenshots/2.0-3.png)

## 安装

从本站下载安装包到U盘，再插入到电视的任意的USB接口，打开电视上的任意文件管理器（建议使用当贝市场）进行安装。

或通过ADB进行安装：

```shell
adb install Android-5.0+.apk
```

小米电视可以使用小米电视助手进行安装。

由于小米出于安全原因，搭载TV HyperOS 2.0的电视机型不再支持APP安装功能，请使用adb方式安装。

部分电视（如海信电视）安装完成后，U盘文件会出现损坏或乱码的问题，此问题可以通过Windows自带的“查错”功能进行修复。建议使用空U盘进行安装。

## 常见问题

* 为什么远程配置视频源文本后，再次打开应用后又恢复到原来的配置？

  如果“应用启动后更新视频源”开启后，且存在视频源地址，则会自动更新，可能会覆盖已保存的视频源文本。

* 为什么我在安装时提示解析包时出现问题？

  我们在上传软件时已分为两种安卓版本，出现此问题的原因是您在Android4.4设备安装时使用了只兼容安卓5.0以上的安装包。

* 直播无法播放？

  软件是否可以正常播放直播取决于直播源，本人并不负责直播源的维护。

## 服务的变更或中止

发生下列情形之一时，开发者有权终止或中断本项目全部服务：

1. 因本项目及服务自身的需要；

2. 因突发性的软硬件设备与电子通信设备故障；

3. 因网络提供商线路或其他故障；

4. 当地政府原因或其他不可抗力的情形。

## 致谢

感谢您的支持，和我们并肩投身于创造更美好的世界，用科技改善人类生活的壮丽事业。

Mr.zhen始终尊重并珍视每一位用户，这是我们的初心也是我们的使命。我们将持续优化服务流程和机制，为用户带来更好的体验。

Mr.zhen 为你解锁 全新可能
