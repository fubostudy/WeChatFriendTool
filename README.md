本项目[WeChatFriendTool](https://github.com/fubostudy/WeChatFriendTool)是基于Tkinter和WeChatPYAPI开发的「微信好友助手」，拥有简洁的可视化界面，可实现以下功能：

1. 登录微信，一键导出微信好友列表，并存储为Excel文件

2. 批量给微信好友发送个性化消息和图片（不同好友发送不同的信息）

3. 一键生成微信好友头像图片墙，包括方形和心形


代码详解与实现过程可查看博客：[【WeChatFriendTool】从0到1，从前端界面到后端接口，详解Python软件开发全过程。干货，看完小白也可以轻松写出一个软件！](https://ferryxie.com/archives/4160)。如果此项目对你有帮助，请动动小手给一个star🌟，感谢！

<p align="center">

<img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/075055.jpg" width="50%"/>

</p>


# 使用教程

项目目录结构如下：

```basic
├── README.md  
├── WeChatFriendTool_1.0.zip   # 软件压缩包
├── figmaDesign                # 设计稿
├── mainCode                   # 源代码
```

使用教程如下：（本软件仅适用于Windows平台，MacOS需要通过虚拟机使用）

1. 本软件依赖于3.3.0.115版本的PC微信，需要在电脑中安装此版本微信，点击下载：[WeChat 3.3.0.115](https://images-ferry.oss-cn-shenzhen.aliyuncs.com/WeChat%203.3.0.115.zip)

2. 克隆本项目到本地

3. 解压 `WeChatFriendTool_1.0.zip`, 将解压后的文件夹添加到白名单，添加方式白名单如下图所示（如果不加入白名单，dll文件会被误识别为病毒，运行软件的时候会出现`缺少依赖`的报错，本软件无毒无后台！）

<p align="center"><img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/081445.png" width="50%"/></p>


4. 双击解压后`WeChatFriendTool_1.0`文件夹下的`main.exe`即可运行程序

<p align="center"><img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/075107.jpg" width="50%"/></p>


5. 如果出现`8888端口被占用`的错误提示。首先需要强行退出软件，然后双击运行文件夹下的`pause.bat`文件即可。

<p align="center">
<img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/081956.jpg" width="50%"/>
</p>


​	
# 功能描述

1. 点击`登录微信`，并且扫码登陆微信；

<p align="center"><img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/075058.png" width="50%"/></p>


2. 点击`导出好友`，即可在文件夹中生成`friends_list.xlsx`文件，此文件包含所有微信好友的唯一识别号（wx_id）、微信昵称（nick_name）、你对此好友的备注（remark）、微信账号（_wx_account）以及微信头像图片链接（avatar_url）

<p align="center">
<img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/075059.png" width="50%"/>
<img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/082648.png" width="50%"/>
</p>


3. 发送文本消息：基于上述导出的`friends_list.xlsx`文件，可以借助备注名称和excel生成批量个性化信息。最后将要发送的信息保存到excel，再点击`上传表格`，将表格上传。
	
	需要注意的是，这里要上传的excel需要严格按照规范来，包括两列：第一列是的唯一识别号（wx_id），表示你要将信息发送给谁；第二列是要发送的信息（meg），表示你要发送什么消息。(第一行的列名命名可以随意，会从第二行开始读取；excel的文件名也可以随意)

4. 发送图片消息：这个选项是**可选**的，点击`上传图片`（建议不要图片太大，不然发送很慢或发送失败），并选择图片即可。需要注意的是，这里是给所上传的Excel文件里面的唯一识别号（wx_id）列的所有人**发送同一张图片**。如果信息和图片确认没问题后，点击发送即可。

   这里笔者以`ready.xlsx`为例进行个性化消息批量发送演示

<p align="center">
<img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/075107.png" width="50%"/>
<img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/075100.png" width="50%"/>
<img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/075109.png" width="50%"/>
</p>


5. 点击`生成好友头像照片墙`，可以生成 「正方形」 和 「心形」 两种格式的照片墙。（如果好友比较多，可能下载过程会有些缓慢）

<p align="center">
<img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/091931.png" width="50%"/>
<img src="https://images-ferry.oss-cn-shenzhen.aliyuncs.com/092101.png" width="50%"/>
</p>


