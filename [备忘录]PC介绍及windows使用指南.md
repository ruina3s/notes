---
tiele: [备忘录]PC介绍及windows使用指南
date: 2022-8-6 18:49:00
tab:
---
PC介绍及windows使用指南
==

[toc]

# 0.简单说明

**PC**：personal computer，个人电脑

本文将记录我个人使用PC过程中遇到的硬件和软件相关问题的解决，及相关使用推荐，由于个人学习不足，硬件仅做少量介绍



# 1.硬件部分

本部分由于自身能力不足以说明清除，故推荐一课程[计算机科学速成课](https://www.bilibili.com/video/BV1EW411u7th)

该课程较具体的说明计算机知识，对于入门非常有帮助



# 待处理

+ [BV1TZ4y1o7c5](https://www.bilibili.com/video/BV1TZ4y1o7c5)
+ [精选软件 (qq.com)](https://mp.weixin.qq.com/s/OenLyfGjWPd1QgQ7c6X8sQ)



win11激活：（power shell）irm https://get.activated.win | iex

# 暂分类

### 1.上帝模式

**新建文件夹**后重命名为

```
GodMode.{ED7BA470-8E54-465E-825C-99712043E01C}
```



### 2.创建新桌面（虚拟）

<kbd>win</kbd>+<kbd>tab</kbd>、<kbd>win</kbd>+<kbd>crtl</kbd>+<kbd>D</kbd>即可，<kbd>win</kbd>+<kbd>crtl</kbd>+<kbd>←</kbd>/<kbd>→</kbd>可左右切换



### 3.微软输入法

u模式、v模式



### 4.windows sandbox



### 5.高级状态栏

<kbd>win</kbd>+<kbd>G</kbd>



### 6.bt下载器

qBittorrent 增强版 https://github.com/c0re100/qBittorrent-Enhanced-Edition/releases

Tracker Lists https://github.com/XIU2/TrackersListCollection/blob/master/README-ZH.md



### 7.迅雷极限精简版



### 8.vs code插件

<kbd>ctrl</kbd>+<kbd>/</kbd>为注释的快捷键

+ Chinese (Simplified)Language Pack for Visual Studio Code

+ 翻译(英汉词典)

+ Code Spell Checker

+ 搜索theme可获取主题

+ Material lcon Theme(图标主题)

+ vscode-icons(官方图标主题)

+ sqltools（数据库管理）[BV1Zq4y1F7iA](https://www.bilibili.com/video/BV1Zq4y1F7iA)



### 9.录屏软件

+ Xbox game bar(<kbd>win</kbd>+<kbd>G</kbd>)
+ Nvidia Experience（**推荐**）
+ obs(steam上有免费版)
+ captura(需要ffmpeg解码器)
+ bandicam





### 10.PowerToys



### 11.steam软件

+ VTube Studio（VTube直播用，有脸部捕捉）
+ VRoid Studio（通过2D绘图建立3D模型）
+ RPG Maker
+ ShareX（截图、录屏、文字识别、加水印等）
+ Boom 3D
+ 3D Mark（电脑性能测试）



### 12.DroidCam

手机虚拟出电脑的摄像头和麦克风



### 13.加密（[灵梦御所]([关于新使用的加密软体Encrypto - 灵梦广场 (acg.is)](https://acg.is/d/10905-encrypto))）

**一、WinCrypt（旧型）解码操作手册：**
1、选择蓝色“open”图标，选取已经下载完整的本体。
**注意：虽然本体文件为DAT文件，但是因为Wincrypt的规则文件是无后缀名的**
2.此时会弹出输入密码的窗口，请在窗口中的两行输入栏中输入密码。
3.此时解码器开始工作，如果密码正确，文件会在主窗口的下方任务栏中显示文件；如果密码错误，软体将自动关闭。
4.如果解码成功，“Encrypt”图标旁边的“Decrypt...”图标会变为可点击状态，此时可以开始解码。
5.选择好路径，开始解码。
**注意：WinCrypt多数情况下不支持非英文及阿拉伯数字路径，请尽可能选择英文和阿拉伯数字路径。**
6.解码进度窗口出现，根据文件的大小，解码事件有些许不同。
**注意：如果解码器在运行过程开始时崩溃，为路径错误，请按条例5的注意项更换路径；如果在中途崩溃，则为运算时内存溢出导致的崩溃，这种情况请减少内存的消耗再解码。**

二、Encrypto（新型）解码操作手册：

下载：https://macpaw.com/encrypto
1.下载Encrypto并确保安装成功。
2.下载完成末尾编号为JS的文件，并对下载后的本体进行修改后缀，后缀为.crypto。然后如果文件图标变为和Encrypto软体图标颜色相近的图标，则表示文件修改成功。
3.此时可以双击文件，会进入Encrypto的输入密码界面，请在此处输入密码。
**注意：Encrypto不支持除阿拉伯数字和英文以外的密码，所以密码绝对不可能包含标点符号、中文字符或者是特殊字符，所以请查询文字段的密码，详细可以看介绍文的加粗部分。**
4.输入密码后，如果密码正确，文件会继续解码，如果错误，会发生错误强制关闭。
5.解码完成后点击窗口下方“Save as”按钮，选择路径保存文件本体（多数情况支持中文路径）。
**注意：两种加密软体的算法完全不一样，所以二者不能相互解码！请确保自己使用的是正确的解码器！**

密码使用的是**游戏王OCG卡片密码**，查卡：https://www.ourocg.cn/



### 14.关闭移动驱动器自启动

控制面板-硬件和声音-自动播放



### 15.ffmpeg使用

下载网站：[ffmpeg](https://ffmpeg.org/)

![image-20220913092549040](https://raw.githubusercontent.com/ruina3s/imgs/main/image-20220913092549040.png)

下载后得到的压缩包解压，并按需求放置于固定位置，并记录以下文件所处路径

![image-20220913092901415](https://raw.githubusercontent.com/ruina3s/imgs/main/image-20220913092901415.png)

打开“控制面板”-“用户账户”-“更改我的环境变量”进行配置

![image-20220913093105618](https://raw.githubusercontent.com/ruina3s/imgs/main/image-20220913093105618.png)

在path项中增加刚才的文件路径，通过命令行输入ffmpeg -version来检测是否配置完成

![image-20220913093253962](https://raw.githubusercontent.com/ruina3s/imgs/main/image-20220913093253962.png)



视频压缩

```shell
ffmpeg  -i [input] -b:v [bps] -r [hz] [output]
[input] 需要压缩的视频的全路径及文件名
[bps] 视频压缩后的比特率，800k-700k算是极限，更底将会开始糊掉
[hz] 视频的帧率
[output] 压缩后的视频的存放路径
```



音视频合并

```shell
ffmpeg -i video.m4s -i audio.m4s -codec copy xxxx.mp4
```



文件格式判断

```shell
ffprobe -show_format xxxx.xxx
# ffprobe是ffmpeg工具的一个组件
```





### 16.游览器app模式（网页以app形式打开）

创建游览器的快捷方式在后面添加

```
--app="[link]" [link] 为要以app模式打开的网页链接，不能以/作为结尾
```

也开在edge游览器中找到**应用**选项自行添加



### 17.GitHub使用

[GitHub Desktop](https://desktop.github.com/)：GitHub的桌面操作版，不需使用git命令，不过最好还是了解git与GitHub的使用原理再使用



**GitHub单文件或目录（文件夹）下载**：

如果使用的游览器是chrome为内核的游览器安装插件：

**GitZip for github**：使用后文件或目录前出现勾选框，勾选后在网页上选择该图标下载

![image-20221010164542288](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20221010164542288.png)

![image-20221010164643736](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20221010164643736.png)

注：打开库若无勾选框可刷新页面再看是否出现



文件夹下载：

安装油猴脚本： [在线下载Github仓库文件夹 (greasyfork.org)](https://greasyfork.org/zh-CN/scripts/411834-download-github-repo-sub-folder)



单文件下载：

安装游览器扩展：**Enhanced GitHub**（使用方法参考扩展安装页，需要设置令牌）





### 18.Cheat Engine

[www.**cheatengine**.org](http://www.baidu.com/link?url=TvE5YLY459KGXtGdOM0kkvCYklWBJe3D5ta-5MxjLcJAaDkQIPEQRB1i2aLDaewZ)

中文包

![image-20221024094112623](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20221024094112623.png)



### 19.磁力链接前缀

```
magnet:?xt=urn:btih:
```



### 20.搜索引擎使用技巧

在搜索引擎输入框中输入关键词后空格输入下列内容完成目标

1. 去广告搜索
   『intitle:（关键词）』

2. 限定文件类型
   『（关键词）filetype:（文件类型）』
   ＊常见文件类型:
   〔pdf〕PDF文件
   〔xls〕:excle文件
   〔ppt〕:powerpoint文件
   〔doc〕:word文件
   〔txt〕:文本文档.

3. 关键词包含在正文中
   『intext:（关键词）』

4. 限定搜索网站
   『（关键词）inurl:（网站类型）』
   ＊常见网站类型
   〔.com〕商业组织和公司。
   〔.net〕网络服务商。
   〔.gov〕政府部门。
   〔.org〕非营利性组织。
   〔.int〕国际组织。
   〔.edu〕教育部门。

5. 限定某一网站

   『（关键词） site:xxx.com』 

6. 限定搜索时间
   如需搜索2018-2019年
   『2018..2019』
   即『（开始时间）..（结束时间）』

注：以上搜索方式可复合使用



### 21.Hyper-V服务

在 控制面板->程序->启用或关闭Windows功能内 打开或关闭Hyper-V服务

并在关闭时运行命令

```
bcdedit /set hypervisorlaunchtype off
```


打开时运行命令

```
bcdedit /set hypervisorlaunchtype Auto
```



### 22.edge游览器插件dark_reader设置

![dark_reader设置](https://raw.githubusercontent.com/ruinasS/imgs/main/dark_reader%E8%AE%BE%E7%BD%AE.png)



### 23.技能树

![cs skill tree](https://raw.githubusercontent.com/ruinasS/imgs/main/cs%20skill%20tree.png)



### 24.word插件

axmath：支持latex



### 25.步骤记录器（win10功能）

搜索psr



### 26.任务计划程序（win10功能）



### 27.自解压文件向导工具

IExpress Wizard，搜索“iexpress”

打包cab，制作安装程序的小工具



### 28.DirectX诊断工具

搜索运行“dxdiag”



### 29.恶意软件删除工具

搜索运行“mrt”



### 30.更换电脑磁盘图标

在磁盘根目录下新建一文件：autorun.inf

输入：

```
[autorun]
icon=xxx.ico (你要换的图标文件名，文件放在目录内)
```



### 31.更换电脑文件夹默认图标

Windows搜索 registry ，或者WIN+R输入regedit

输入下面这个路径：

```
Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer 
```

在Shell Icons文件夹下，右键new -> string value. 命名为 2.  重复一次命名为 3.

找到想替换的图标路径位置，复制路径

右键 2. 选择修改数据，把ico路径填进去，3.的值也如此

重启文件资源管理器



### 32.IObit Unlocker

解除文件、目录、磁盘、移动U盘的占用锁定，并告知锁定的程序进程名

[IObit Unlocker](https://www.iobit.com/en/iobit-unlocker.php#)



### 33.FL studio





### 34.自定义开机自启动

win+r开启运行界面，输入：`Shell:Startup`，在打开的**启动**文件夹中放入自己想要开机后启动的程序或快捷方式



### 35.QuickLook



### 36.Adobe Photoshop Express



### 37.FluentCast



### 38.摸鱼/Loaf



### 39.修改系统应用安装位置

设置/系统/存储/更改新内容的保存位置



### 40.windows娘主题



### 41.edge 展台模式数字/交互式标牌（打开就全屏）

```url
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

缺点：不可按<kbd>f11</kbd>退出

参考：[配置 Microsoft Edge 展台模式 | Microsoft Learn](https://learn.microsoft.com/zh-cn/deployedge/microsoft-edge-configure-kiosk-mode)

个人示例：

```
"C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" --kiosk C:\Users\XXX\Desktop\test.html --edge-kiosk-type=fullscreen3

"C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" --kiosk https://chat.openai.com --edge-kiosk-type=fullscreen
```



### 42.压缩包变图片

做好压缩包，选择好图片，在cmd命令行中

```shell
copy /b 图片路径\图片名.后缀+压缩包文件路径\压缩包文件名.后缀 输出图片路径\输出图片名.后缀
```

示例：

![image-20230607170157144](https://raw.githubusercontent.com/ruina3s/imgs/main/image-20230607170157144.png)



### 43.TrID  

分析文件类型，示例：

```shell
 C:\TrID>trid c:\Download\AvBatEx.bav

 TrID/32 - File Identifier v2.24 - (C) 2003-16 By M.Pontello

 Collecting data from file: f:\Download\AvBatEx.bav
 Definitions found: 5702
 Analyzing...

  75.8% (.BAV) The Bat! Antivirus plugin (187530/5/21)
  15.2% (.EXE) Win32 Executable MS Visual C++ (generic) (37706/45/16) 
   4.3% (.EXE) Win32 Executable Generic (10527/13/4)
   3.1% (.DLL) Win32 Dynamic Link Library (generic) (7600/42/2)
   0.8% (.EXE) Generic Win/DOS Executable (2002/3)
```



### 44.图标变白重建

ie4uinit.exe -show

- 在 **Windows 10 和 Windows 11** 系统中，你应该使用 `-show` 参数。
- 在 **Windows 7 及更早版本**的系统中，则可能需要使用 `-ClearIconCache` 参数



# 问题处理

B站：[BV1iT4y1D7nZ](https://www.bilibili.com/video/BV1iT4y1D7nZ)