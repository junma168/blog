---
title: 利用onedrive新建个人歌单
author: 微光
tags:
  - music
categories:
  - 教程
  - hexo
cover: >-
  https://preview.cloud.189.cn/image/imageAction?param=AF0B738A595F84D07C8F9E0EF5412D129FC3CECC88C594B800DE195FE24831D4D8D4926831A8F1853568DDB30D5E94EEF85258C030D30DE828F3D0CAC87B3179DDB58E1AFDE801B1A8B56F16BF71CB5993C00499A30D6879F9583B8FB9CFE3F7214F8E8FFA5E841DC19FA03AB34E94D3E87C690E
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
