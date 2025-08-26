---
title: 安知鱼主题标签 Tag Plugins
author: 微光
tags:
  - anzhiyu
categories:
  - 教程
  - hexo
cover: https://s21.ax1x.com/2025/08/05/pVUDsDf.jpg
date: 2025-08-21 14:58:15
---
[安知鱼主题标签 Tag Plugins | 安知鱼](https://blog.anheyu.com/posts/d50a.html)

## 段落文本 p

{% tabs Unique name, 3 %}

<!-- tab 标签语法 -->

```
{% p 样式参数(参数以空格划分), 文本内容 %}
```

<!-- endtab -->

<!-- tab 配置参数 -->

1. 字体: logo, code
2. 颜色: {% span red, red%}、{% span yellow,yellow%}、{% span green,green%}、{% span cyan,cyan%}、{% span blue,blue%}、{% span gray,gray%}
3. 大小: small, h4, h3, h2, h1, large, huge, ultra
4. 对齐方向: left, center, right

<!-- endtab -->

<!-- tab 样式预览 -->

- 彩色文字
  在一段话中方便插入各种颜色的标签，包括：{% p red, 红色 %}、{% p yellow, 黄色 %}、{% p green, 绿色 %}、{% p cyan, 青色 %}、{% p blue, 蓝色 %}、{% p gray, 灰色 %}。
- 超大号文字
  文档「开始」页面中的标题部分就是超大号文字。
  {% p center logo large, Volantis %}
  {% p center small, A Wonderful Theme for Hexo %}

<!-- endtab -->

<!-- tab 示例源码 -->

```
- 彩色文字
  在一段话中方便插入各种颜色的标签，包括：{% p red, 红色 %}、{% p yellow, 黄色 %}、{% p green, 绿色 %}、{% p cyan, 青色 %}、{% p blue, 蓝色 %}、{% p gray, 灰色 %}。
- 超大号文字
  文档「开始」页面中的标题部分就是超大号文字。
  {% p center logo large, Volantis %}
  {% p center small, A Wonderful Theme for Hexo %}
```

<!-- endtab -->

{% endtabs %}

---

## 行内文本 span

{% tabs Unique name, 3 %}

<!-- tab 标签语法 -->

```
{% span 样式参数(参数以空格划分), 文本内容 %}
```

<!-- endtab -->

<!-- tab 配置参数 -->

1. 字体: logo, code
2. 颜色:  {% span red, red%}、{% span yellow,yellow%}、{% span green,green%}、{% span cyan,cyan%}、{% span blue,blue%}、{% span gray,gray%}
3. 大小: small, h4, h3, h2, h1, large, huge, ultra
4. 对齐方向: left, center, right

<!-- endtab -->

<!-- tab 样式预览 -->

- 彩色文字
  在一段话中方便插入各种颜色的标签，包括：{% span red, 红色 %}、{% span yellow, 黄色 %}、{% span green, 绿色 %}、{% span cyan, 青色 %}、{% span blue, 蓝色 %}、{% span gray, 灰色 %}。
- 超大号文字
  文档「开始」页面中的标题部分就是超大号文字。
  {% span center logo large, Volantis %}
  {% span center small, A Wonderful Theme for Hexo %}

<!-- endtab -->

<!-- tab 示例源码 -->

```
- 彩色文字
  在一段话中方便插入各种颜色的标签，包括：{% span red, 红色 %}、{% span yellow, 黄色 %}、{% span green, 绿色 %}、{% span cyan, 青色 %}、{% span blue, 蓝色 %}、{% span gray, 灰色 %}。
- 超大号文字
  文档「开始」页面中的标题部分就是超大号文字。
  {% span center logo large, Volantis %}
  {% span center small, A Wonderful Theme for Hexo %}
```

<!-- endtab -->

{% endtabs %}

---

## 行内文本样式 text

{% tabs Unique name, 2%}

<!-- tab 标签语法 -->

```
{% u 文本内容 %}
{% emp 文本内容 %}
{% wavy 文本内容 %}
{% del 文本内容 %}
{% kbd 文本内容 %}
{% psw 文本内容 %}
```

<!-- endtab -->

<!-- tab 样式预览 -->

1. 带 {% u 下划线 %} 的文本
2. 带 {% emp 着重号 %} 的文本
3. 带 {% wavy 波浪线 %} 的文本
4. 带 {% del 删除线 %} 的文本
5. 键盘样式的文本 {% kbd command %} + {% kbd D %}
6. 密码样式的文本：{% psw 这里没有验证码 %}

<!-- endtab -->

<!-- tab 示例源码 -->

```
1. 带 {% u 下划线 %} 的文本
2. 带 {% emp 着重号 %} 的文本
3. 带 {% wavy 波浪线 %} 的文本
4. 带 {% del 删除线 %} 的文本
5. 键盘样式的文本 {% kbd command %} + {% kbd D %}
6. 密码样式的文本：{% psw 这里没有验证码 %}
```

<!-- endtab -->

{% endtabs %}

## 分栏 tab

{% note info simple %}分栏支持内置阿里图标，如果开启了 `fontawesome`可以使用 fontawesome 的图标，否则只能使用默内置阿里图标{% endnote %}

{% tabs Unique name, 3 %}

<!-- tab 标签语法 -->

```
{% tabs Unique name, [index] %}

<!-- tab [Tab caption] [@icon] -->

Any content (support inline tags too).

<!-- endtab -->

{% endtabs %}
```

<!-- endtab -->

<!-- tab 配置参数 -->

1. Unique name :
   - 选项卡块标签的唯一名称，不带逗号。
   - 将在#id 中用作每个标签及其索引号的前缀。
   - 如果名称中包含空格，则对于生成#id，所有空格将由破折号代替。
   - 仅当前帖子/页面的 URL 必须是唯一的！
2. [index]:
   - 活动选项卡的索引号。
   - 如果未指定，将选择第一个标签（1）。
   - 如果 index 为-1，则不会选择任何选项卡。
   - 可选参数。
3. [Tab caption]:
   - 当前选项卡的标题。
   - 如果未指定标题，则带有制表符索引后缀的唯一名称将用作制表符的标题。
   - 如果未指定标题，但指定了图标，则标题将为空。
   - 可选参数。
4. [@icon]: - FontAwesome 图标名称（全名，看起来像“ fas fa-font”） - 可以指定带空格或不带空格； - 例如’Tab caption @icon’ 和 ‘Tab caption@icon’. - 可选参数。

<!-- endtab -->

<!-- tab 样式预览 -->

{% note primary simple %}Demo 1 - 预设选择第一个【默认】{% endnote %}

{% tabs test1 %}

<!-- tab -->

**This is Tab 1.**

<!-- endtab -->

<!-- tab -->

**This is Tab 2.**

<!-- endtab -->

<!-- tab -->

**This is Tab 3.**

<!-- endtab -->

{% endtabs %}

{% note primary simple %}Demo 2 - 预设选择 tabs{% endnote %}

{% tabs test2, 3 %}

<!-- tab -->

**This is Tab 1.**

<!-- endtab -->

<!-- tab -->

**This is Tab 2.**

<!-- endtab -->

<!-- tab -->

**This is Tab 3.**

<!-- endtab -->

{% endtabs %}

{% note primary simple %}Demo 3 - 没有预设值{% endnote %}

{% tabs test3, -1 %}

<!-- tab -->

**This is Tab 1.**

<!-- endtab -->

<!-- tab -->

**This is Tab 2.**

<!-- endtab -->

<!-- tab -->

**This is Tab 3.**

<!-- endtab -->

{% endtabs %}

{% note primary simple %}Demo 4 - 自定义 Tab 名 + 只有 icon + icon 和 Tab 名{% endnote %}

{% tabs test4 %}

<!-- tab 第一个Tab -->

**tab 名字为第一个 Tab**

<!-- endtab -->

<!-- tab @fab fa-apple-pay -->

**只有图标 没有 Tab 名字**

<!-- endtab -->

<!-- tab 炸弹@fas fa-bomb -->

**名字+icon**

<!-- endtab -->

{% endtabs %}

<!-- endtab -->

<!-- tab 示例源码 -->

{% note primary simple %}Demo 1 - 预设选择第一个【默认】{% endnote %}

```
{% tabs test1 %}

<!-- tab -->

**This is Tab 1.**

<!-- endtab -->

<!-- tab -->

**This is Tab 2.**

<!-- endtab -->

<!-- tab -->

**This is Tab 3.**

<!-- endtab -->

{% endtabs %}
```

{% note primary simple %}Demo 2 - 预设选择 tabs{% endnote %}

```
{% tabs test2, 3 %}

<!-- tab -->

**This is Tab 1.**

<!-- endtab -->

<!-- tab -->

**This is Tab 2.**

<!-- endtab -->

<!-- tab -->

**This is Tab 3.**

<!-- endtab -->

{% endtabs %}
```

{% note primary simple %}Demo 3 - 没有预设值{% endnote %}

```
{% tabs test3, -1 %}

<!-- tab -->

**This is Tab 1.**

<!-- endtab -->

<!-- tab -->

**This is Tab 2.**

<!-- endtab -->

<!-- tab -->

**This is Tab 3.**

<!-- endtab -->

{% endtabs %}
```

{% note primary simple %}Demo 4 - 自定义 Tab 名 + 只有 icon + icon 和 Tab 名{% endnote %}

```
{% tabs test4 %}

<!-- tab 第一个Tab -->

**tab 名字为第一个 Tab**

<!-- endtab -->

<!-- tab @fab fa-apple-pay -->

**只有图标 没有 Tab 名字**

<!-- endtab -->

<!-- tab 炸弹@fas fa-bomb -->

**名字+icon**

<!-- endtab -->

{% endtabs %}
```

<!-- endtab -->

{% endtabs %}

---

## 按钮 btns

{% tabs Unique name, 3 %}

<!-- tab 标签语法 -->

```
{% btns 样式参数 %}
{% cell 标题, 链接, 图片或者图标 %}
{% cell 标题, 链接, 图片或者图标 %}
{% endbtns %}
```

<!-- endtab -->

<!-- tab 配置参数 -->

1. 圆角样式：rounded, circle
2. 增加文字样式：可以在容器内增加 `<b>标题</b>` 和 `<p>描述文字</p>`
3. 布局方式：
   默认为自动宽度，适合视野内只有一两个的情况。


   | **参数** | **含义**                               |
   | -------- | :------------------------------------- |
   | wide     | 宽一点的按钮                           |
   | fill     | 填充布局，自动铺满至少一行，多了会换行 |
   | center   | 居中，按钮之间是固定间距               |
   | around   | 居中分散                               |
   | grid2    | 等宽最多 2 列，屏幕变窄会适当减少列数  |
   | grid3    | 等宽最多 3 列，屏幕变窄会适当减少列数  |
   | grid4    | 等宽最多 4 列，屏幕变窄会适当减少列数  |
   | grid5    | 等宽最多 5 列，屏幕变窄会适当减少列数  |

<!-- endtab -->

<!-- tab 样式预览 -->

1. 如果需要显示类似「团队成员」之类的一组含有头像的链接：

   {% btns circle grid5 %}
   {% cell xaoxuu, https://xaoxuu.com, https://bu.dusays.com/2023/06/01/64787e6a5816d.png %}
   {% cell xaoxuu, https://xaoxuu.com, https://bu.dusays.com/2023/06/01/64787e6a5816d.png %}
   {% cell xaoxuu, https://xaoxuu.com, https://bu.dusays.com/2023/06/01/64787e6a5816d.png %}
   {% cell xaoxuu, https://xaoxuu.com, https://bu.dusays.com/2023/06/01/64787e6a5816d.png %}
   {% cell xaoxuu, https://xaoxuu.com, https://bu.dusays.com/2023/06/01/64787e6a5816d.png %}
   {% endbtns %}

   2.或者含有图标的按钮

   {% btns rounded grid5 %}
   {% cell 下载源码, /, anzhiyufont anzhiyu-icon-bolt %}
   {% cell 查看文档, /, anzhiyufont anzhiyu-icon-book %}
   {% endbtns %}

   3.圆形图标 + 标题 + 描述 + 图片 + 网格 5 列 + 居中

{% btns circle center grid5 %}
<a href='https://apps.apple.com/cn/app/heart-mate-pro-hrm-utility/id1463348922?ls=1' class="no-text-decoration">
<i class='anzhiyufont anzhiyu-icon-heartbeat'></i>
<b>心率管家</b>
{% p red, 专业版 %}
<img src='https://s21.ax1x.com/2025/08/12/pVwksIJ.jpg'>
</a>
<a href='https://apps.apple.com/cn/app/heart-mate-lite-hrm-utility/id1475747930?ls=1' class="no-text-decoration">
<i class='anzhiyufont anzhiyu-icon-heartbeat'></i>
<b>心率管家</b>
{% p green, 免费版 %}
<img src='./../../../Imagebackup/pVBXpLj.jpg'>
</a>
{% endbtns %}

<!-- endtab -->

<!-- tab 示例源码 -->

1.如果需要显示类似「团队成员」之类的一组含有头像的链接：

```
{% btns circle grid5 %}
{% cell xaoxuu, https://xaoxuu.com, https://bu.dusays.com/2023/06/01/64787e6a5816d.png %}
{% cell xaoxuu, https://xaoxuu.com, https://bu.dusays.com/2023/06/01/64787e6a5816d.png %}
{% cell xaoxuu, https://xaoxuu.com, https://bu.dusays.com/2023/06/01/64787e6a5816d.png %}
{% cell xaoxuu, https://xaoxuu.com, https://bu.dusays.com/2023/06/01/64787e6a5816d.png %}
{% cell xaoxuu, https://xaoxuu.com, https://bu.dusays.com/2023/06/01/64787e6a5816d.png %}
{% endbtns %}
```

2.或者含有图标的按钮

```
{% btns rounded grid5 %}
{% cell 下载源码, /, anzhiyufont anzhiyu-icon-bolt %}
{% cell 查看文档, /, anzhiyufont anzhiyu-icon-book %}
{% endbtns %}
```

3.圆形图标 + 标题 + 描述 + 图片 + 网格 5 列 + 居中

```
{% btns circle center grid5 %}
<a href='https://apps.apple.com/cn/app/heart-mate-pro-hrm-utility/id1463348922?ls=1' class="no-text-decoration">
<i class='anzhiyufont anzhiyu-icon-heartbeat'></i>
<b>心率管家</b>
{% p red, 专业版 %}
<img src='https://s21.ax1x.com/2025/08/12/pVwksIJ.jpg'>
</a>
<a href='https://apps.apple.com/cn/app/heart-mate-lite-hrm-utility/id1475747930?ls=1' class="no-text-decoration">
<i class='anzhiyufont anzhiyu-icon-heartbeat'></i>
<b>心率管家</b>
{% p green, 免费版 %}
<img src='https://s21.ax1x.com/2025/08/20/pVBXpLj.jpg'>
</a>
{% endbtns %}
```

<!-- endtab -->

{% endtabs %}

---

## 按钮 btn

{% tabs Unique name, 3 %}

<!-- tab 标签语法 -->

```
{% btn [url],[text],[icon],[color] [style] [layout] [position] [size] %}

[url] : 链接
[text] : 按钮文字
[icon] : [可选] 图标
[color] : [可选] 按钮背景顔色(默认 style 时）
按钮字体和边框顔色(outline 时)
default/blue/pink/red/purple/orange/green
[style] : [可选] 按钮样式 默认实心
outline/留空
[layout] : [可选] 按钮佈局 默认为 line
block/留空
[position] : [可选] 按钮位置 前提是设置了 layout 为 block 默认为左边
center/right/留空
[size] : [可选] 按钮大小
larger/留空
```

<!-- endtab -->

<!-- tab 配置参数 -->


| 参数     | 含义                                                                                                       |
| -------- | ---------------------------------------------------------------------------------------------------------- |
| url      | 链接                                                                                                       |
| text     | 按钮文字                                                                                                   |
| icon     | [可选] 图标，如果开启了`fontawesome`可以使用 fontawesome 的图标，否则只能使用默内置图标                    |
| color    | [可选] 按钮背景顔色(默认 style 时）按钮字体和边框顔色(outline 时)default/blue/pink/red/purple/orange/green |
| style    | [可选] 按钮样式 默认实心数，outline/留空                                                                   |
| layout   | [可选] 按钮佈局 默认为 line block/留空                                                                     |
| position | [可选] 按钮位置 前提是设置了 layout 为 block 默认为左边 center/right/留空数                                |
| size     | [可选] 按钮大小 larger/留空                                                                                |

<!-- endtab -->

<!-- tab 样式预览 -->

1. 一组按钮

   This is my website, click the button {% btn 'https://blog.anheyu.com/',AnZhiYu %}
   This is my website, click the button {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right %}
   This is my website, click the button {% btn 'https://blog.anheyu.com/',AnZhiYu,,outline %}
   This is my website, click the button {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline %}
   This is my website, click the button {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,larger %}
2. 调整位置/大小

   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,block %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,block center larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,block right outline larger %}
3. more than one button in center

   <span>
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,blue larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,pink larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,red larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,purple larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,orange larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,green larger %}
   </span>
4. 居中按钮

   <div class="btn-center">
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline blue larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline pink larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline red larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline purple larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline orange larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline green larger %}
   </div>

<!-- endtab -->

<!-- tab 示例源码 -->

1. 一组按钮

   ```
   This is my website, click the button {% btn 'https://blog.anheyu.com/',AnZhiYu %}
   This is my website, click the button {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right %}
   This is my website, click the button {% btn 'https://blog.anheyu.com/',AnZhiYu,,outline %}
   This is my website, click the button {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline %}
   This is my website, click the button {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,larger %}
   ```
2. 调整位置/大小

   ```
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,block %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,block center larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,block right outline larger %}
   ```
3. more than one button in center

   ```
   <span>
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,blue larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,pink larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,red larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,purple larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,orange larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,green larger %}
   </span>
   ```
4. 居中按钮

   ```
   <div class="btn-center">
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline blue larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline pink larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline red larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline purple larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline orange larger %}
   {% btn 'https://blog.anheyu.com/',AnZhiYu,anzhiyufont anzhiyu-icon-circle-arrow-right,outline green larger %}
   </div>
   ```

<!-- endtab -->

{% endtabs %}

---

## 网站卡片 sites

{% tabs Unique name, 2%}

<!-- tab 标签语法 -->

```
{% sitegroup %}
{% site 标题, url=链接, screenshot=截图链接, avatar=头像链接（可选）, description=描述（可选） %}
{% site 标题, url=链接, screenshot=截图链接, avatar=头像链接（可选）, description=描述（可选） %}
{% endsitegroup %}
```

<!-- endtab -->

<!-- tab 样式预览 -->

{% sitegroup %}
{% site xaoxuu, url=https://xaoxuu.com, screenshot=https://bu.dusays.com/2023/06/01/6478965ce6557.webp, avatar=https://cdn1.tianli0.top/gh/xaoxuu/cdn-assets/avatar/avatar.png, description=简约风格 %}
{% site Colsrch, url=https://colsrch.top, screenshot=https://i.loli.net/2020/08/22/dFRWXm52OVu8qfK.png, avatar=https://cdn1.tianli0.top/gh/Colsrch/images/Colsrch/avatar.jpg, description=这是一段关于这个网站的描述文字 %}
{% site Linhk1606, url=https://linhk1606.github.io, screenshot=https://bu.dusays.com/2023/06/01/6478963584621.png, avatar=https://bu.dusays.com/2023/06/01/6478968743368.png, description=这是一段关于这个网站的描述文字 %}
{% endsitegroup %}

<!-- endtab -->

<!-- tab 示例源码 -->

```
{% sitegroup %}
{% site xaoxuu, url=https://xaoxuu.com, screenshot=https://bu.dusays.com/2023/06/01/6478965ce6557.webp, avatar=https://cdn1.tianli0.top/gh/xaoxuu/cdn-assets/avatar/avatar.png, description=简约风格 %}
{% site Colsrch, url=https://colsrch.top, screenshot=https://i.loli.net/2020/08/22/dFRWXm52OVu8qfK.png, avatar=https://cdn1.tianli0.top/gh/Colsrch/images/Colsrch/avatar.jpg, description=这是一段关于这个网站的描述文字 %}
{% site Linhk1606, url=https://linhk1606.github.io, screenshot=https://bu.dusays.com/2023/06/01/6478963584621.png, avatar=https://bu.dusays.com/2023/06/01/6478968743368.png, description=这是一段关于这个网站的描述文字 %}
{% endsitegroup %}
```

<!-- endtab -->

{% endtabs %}

## 单张图片 image

{% tabs Unique name, 3%}

<!-- tab 标签语法 -->

```
{% image 链接, width=宽度（可选）, height=高度（可选）, alt=描述（可选）, bg=占位颜色（可选） %}
```

<!-- endtab -->

<!-- tab 配置参数 -->

1. 图片宽度高度：width=300px, height=32px
2. 图片描述：alt=图片描述（butterfly 需要在主题配置文件中开启图片描述）
3. 占位背景色：bg=#f2f2f2

<!-- endtab -->

<!-- tab 样式预览 -->

1. 添加描述：

   {% image https://s21.ax1x.com/2025/08/20/pVBXpLj.jpg, alt=看什么看，咬死你。 %}
2. 指定宽度：

   {% image https://s21.ax1x.com/2025/08/20/pVBXpLj.jpg, width=400px %}
3. 指定宽度并添加描述：

   {% image https://s21.ax1x.com/2025/08/20/pVBXpLj.jpg, width=400px, alt=看什么看，咬死你。 %}
4. 设置占位背景色：

   {% image https://s21.ax1x.com/2025/08/20/pVBXpLj.jpg, width=400px, bg=#1D0C04, alt=优化不同宽度浏览的观感 %}

<!-- endtab -->

<!-- tab 示例源码 -->

1. 添加描述：

   ```
   {% image https://bu.dusays.com/2023/06/01/6478937d7de6f.webp, alt=每天下课回宿舍的路，没有什么故事。 %}
   ```
2. 指定宽度：

   ```
   {% image https://bu.dusays.com/2023/06/01/6478937d7de6f.webp, width=400px %}
   ```
3. 指定宽度并添加描述：

   ```
   {% image https://bu.dusays.com/2023/06/01/6478937d7de6f.webp, width=400px, alt=每天下课回宿舍的路，没有什么故事。 %}
   ```
4. 设置占位背景色：

   ```
   {% image https://bu.dusays.com/2023/06/01/6478937d7de6f.webp, width=400px, bg=#1D0C04, alt=优化不同宽度浏览的观感 %}
   ```

<!-- endtab -->

{% endtabs %}

---

## inlineImg 行内图片

{% tabs 行内图片, 3 %}

<!-- tab 标签语法 -->

```
{% inlineImg [src] [height] %}

[src] : 图片链接
[height] ： 图片高度限制【可选】
```

<!-- endtab -->

<!-- tab 配置参数 -->


| 参数   | 含义                 |
| ------ | -------------------- |
| src    | 图片链接             |
| height | 图片高度限制【可选】 |

<!-- endtab -->

<!-- tab 样式预览 -->

你看我长得漂亮不

![](./../../../Imagebackup/pVBXpLj-1756193288502-4.jpg)

我觉得很漂亮 {% inlineImg https://i.loli.net/2021/03/19/5M4jUB3ynq7ePgw.png 150px %}

<!-- endtab -->

<!-- tab 示例源码 -->

```
你看我长得漂亮不

![](https://i.loli.net/2021/03/19/2P6ivUGsdaEXSFI.png)

我觉得很漂亮 {% inlineImg https://i.loli.net/2021/03/19/5M4jUB3ynq7ePgw.png 150px %}
```

<!-- endtab -->

{% endtabs %}

---

## 行内图片 inlineimage

{% tabs 行内图片 inlineimage, 3 %}

<!-- tab 标签语法 -->

```
{% inlineimage 图片链接, height=高度（可选） %}
```

<!-- endtab -->

<!-- tab 配置参数 -->

1. 高度：height=20px

<!-- endtab -->

<!-- tab 样式预览 -->

这是 {% inlineimage https://bu.dusays.com/2023/06/01/647895232e5d5.webp %} 一段话。

这又是 {% inlineimage https://bu.dusays.com/2022/05/19/6285328a83ca7.gif, height=40px %} 一段话。

<!-- endtab -->

<!-- tab 示例源码 -->

```
这是 {% inlineimage https://bu.dusays.com/2023/06/01/647895232e5d5.webp %} 一段话。

这又是 {% inlineimage https://bu.dusays.com/2022/05/19/6285328a83ca7.gif, height=40px %} 一段话。
```

<!-- endtab -->

{% endtabs %}

---

## label 标签

{% tabs label 标签, 3 %}

<!-- tab 标签语法 -->

```
{% label text color %}
```

<!-- endtab -->

<!-- tab 配置参数 -->


| 参数  | 含义                                                                        |
| ----- | --------------------------------------------------------------------------- |
| text  | 文字                                                                        |
| color | 【可选】背景颜色，默认为 default，default/blue/pink/red/purple/orange/green |

<!-- endtab -->

<!-- tab 样式预览 -->

臣亮言：{% label 先帝 %}创业未半，而{% label 中道崩殂 blue %}。今天下三分，{% label 益州疲敝 pink %}，此诚{% label 危急存亡之秋 red %}也！然侍衞之臣，不懈于内；{% label 忠志之士 purple %}，忘身于外者，盖追先帝之殊遇，欲报之于陛下也。诚宜开张圣听，以光先帝遗德，恢弘志士之气；不宜妄自菲薄，引喻失义，以塞忠谏之路也。
宫中、府中，俱为一体；陟罚臧否，不宜异同。若有{% label 作奸 orange %}、{% label 犯科 green %}，及为忠善者，宜付有司，论其刑赏，以昭陛下平明之治；不宜偏私，使内外异法也。

<!-- endtab -->

<!-- tab 示例源码 -->

```
臣亮言：{% label 先帝 %}创业未半，而{% label 中道崩殂 blue %}。今天下三分，{% label 益州疲敝 pink %}，此诚{% label 危急存亡之秋 red %}也！然侍衞之臣，不懈于内；{% label 忠志之士 purple %}，忘身于外者，盖追先帝之殊遇，欲报之于陛下也。诚宜开张圣听，以光先帝遗德，恢弘志士之气；不宜妄自菲薄，引喻失义，以塞忠谏之路也。
宫中、府中，俱为一体；陟罚臧否，不宜异同。若有{% label 作奸 orange %}、{% label 犯科 green %}，及为忠善者，宜付有司，论其刑赏，以昭陛下平明之治；不宜偏私，使内外异法也。
```

<!-- endtab -->

{% endtabs %}

---

## timeline

{% tabs timeline, 3 %}

<!-- tab 标签语法 -->

```
{% timeline title,color %}

<!-- timeline title -->

xxxxx

<!-- endtimeline -->
<!-- timeline title -->

xxxxx

<!-- endtimeline -->

{% endtimeline %}
```

<!-- endtab -->

<!-- tab 配置参数 -->


| 参数  | 含义                                                                       |
| ----- | -------------------------------------------------------------------------- |
| title | 标题/时间线                                                                |
| color | timeline 颜色，default(留空) / blue / pink / red / purple / orange / green |

<!-- endtab -->

<!-- tab 样式预览 -->

1. 默认颜色

   {% timeline 2022 %}

   <!-- timeline 01-02 -->

   这是测试页面

   <!-- endtimeline -->

   {% endtimeline %}
2. blue

   {% timeline 2022,blue %}

   <!-- timeline 01-02 -->

   这是测试页面

   <!-- endtimeline -->

   {% endtimeline %}
3. pink

   {% timeline 2022,pink %}

   <!-- timeline 01-02 -->

   这是测试页面

   <!-- endtimeline -->

   {% endtimeline %}
4. red

   {% timeline 2022,red %}

   <!-- timeline 01-02 -->

   这是测试页面

   <!-- endtimeline -->

   {% endtimeline %}
5. purple

   {% timeline 2022,purple %}

   <!-- timeline 01-02 -->

   这是测试页面

   <!-- endtimeline -->

   {% endtimeline %}
6. orange

   {% timeline 2022,orange %}

   <!-- timeline 01-02 -->

   这是测试页面

   <!-- endtimeline -->

   {% endtimeline %}
7. green

{% timeline 2022,green %}

<!-- timeline 01-02 -->

这是测试页面

<!-- endtimeline -->

{% endtimeline %}

<!-- endtab -->

<!-- tab 示例源码 -->

1. 默认颜色

   ```
   {% timeline 2022 %}
   <!-- timeline 01-02 -->

   这是测试页面
   <!-- endtimeline -->

   {% endtimeline %}
   ```
2. blue

   ```
   {% timeline 2022,blue %}
   <!-- timeline 01-02 -->

   这是测试页面
   <!-- endtimeline -->

   {% endtimeline %}
   ```
3. pink

   ```
   {% timeline 2022,pink %}
   <!-- timeline 01-02 -->

   这是测试页面
   <!-- endtimeline -->

   {% endtimeline %}
   ```
4. red

   ```
   {% timeline 2022,red %}
   <!-- timeline 01-02 -->

   这是测试页面
   <!-- endtimeline -->

   {% endtimeline %}
   ```
5. purple

   ```
   {% timeline 2022,purple %}
   <!-- timeline 01-02 -->

   这是测试页面
   <!-- endtimeline -->

   {% endtimeline %}
   ```
6. orange

   ```
   {% timeline 2022,orange %}
   <!-- timeline 01-02 -->

   这是测试页面
   <!-- endtimeline -->

   {% endtimeline %}
   ```
7. green

   ```
   {% timeline 2022,green %}
   <!-- timeline 01-02 -->

   这是测试页面
   <!-- endtimeline -->

   {% endtimeline %}
   ```

<!-- endtab -->

{% endtabs %}

---

## flink 友链标签

{% note blue 'anzhiyufont anzhiyu-icon-bullhorn' simple %}可在任何界面插入类似`友情链接`列表效果，内容格式与友情链接界面一样，支持 `yml 格式`,注意`yml数据`具有格式要求，请注意格式对齐，防止被编辑器格式化导致格式错误从而报错。{% endnote %}

{% tabs flink 友链标签, 3 %}

<!-- tab 标签语法 -->

```
{% flink %}
xxxxxx
{% endflink %}
```

<!-- endtab -->

<!-- tab 配置参数 -->


| 参数        | 含义                                                |
| ----------- | --------------------------------------------------- |
| class_name  | h2标题                                              |
| flink_style | 【可选】友链样式，默认为 flexcard，flexcard/anzhiyu |
| link_list   | 【可选】友链样式，默认为 flexcard，flexcard/anzhiyu |

<!-- endtab -->

<!-- tab 样式预览 -->

{% flink %}

- class_name: 推荐博客
  flink_style: flexcard
  link_list:

  - name: 安知鱼
    link: https://blog.anheyu.com/
    avatar: https://npm.elemecdn.com/anzhiyu-blog-static@1.0.4/img/avatar.jpg
    descr: 生活明朗，万物可爱
    siteshot: https://npm.elemecdn.com/anzhiyu-theme-static@1.1.6/img/blog.anheyu.com.jpg
- class_name: 网站
  class_desc: 值得推荐的网站
  flink_style: anzhiyu
  link_list:

  - name: Youtube
    link: https://www.youtube.com/
    avatar: https://i.loli.net/2020/05/14/9ZkGg8v3azHJfM1.png
    descr: 视频网站
  - name: Weibo
    link: https://www.weibo.com/
    avatar: https://i.loli.net/2020/05/14/TLJBum386vcnI1P.png
    descr: 中国最大社交分享平台
  - name: Twitter
    link: https://twitter.com/
    avatar: https://i.loli.net/2020/05/14/5VyHPQqR6LWF39a.png
    descr: 社交分享平台
    {% endflink %}

<!-- endtab -->

<!-- tab 示例源码 -->

```
{% flink %}
- class_name: 推荐博客
  flink_style: flexcard
  link_list:
    - name: 安知鱼
      link: https://blog.anheyu.com/
      avatar: https://npm.elemecdn.com/anzhiyu-blog-static@1.0.4/img/avatar.jpg
      descr: 生活明朗，万物可爱
      siteshot: https://npm.elemecdn.com/anzhiyu-theme-static@1.1.6/img/blog.anheyu.com.jpg

- class_name: 网站
  class_desc: 值得推荐的网站
  flink_style: anzhiyu
  link_list:
    - name: Youtube
      link: https://www.youtube.com/
      avatar: https://i.loli.net/2020/05/14/9ZkGg8v3azHJfM1.png
      descr: 视频网站
    - name: Weibo
      link: https://www.weibo.com/
      avatar: https://i.loli.net/2020/05/14/TLJBum386vcnI1P.png
      descr: 中国最大社交分享平台
    - name: Twitter
      link: https://twitter.com/
      avatar: https://i.loli.net/2020/05/14/5VyHPQqR6LWF39a.png
      descr: 社交分享平台
{% endflink %}
```

<!-- endtab -->

{% endtabs %}

---

## mermaid 图

{% note blue 'anzhiyufont anzhiyu-icon-bullhorn' simple %}使用`mermaid标签`可以绘制Flowchart（流程图）、Sequence diagram（时序图 ）、Class Diagram（类别图）、State Diagram（状态图）、Gantt（甘特图）和Pie Chart（圆形图），具体可以查看[mermaid文档](https://mermaid.js.org/#/){% endnote %}

修改 `主题配置文件`

```
# mermaid
# see https://github.com/mermaid-js/mermaid
mermaid:
  enable: true
  # built-in themes: default/forest/dark/neutral
  theme:
    light: default
    dark: dark
```

{% tabs label mermaid 图, 2 %}

<!-- tab 标签语法 -->

```
{% mermaid %}
内容
{% endmermaid %}
```

<!-- endtab -->

<!-- tab 样式预览 -->

{% mermaid %}
pie
title Key elements in Product X
"Calcium" : 42.96
"Potassium" : 50.05
"Magnesium" : 10.01
"Iron" :  5
{% endmermaid %}

<!-- endtab -->

<!-- tab 示例源码 -->

```
{% mermaid %}
pie
    title Key elements in Product X
    "Calcium" : 42.96
    "Potassium" : 50.05
    "Magnesium" : 10.01
    "Iron" :  5
{% endmermaid %}
```

<!-- endtab -->

{% endtabs %}

---

## 复选列表 checkbox

{% tabs 复选列表 checkbox, 3 %}

<!-- tab 标签语法 -->

```
{% checkbox 样式参数（可选）, 文本（支持简单md） %}
```

<!-- endtab -->

<!-- tab 配置参数 -->

1. 样式: plus, minus, times
2. 颜色: {% span red, red%},{% span yellow, yellow%},{% span green, green%},{% span cyan, cyan%},{% span blue, blue%},{% span gray, gray %}
3. 选中状态: checked

<!-- endtab -->

<!-- tab 样式预览 -->

{% checkbox 纯文本测试 %}
{% checkbox checked, 支持简单的 [markdown](https://guides.github.com/features/mastering-markdown/) 语法 %}
{% checkbox red, 支持自定义颜色 %}
{% checkbox green checked, 绿色 + 默认选中 %}
{% checkbox yellow checked, 黄色 + 默认选中 %}
{% checkbox cyan checked, 青色 + 默认选中 %}
{% checkbox blue checked, 蓝色 + 默认选中 %}
{% checkbox plus green checked, 增加 %}
{% checkbox minus yellow checked, 减少 %}
{% checkbox times red checked, 叉 %}

<!-- endtab -->

<!-- tab 示例源码 -->

```
{% checkbox 纯文本测试 %}
{% checkbox checked, 支持简单的 [markdown](https://guides.github.com/features/mastering-markdown/) 语法 %}
{% checkbox red, 支持自定义颜色 %}
{% checkbox green checked, 绿色 + 默认选中 %}
{% checkbox yellow checked, 黄色 + 默认选中 %}
{% checkbox cyan checked, 青色 + 默认选中 %}
{% checkbox blue checked, 蓝色 + 默认选中 %}
{% checkbox plus green checked, 增加 %}
{% checkbox minus yellow checked, 减少 %}
{% checkbox times red checked, 叉 %}
```

<!-- endtab -->

{% endtabs %}

---

## dogeplayer 多吉云播放器

{% note blue 'anzhiyufont anzhiyu-icon-bullhorn' simple %}快捷引入[多吉云视频](https://console.dogecloud.com/vod/overview){% endnote %}

{% tabs dogeplayer 多吉云播放器, 3 %}

<!-- tab 标签语法 -->

```
{% dogeplayer 4945 ebb742fd1f0b5a7b %}
```

<!-- endtab -->

<!-- tab 配置参数 -->

获取`userId`与`vcode`

![pVyW54g.webp](https://s21.ax1x.com/2025/08/26/pVyW54g.webp)


| 参数   | 含义         |
| ------ | ------------ |
| userId | 多吉云userId |
| vcode  | 视频vcode    |

<!-- endtab -->

<!-- tab 样式预览 -->

{% dogeplayer 4945 ebb742fd1f0b5a7b %}

<!-- endtab -->

<!-- tab 示例源码 -->

```
{% dogeplayer 4945 ebb742fd1f0b5a7b %}
```

<!-- endtab -->

{% endtabs %}

---

## 折叠框 folding

{% note blue 'anzhiyufont anzhiyu-icon-bullhorn' simple %}折叠框 folding{% endnote %}

{% tabs 折叠框 folding, 3 %}

<!-- tab 标签语法 -->

```
{% folding 参数（可选）, 标题 %}
![](https://bu.dusays.com/2023/06/01/64788d71c832d.webp)
{% endfolding %}
```

<!-- endtab -->

<!-- tab 配置参数 -->

1. 颜色：blue, cyan, green, yellow, red
2. 状态：状态填写 open 代表默认打开。

<!-- endtab -->

<!-- tab 样式预览 -->

{% folding 查看图片测试 %}

![](https://bu.dusays.com/2023/06/01/64788d71c832d.webp)

{% endfolding %}

{% folding cyan open, 查看默认打开的折叠框 %}

这是一个默认打开的折叠框。

{% endfolding %}

{% folding green, 查看代码测试 %}
假装这里有代码块（代码块没法嵌套代码块）
{% endfolding %}

{% folding yellow, 查看列表测试 %}

- haha
- hehe

{% endfolding %}

{% folding red, 查看嵌套测试 %}

{% folding, 查看嵌套测试2 %}

{% folding 查看嵌套测试3 %}

hahaha <span><img src='./../../../Imagebackup/64788cd5a356b.png' style='height:24px'></span>

{% endfolding %}

{% endfolding %}

{% endfolding %}

<!-- endtab -->

<!-- tab 示例源码 -->

```
{% folding 查看图片测试 %}

![](https://bu.dusays.com/2023/06/01/64788d71c832d.webp)

{% endfolding %}

{% folding cyan open, 查看默认打开的折叠框 %}

这是一个默认打开的折叠框。

{% endfolding %}

{% folding green, 查看代码测试 %}
假装这里有代码块（代码块没法嵌套代码块）
{% endfolding %}

{% folding yellow, 查看列表测试 %}

- haha
- hehe

{% endfolding %}

{% folding red, 查看嵌套测试 %}

{% folding, 查看嵌套测试2 %}

{% folding 查看嵌套测试3 %}

hahaha <span><img src='https://bu.dusays.com/2023/06/01/64788cd5a356b.png' style='height:24px'></span>

{% endfolding %}

{% endfolding %}

{% endfolding %}
```

<!-- endtab -->

{% endtabs %}

---

## Gallery 相册图库

一个图库集合。

{% tabs Gallery 相册图库, 3 %}

<!-- tab 标签语法 -->

1. gallerygroup 相册图库

   ```
   <div class="gallery-group-main">
   {% galleryGroup name description link img-url %}
   {% galleryGroup name description link img-url %}
   {% galleryGroup name description link img-url %}
   </div>
   ```
2. gallery 相册

   {% tabs gallery 相册, 1 %}

   <!-- tab 本地 -->

   ```
   {% gallery %}
   markdown 图片格式
   {% endgallery %}

   {% gallery true,220,10 %}
   markdown 图片格式
   {% endgallery %}

   {% gallery true,,10 %}
   markdown 图片格式
   {% endgallery %}
   ```


   | 参数名    | 释义                                                                                |
   | --------- | ----------------------------------------------------------------------------------- |
   | lazyload  | 【可选】点击按钮加载更多图片，填写 true/false。默认为`false`。                      |
   | rowHeight | 【可选】图片显示的高度，如果需要一行显示更多的图片，可设置更小的数字。默认为`220`。 |
   | limit     | 【可选】每次加载多少张照片。默认为`10`。                                            |


   <!-- endtab -->

   <!-- tab 远程 -->

   ```
   {% gallery url,[link],[lazyload],[rowHeight],[limit] %}
   {% endgallery %}
   ```


   | 参数名    | 释义                                                                                |
   | --------- | ----------------------------------------------------------------------------------- |
   | url       | 【必须】 识别词                                                                     |
   | link      | 【必须】远程的 json 链接                                                            |
   | lazyload  | 【可选】点击按钮加载更多图片，填写 true/false。默认为`false`。                      |
   | rowHeight | 【可选】图片显示的高度，如果需要一行显示更多的图片，可设置更小的数字。默认为`220`。 |
   | limit     | 【可选】每次加载多少张照片。默认为`10`。                                            |

   远程链接 Json 的例子

   有三个参数，`url`是必须存在的，`alt` 和 `title` 可有，也可没有

   ```
   [
     {
       "url": "https://cdn1.tianli0.top/gh/jerryc127/CDN/img/IMG_0556.jpg",
       "alt": "IMG_0556.jpg",
       "title": "这是title"
     },
     {
       "url": "https://cdn1.tianli0.top/gh/jerryc127/CDN/img/IMG_0472.jpg",
       "alt": "IMG_0472.jpg"
     },
     {
       "url": "https://cdn1.tianli0.top/gh/jerryc127/CDN/img/IMG_0453.jpg",
       "alt": ""
     },
     {
       "url": "https://cdn1.tianli0.top/gh/jerryc127/CDN/img/IMG_0931.jpg",
       "alt": ""
     }
   ]
   ```

   示例

   ```
   {% gallery url,https://xxxx.com/sss.json %}
   {% endgallery %}

   {% gallery url,https://xxxx.com/sss.json,true,220,10 %}
   {% endgallery %}

   {% gallery url,https://xxxx.com/sss.json,true,,10 %}
   {% endgallery %}
   ```

   <!-- endtab -->

   {% endtabs %}

<!-- endtab -->

<!-- tab 配置参数 -->

- gallerygroup 相册图库


| 参数名      | 释义                 |
| ----------- | -------------------- |
| name        | 图库名字             |
| description | 图库描述             |
| link        | 链接到对应相册的地址 |
| img-url     | 图库封面             |

```
{% note info simple %}思维拓展一下，相册图库的实质其实就是个快捷方式，可以自定义添加描述、封面、链接。那么我们未必要把它当做一个相册，完全可以作为一个链接卡片，链接到视频、QQ、友链都是不错的选择。{% endnote %}
```

- gallery 相册

区别于旧版的 Gallery 相册,新的 Gallery 相册会自动根据图片长度进行排版，书写也更加方便，与 markdown 格式一样。可根据需要插入到相应的 md。无需再自己配置长宽。**建议在粘贴时故意使用长短、大小、横竖不一的图片**，会有更好的效果。（尺寸完全相同的图片只会平铺输出，效果很糟糕）

{% tabs gallery 相册, 1 %}

<!-- tab 本地 -->

```
{% gallery %}
markdown 图片格式
{% endgallery %}

{% gallery true,220,10 %}
markdown 图片格式
{% endgallery %}

{% gallery true,,10 %}
markdown 图片格式
{% endgallery %}
```


| 参数名    | 释义                                                                                |
| --------- | ----------------------------------------------------------------------------------- |
| lazyload  | 【可选】点击按钮加载更多图片，填写 true/false。默认为`false`。                      |
| rowHeight | 【可选】图片显示的高度，如果需要一行显示更多的图片，可设置更小的数字。默认为`220`。 |
| limit     | 【可选】每次加载多少张照片。默认为`10`。                                            |

<!-- endtab -->

<!-- tab 远程 -->

```
{% gallery url,[link],[lazyload],[rowHeight],[limit] %}
{% endgallery %}
```


| 参数名    | 释义                                                                                |
| --------- | ----------------------------------------------------------------------------------- |
| url       | 【必须】 识别词                                                                     |
| link      | 【必须】远程的 json 链接                                                            |
| lazyload  | 【可选】点击按钮加载更多图片，填写 true/false。默认为`false`。                      |
| rowHeight | 【可选】图片显示的高度，如果需要一行显示更多的图片，可设置更小的数字。默认为`220`。 |
| limit     | 【可选】每次加载多少张照片。默认为`10`。                                            |

远程链接 Json 的例子

有三个参数，`url`是必须存在的，`alt` 和 `title` 可有，也可没有。

```
[
  {
    "url": "https://cdn1.tianli0.top/gh/jerryc127/CDN/img/IMG_0556.jpg",
    "alt": "IMG_0556.jpg",
    "title": "这是title"
  },
  {
    "url": "https://cdn1.tianli0.top/gh/jerryc127/CDN/img/IMG_0472.jpg",
    "alt": "IMG_0472.jpg"
  },
  {
    "url": "https://cdn1.tianli0.top/gh/jerryc127/CDN/img/IMG_0453.jpg",
    "alt": ""
  },
  {
    "url": "https://cdn1.tianli0.top/gh/jerryc127/CDN/img/IMG_0931.jpg",
    "alt": ""
  }
]
```

示例

```
{% gallery url,https://xxxx.com/sss.json %}
{% endgallery %}

{% gallery url,https://xxxx.com/sss.json,true,220,10 %}
{% endgallery %}

{% gallery url,https://xxxx.com/sss.json,true,,10 %}
{% endgallery %}
```

<!-- endtab -->

{% endtabs %}

<!-- endtab -->

<!-- tab 样式预览 -->

1. gallerygroup 相册图库

   <div class="gallery-group-main">
    {% galleryGroup MC 在Rikkaの六花服务器里留下的足迹 '/wordScenery/' https://bu.dusays.com/2023/06/01/64788f24d05bd.webp %}
    {% galleryGroup Gundam 哦咧哇gundam哒！ '/thousand/' https://bu.dusays.com/2023/06/01/64788f456fc3d.webp %}
    {% galleryGroup I-am-Akilar 某种意义上也算自拍吧 '/wallpaper/' https://bu.dusays.com/2023/06/01/64788f83e5fa1.webp %}
   </div>
2. gallery 相册

   {% gallery true,,2 %}
   ![](https://bu.dusays.com/2023/06/01/647896b15759c.jpg)
   ![](https://bu.dusays.com/2023/06/01/647896cabde59.jpg)
   ![](https://bu.dusays.com/2023/06/01/647896eb0f3ea.jpg)
   ![](https://bu.dusays.com/2023/06/01/647890012b1ec.webp)
   ![](https://i.loli.net/2019/12/25/6nepIJ1xTgufatZ.jpg)
   ![](https://i.loli.net/2019/12/25/E7Jvr4eIPwUNmzq.jpg)
   ![](https://i.loli.net/2019/12/25/mh19anwBSWIkGlH.jpg)
   ![](https://i.loli.net/2019/12/25/2tu9JC8ewpBFagv.jpg)
   {% endgallery %}

<!-- endtab -->

<!-- tab 示例源码 -->

{% note info simple %}对于很多同学提问的gallerygroup和gallery相册页的链接问题。这里说下我个人的使用习惯。一般使用相册图库的话，可以在导航栏加一个 gallery 的 page(**使用指令`hexo new page gallery`添加**)，里面放相册图库作为封面。然后在`[Blogroot]/source/gallery/`下面建立相应的文件夹，例如若按照这里的示例，若欲使用`/gallery/MC/`路径访问 MC 相册，则需要新建`[Blogroot]/source/gallery/MC/index.md`，并在里面填入`gallery`相册内容。注意 ⚠️：本站相册集为单独优化，可参考[配置相册页面](https://blog.anheyu.com/posts/220c.html)。{% endnote %}

1. gallerygroup 相册图库

   ```
   <div class="gallery-group-main">
    {% galleryGroup MC 在Rikkaの六花服务器里留下的足迹 '/wordScenery/' https://bu.dusays.com/2023/06/01/64788f24d05bd.webp %}
    {% galleryGroup Gundam 哦咧哇gundam哒！ '/thousand/' https://bu.dusays.com/2023/06/01/64788f456fc3d.webp %}
    {% galleryGroup I-am-Akilar 某种意义上也算自拍吧 '/wallpaper/' https://bu.dusays.com/2023/06/01/64788f83e5fa1.webp %}
   </div>
   ```
2. gallery 相册

   ```
   {% gallery true,,2 %}
   ![](https://bu.dusays.com/2023/06/01/647896b15759c.jpg)
   ![](https://bu.dusays.com/2023/06/01/647896cabde59.jpg)
   ![](https://bu.dusays.com/2023/06/01/647896eb0f3ea.jpg)
   ![](https://bu.dusays.com/2023/06/01/647890012b1ec.webp)
   ![](https://i.loli.net/2019/12/25/6nepIJ1xTgufatZ.jpg)
   ![](https://i.loli.net/2019/12/25/E7Jvr4eIPwUNmzq.jpg)
   ![](https://i.loli.net/2019/12/25/mh19anwBSWIkGlH.jpg)
   ![](https://i.loli.net/2019/12/25/2tu9JC8ewpBFagv.jpg)
   {% endgallery %}
   ```

<!-- endtab -->

{% endtabs %}


![](https://dlink.host/1drv/aHR0cHM6Ly8xZHJ2Lm1zL2kvYy9mNzAwYmM1NGU3YTk2MWQ1L0VlV2I2bTBuck50T29KdzZBWmx4UExzQk82M0tfS2ZRRVBQOXdLbWdjVTJfTEE_ZT1iM1RURlQ.jpg)
