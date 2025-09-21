---
title: Github访问加速方式
author: 微光
tags:
  - GitHub
categories:
  - 教程
cover: >-
  https://preview.cloud.189.cn/image/imageAction?param=AC0F139CAC578D52397C33F1C2848981148718CFC0BFF7CF2F51C0B80A0CAB26B00EC09C3BD3DACC46C205AEA7272C06419D7FC5086D11DBC015521A8323CAC50E6560603C8B031A0737E889DF1B9E846E49DE65F74187A020E357FEF4474D8057328284CC3BBDFF99B3C9602F15A681769FC7DB
date: 2025-09-09 00:16:52
---
最近利用hexoPro部署项目到GitHub上面总是报错，发现是GitHub链接有问题，于是在往上找到了一个方法。

# 第一步：获取 GitHub 的最新 IP 地址

通过在线DNS解析网站例如https://www.ipaddress.com/, 在`Lookup any IP Address or Website`处输入域名`github.com`,获取A记录的ip即可,如下图：

![ip获取](https://preview.cloud.189.cn/image/imageAction?param=1237EA03A8DCC9B52BB4C983E902C0525D0751624B40B7FD357AA1070B47826ED7F3DDEB7F0C46B359C9D3C23C338378E48D57EDAA89F4FEB1D98B8E0901835438363D5E657B701197FD4272A2B29DF46FF496320762CD8AEF812E4298B392D9CD049B727BA015A2689A8EC1EB154DB6021EE25B)
把获取到的对应IP拷贝出来

# 第二步：修改 hosts 文件

将拷贝出来的IP复制到hosts文件（文件路径为C:\Windows\System32\drivers\etc），配置为

![host修改](https://preview.cloud.189.cn/image/imageAction?param=279AA11515B15C85E055435513FE818F4816517606677A10A6DA1FAFED976A24FDE34B3711E00615D9CFBF9FD266D62660C0878A1544A057FB0CC26D9BB1DC38165FB38C772A407CBE5376035135E941843229652B2D6591A796F209AE953E98A4A0176F8D7D7C41A0ED83C8AA8B1E67530DDFED)
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
