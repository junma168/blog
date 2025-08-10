---
title: movies
date: 2025-08-05 21:22:46
tags:
  - study
categories:
  - 教程
  - hexo
keywords: "hexo重新部署恢复"
description: ""  # 冒号后有空格
top_img:         # 保持空值格式
cover: "https://s21.ax1x.com/2025/08/05/pVUUBjO.jpg"  # URL加引号

---

📚 文档目录

🚀 快速开始 - 📑 主题页面 - 📌 主题配置 - ⚔️ 标签外挂 - ❓ 主题问答 - ⚡️ 进阶教程

你可以通过右下角的 简 按钮切换为简体显示

hexo-theme-butterfly 是基于 hexo-theme-melody 的基础上进行开发的主题。

安装
Git 安装
npm 安装
如果你身处中国大陆，且访问 Github 不稳定，你可以用 Gitee 安装
稳定版【建议】

在你的 Hexo 根目录里

POWERSHELL
1
git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly
测试版

测试版可能存在 Bugs，追求稳定的请安装稳定版

如果想要安装比较新的 dev 分支，可以

POWERSHELL
1
git clone -b dev https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly
升级方法：在主题目录下，运行 git pull


应用主题
修改 Hexo 根目录下的 _config.yml，把主题改为 butterfly

YAML
1
theme: butterfly
安装插件
如果你没有 pug 以及 stylus 的渲染器，请下载安装：

POWERSHELL
1
npm install hexo-renderer-pug hexo-renderer-stylus --save
升级建议
升级完成后，请到 Github 的 Releases 界面查看新版的更新内容。

里面有标注 _config 文件的变更内容（如有），请根据实际情况更新你的配置内容。

为了减少升级主题后带来的不便，请使用以下方法（建议，可以不做）：

在 hexo 的根目录创建一个文件 _config.butterfly.yml，并把主题目录的 _config.yml 内容复制到 _config.butterfly.yml 去。

注意:

复制的是主题的 _config.yml ，而不是 hexo 的 _config.yml

不要把主题目录的 _config.yml 删掉

以后只需要在 _config.butterfly.yml 进行配置就行。如果使用了 _config.butterfly.yml， 配置主题的 _config.yml 将不会有效果。

Hexo 会自动合併主题中的 _config.yml 和 _config.butterfly.yml 里的配置，如果存在同名配置，会使用 _config.butterfly.yml 的配置，其优先度较高。


作者: Jerry
連結: https://butterfly.js.org/posts/21cfbf15/
來源: Butterfly
版權屬於作者所有。商業用途請聯絡作者獲得授權，非商業用途請註明出處。




