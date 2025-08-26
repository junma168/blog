---
title: 利用onedrive新建个人歌单
author: 微光
tags:
  - music
categories:
  - 教程
  - hexo
cover: >-
  https://dlink.host/1drv/aHR0cHM6Ly8xZHJ2Lm1zL2kvYy9mNzAwYmM1NGU3YTk2MWQ1L0VaYkF4VW53U0lOR2htQVptbE9IajUwQjhTbVB6WW9fTlowa196RXd0Ry1YbFE_ZT1kemtCeHI.png
date: 2025-08-26 21:16:07
---
{% note modern %}由于各大音乐网站有vip限制，无法集成vip音乐到博客当中，但可以想一个折中的方法，可以利用OneDrive将歌曲存入，分享，然后利用直链工具即可。{% endnote %}

# 音乐下载

有会员的可去各大音乐平台下载。没有的自行想办法

# 歌词下载

[myfreemp3 音乐官网-mp3 歌曲免费下载-myfreemp3 在线音乐免费下载官网-歌曲下载-myfreemp3 app 官网下载](https://www.myfreemp3.com.cn/)

# 共享音乐

首先在本地OneDrive文件夹中将需要的音乐选中，右键-共享-复制链接

# 直链转换

打开浏览器，输入[直链工具网址]([OneDrive 网盘永久外链地址生成工具 OneDrive 直链在线生成 | Gimhoy Studio](https://onedrive.gimhoy.com/))将刚刚复制的链接填入，选择转换格式，点击获取即可获取永久直链。

# 博客配置

将安知鱼主题博客打开，找到music.json，将刚刚获得的直链填入即可

# 歌词跨域解决方案

由于歌词.lrc文件我在使用的时候发现跨域问题，暂时可用CORS 代理（临时解决方案）

``https://api.codetabs.com/v1/proxy?quest=你的直链URL``

**注意**：代理服务可能不稳定，仅建议用于开发测试。
