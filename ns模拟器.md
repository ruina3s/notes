---
title: ns模拟器
date: 2024-1-22 12:30:00
tab:
---

# NS模拟器使用

Nintendo switch游戏模拟器目前较常见的有两款

![image-20240122172508697](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20240122172508697.png)

此处仅记录个人在使用的YUZU模拟器相关内容

[toc]



## 安装

YUZU的官网[yuzu - Nintendo Switch Emulator (yuzu-emu.org)](https://yuzu-emu.org/)

也可以直接去YUZU在GitHub的项目下载安装[yuzu-emu/yuzu-mainline (github.com)](https://github.com/yuzu-emu/yuzu-mainline)



## 使用

下载好switch游戏后，打开模拟器选择你游戏放的位置**添加游戏目录**

![image-20240122173640469](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20240122173640469.png)



## 游戏相关

 YUZU模拟器只能识别格式为**xci**、以及**nsp**的游戏文件，若下载到格式为**nsz**的游戏，需要使用**SAK**这个软件进行转换（实际为游戏文件解密）

![image-20240122173910897](https://raw.githubusercontent.com/ruinasS/imgs/main/image-20240122173910897.png)

使用该软件也有需要注意的部分，你需要去下载最新的**prod.keys**与**title.keys**文件放到该软件目录下的**bin**文件夹内

注：若游戏越新，那么这两个文件越需要下载最新，否则软件无法对游戏文件进行转换
