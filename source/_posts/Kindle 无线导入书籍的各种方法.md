---
abbrlink: ''
categories: []
date: '2024-07-28T16:24:15.442786+08:00'
tags: []
title: Kindle 无线导入书籍的各种方法
updated: '2024-07-28T16:45:24.015+08:00'
---
*注意:本文是基于你已越狱Kindle并阅读第三方漫画的情况下!*

## Send to Kindle

*用Send2Kindle必须先注册Kindle!*

### 优却点

缺点:

- 不支持.mobi格式
- 网页版最高200MB/文件，邮件最高50MB/文件

优点:

- 可以自动把不支持的.epub格式转换成Kindle支持的格式
- 导入后可以显示在桌面
- 自带5GB云储存(好像是)

### 教程

#### 网页版

打开 [amazon.com/sendtokindle](https://amazon.com/sendtokindle)
即可直接上传书籍

#### 邮件

邮件的设置则比较麻烦，需要打开Amazon帐号对应的地区来设置
比如我的帐号是英国区，所以要打开[amazon.co.uk/hz/mycd/myx](https://amazon.co.uk/hz/mycd/myx)
点击上方的Preferences>Personal Document Settings>Approved Personal Document E-mail List
这里选择Add a new approved e-mail address
这里添加邮箱白名单

添加后回去上面的Send-to-Kindle E-Mail Settings
可以看到Kindle的邮箱，这个邮箱就是用于传书的
把书籍作为附件发送到这个邮箱，在Kindle下次联网后就会自动下载了

## KOReader

*使用KOReader前必须越狱!*

### 优却点

缺点:

- 书籍不显示在桌面

优点:

- 有多种传书方式
- 对PDF格式支持较好

### 教程

#### WebDAV/FTP/Dropbox

打开KOReader，下滑菜单>扳手按钮>云端储存>加号
可以选择WebDAV/FTP/Dropbox
输入服务器后点击名称就能打开目录啦
![](https://bu.dusays.com/2024/07/28/66a6178cb8096.jpg)

#### Calibre

打开Calibre>连线与分享>启动无线装置连线
![](https://bu.dusays.com/2024/07/28/66a61a2ef1ed4.jpg)

打开KOReader，下滑菜单>扳手按钮>Calibre>无线设定>服务器地址
![](https://bu.dusays.com/2024/07/28/66a61b0faf40a.jpg)
填入服务器的IP地址，端口默认9090

选择需要传的书，传送到装置
![](https://bu.dusays.com/2024/07/28/66a61be076179.jpg)

完，下次说怎么找书

