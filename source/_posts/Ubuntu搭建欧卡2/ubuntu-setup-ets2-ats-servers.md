---
abbrlink: ''
categories: []
date: '2024-07-23T19:03:51.693020+08:00'
tags: []
title: Ubuntu搭建欧卡2/美卡联机服务器 详细教程
updated: '2024-07-23T19:03:51.096+08:00'
---
> 此博文由[旧博客](https://web.archive.org/web/20240225235726/https://wuminboke.site)搬运，不会再回复评论！

# 正文

理论上适用於美卡和欧卡，但是本文基于欧卡，美卡请自行探索\~
两款游戏经常打折，最低价11，日常30多
高于30不建议买，另外，DLC也是建议打折再买，可以省下不少钱

## steamcmd安装

*[From](https://developer.valvesoftware.com/wiki/SteamCMD)*

```bash
sudo add-apt-repository multiverse; sudo dpkg --add-architecture i386; sudo apt update 
sudo apt install steamcmd
steamcmd
login anonymous
```

这里需要注意:
欧卡id: 1948160
美卡id: 2239530
这里以欧卡为例 `app_update 1948160`

安装后cd到游戏目录 `cd '/Steam/steamapps/common/Euro Truck Simulator 2 Dedicated Server'`

到这里，安装的部分就告一段落了

## 获取配置文件

在游戏中按\~这个键，输入`export_server_packages`
然后打开`Documents\Euro Truck Simulator 2`
找到`server_packages.dat`,`server_packages.sii`
复制到`save`内

## 启动

```
cd '/Steam/steamapps/common/Euro Truck Simulator 2 Dedicated Server/bin/linux_x64/'
chmod -xxx server_launch.sh
./server_launch.sh
```

## 公开列表

如果想让服务器公开到运联列表(默认是只能搜索数字的)
*在这部折腾好久，最后发现欧卡的搜索有点问题，我打开的选择性模组然后就搜不到啦\~*
`server_config.sii`:
确保`mods_optioning: false`不然搜不到，并且`show_server: true`打开

打开steam: [https://steamcommunity.com/dev/managegameservers](https://steamcommunity.com/dev/managegameservers)
欧卡id: 1948160
美卡id: 2239530
把获取到的key 放到`server_config.sii`: ` server_logon_token`

## 管理员

建议把自己设置为管理员
获取自己steam id的步骤:
打开steam，点击右上角用户名，在左上角标题下面那行小字就是id啦
最后在`server_config.sii`:

```xml
moderator_list: 1
 moderator_list[0]: 你的steamid
```

```*开始快乐的卡车生涯吧\~*
~~说实话tmp更好玩~~
