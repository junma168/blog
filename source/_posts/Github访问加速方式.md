---
title: Github访问加速方式
author: 微光
tags:
  - GitHub
categories:
  - 教程
cover: >-
  https://lz.qaiu.top/parser?url=https://cloud.189.cn/web/share?code=Afym6jJ7Bjuu（访问码：u00p）
date: 2025-09-09 00:16:52
---
最近利用hexoPro部署项目到GitHub上面总是报错，发现是GitHub链接有问题，于是在往上找到了一个方法。

# 第一步：获取 GitHub 的最新 IP 地址

通过在线DNS解析网站例如https://www.ipaddress.com/, 在`Lookup any IP Address or Website`处输入域名`github.com`,获取A记录的ip即可,如下图：

![ip获取](https://lz.qaiu.top/parser?url=https://cloud.189.cn/web/share?code=3QZr6faMr6Vz（访问码：nt7l）)
把获取到的对应IP拷贝出来

# 第二步：修改 hosts 文件

将拷贝出来的IP复制到hosts文件（文件路径为C:\Windows\System32\drivers\etc），配置为

![host修改](https://lz.qaiu.top/parser?url=https://cloud.189.cn/web/share?code=UrEfIbMvQfaq（访问码：u8ta）)
配置好后，点击保存即可。如果配置后，提示保存不了，可以复制该文件到桌面，重新配置后点击保存，然后再次复制覆盖掉原文件即可。

# 第三步：刷新 DNS 缓存

修改 hosts 文件后，需要让系统重新加载 DNS 记录才能生效。

Windows (命令提示符或 PowerShell 管理员模式):

在开始菜单搜索“cmd”或“PowerShell”。

右键点击，选择“以管理员身份运行”。

输入以下命令：
`ipconfig /flushdns`

# 第四步：测试连接

在终端或命令提示符中，使用 ping 命令测试是否生效：
`ping github.com`
如果 hosts 修改成功，你应该能看到它正在解析到你刚才手动设置的 IP 地址，并且有回复数据包。
**注意事项：**
IP 有效性：如果过一段时间后又失效了，说明 GitHub 的 IP 变了，需要重新执行第一步，获取最新 IP 并更新 hosts 文件。

备份：修改 hosts 文件前，可以先将原文件复制一份备份，以防出错。
