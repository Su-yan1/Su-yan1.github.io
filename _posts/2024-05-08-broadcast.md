---
layout:     post
title:      "降噪软件的使用"
subtitle:   "NVIDIA Broadcast的使用"
date:       2004-05-07 12:00:00
author:     "lateyoung"
header-img: "img/img-Broadcast.jpg"
catalog: true
tags:
    - Broadcast
---
> “降噪软件NVIDIA Broadcast的使用”

### NVIDIA Broadcast

NVIDIA Broadcast官网地址：[NVIDIA Broadcast](https://www.nvidia.cn/geforce/broadcasting/broadcast-app/)

### 主要功能

1. **声音增强：**
   - *降噪*：NVIDIA Broadcast 可以利用 AI 技术对麦克风输入进行降噪处理，消除背景噪音，使声音更加清晰。
   - *消除回声*：软件能够识别和消除音频输入中的回声，提高通信和录制的声音质量。
   - *语音增强*：NVIDIA Broadcast 可以增强用户的语音，在线通话和直播中让声音更加清晰、自然。

2. **视频增强：**
   - *虚拟背景*：软件支持虚拟背景功能，能够实时替换背景，让用户在视频通话和直播中展示不同的背景效果。
   - *人脸追踪*：NVIDIA Broadcast 可以识别和追踪用户的脸部，在视频通话和直播中保持用户的脸部始终在画面中央，提高视频质量。
   - *自动框选*：软件可以自动检测和框选用户，将用户的头像或人物从背景中分离出来，使得视频通话和直播更加专业。

3. **通用功能：**
   - *硬件加速*：NVIDIA Broadcast 利用 NVIDIA GPU 的硬件加速功能，提供更快的处理速度和更低的延迟。
   - *跨应用支持*：软件能够与主流的通讯应用（如 Zoom、Teams、Discord 等）和流媒体平台（如 Twitch、YouTube 等）无缝集成，方便用户在不同的平台上应用这些功能。

总的来说，NVIDIA Broadcast 是一款功能强大的音视频处理软件，利用 NVIDIA 的 AI 技术提供了一系列实用的声音和视频增强功能，适用于各种场景下的音视频通信、内容创作和直播。



### NVIDIA Broadcast的使用

1. 麦克风降噪

   在安装了Broadcast后，系统会默认添加一个叫做`Speakers`的输入设备，我已经设置这个设备为默认的输入设备，但是我们还需要在Broadcast中将麦克风源设置为我们之前的输入设备，通常为<font color="red">耳机型号或者麦克风型号</font>，在设置后可以点击右边的录制进行尝试，如果录制后没有声音请更换麦克风源。

   注意：

   - 如果不需要降噪功能请在Broadcast软件中将`效果`旁边的按钮取消
   - 在电脑需要使用到麦克风时，<font color="red">Broadcast软件需全程开启！</font>
   - 如果不再需要降噪软件，请在系统`程序与功能`设置中将Broadcast卸载。

   ![麦克风降噪](https://pic4.zhimg.com/80/v2-41e766edc7107fc59c9214504beeb32b_720w.webp)

2. 扬声器降噪

   没什么用，<font color="red">别开！</font>开了以后会对扬声器原本的声音进行降噪，遮盖掉包括音乐声等声音。

3. 相机功能

   在NVIDIA Broadcast的相机界面下，选择相机源之后（如我们这里选择的是C922 Pro摄像头），可以调整输出的画面分辨率和帧率，下面的效果选项栏中，可以选择想要开启的背景功能。当前的NVIDIA Broadcast版本中，为玩家提供了“背景模糊”、“背景更换”、“背景删除”和“自动聚焦”四种效果。

   ![背景删除](https://pic4.zhimg.com/80/v2-2924c2fdde0681d6931a85373f566fb7_720w.webp)

   使用背景更换功能还能在删除背景后使用自定义的图片或视频

   ![change](https://pic4.zhimg.com/80/v2-830ce9129ee4a7f063a20ab29162b5d7_720w.webp)

   背景模糊功能可以识别当前主播的人像主体，并将背景进行模糊处理，从而实现突出主体，减少杂乱背景对直播的影响，或者在纵深较低的直播环境中模拟出更强烈的背景虚化效果，实现更好的直播体验。

   ![blur](https://pic3.zhimg.com/80/v2-70164cd4fcaa67cdf02310a18fc9528e_720w.webp)



### Broadcast与OBS联动

在开启NVIDIA Broadcast的情况下，软件会生成虚拟的视频设备和音频设备。打开OBS后，点击添加“视频捕获设备”，在弹出的选项框中选择“Camera（NVIDIA Broadcast）”即可使用由NVIDIA Broadcast处理后的视频画面。如果还需要使用音频处理，那么还可以添加一个“音频输入捕获”，设备选择为“麦克风（NVIDIA Broadcast）”。

![Broadcast combine OBS](https://pic2.zhimg.com/80/v2-70d7a0042cfb8ff00bf42349bad9d109_720w.webp)

添加新的麦克风来源同样也在OBS的来源部分，点击＋号后点击音频输入采集后，选择经过Broadcast处理过的音频输入即可。

![添加音频输入设备](https://img2.imgtp.com/2024/05/09/hwl5i5x9.png)

   到这里Broadcast的常用设置和与OBS的配合使用就结束了。

   

   