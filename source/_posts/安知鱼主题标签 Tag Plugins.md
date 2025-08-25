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

{% tabs Unique name, [index] %}

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

{% tabs Unique name, [index] %}

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

{% tabs Unique name, [index] %}

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

{% tabs Unique name, [index] %}

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

{% tabs Unique name, [index] %}

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

{% tabs Unique name, [index] %}

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

{% tabs Unique name, [index] %}

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

{% tabs Unique name, [index] %}

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



嘻嘻嘻
